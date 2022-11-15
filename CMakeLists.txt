cmake_minimum_required(VERSION 3.5)
project(SpaceExplorationGame)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES main.cpp)
add_executable(SpaceExplorationGame ${SOURCE_FILES} main.cpp)

INCLUDE_DIRECTORIES(  /usr/local/Cellar/allegro/5.2.8.0_2/include )
LINK_DIRECTORIES(  /usr/local/Cellar/allegro/5.2.8.0_2/lib )

file(GLOB LIBRARIES "/usr/local/Cellar/allegro/5.2.8.0_2/lib/*.dylib")
message("LIBRARIES = ${LIBRARIES}")

TARGET_LINK_LIBRARIES(SpaceExplorationGame  ${LIBRARIES})