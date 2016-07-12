project( BOOST )
cmake_minimum_required( VERSION 2.6 )

include_directories( ${CMAKE_SOURCE_DIR}/include )

# build MiniBoost
add_subdirectory( libs )

add_executable( ${PROJECT_NAME} main.cpp )
target_link_libraries( ${PROJECT_NAME} MiniBoost )
