project( BOOST )
cmake_minimum_required( VERSION 2.6 )

message( "cmake command is " ${CMAKE_COMMAND} )
# execute_process( COMMAND "${CMAKE_COMMAND}" "-E" "tar" "xJ" "${CMAKE_SOURCE_DIR}/include.zip" )
execute_process(COMMAND ${CMAKE_COMMAND} -E tar xzf include.tar.gz )

# build MiniBoost
include_directories( ${CMAKE_SOURCE_DIR}/include )
add_subdirectory( libs )

add_executable( ${PROJECT_NAME} main.cpp )
target_link_libraries( ${PROJECT_NAME} MiniBoost )
