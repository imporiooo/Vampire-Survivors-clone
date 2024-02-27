cmake_minimum_required(VERSION 3.10)


project(Test)


add_executable(${PROJECT_NAME} Main.cpp)


option(BUILD_SHARED_LIBS "Build shared libraries" OFF)

include(FetchContent)
FetchContent_Declare(
  SFML
  GIT_REPOSITORY https://github.com/SFML/SFML.git
  GIT_TAG 2.6.x)
FetchContent_MakeAvailable(SFML)
target_link_libraries(${PROJECT_NAME} sfml-graphics)