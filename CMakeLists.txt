cmake_minimum_required(VERSION 2.8)

set(
        CMAKE_RUNTIME_OUTPUT_DIRECTORY
        ${CMAKE_HOME_DIRECTORY}/bin
)

add_definitions(
        -std=c++11
)

link_libraries(
        -lopencv_contrib
        -lopencv_core
        -lopencv_highgui
        -lopencv_imgproc
)

FILE(GLOB_RECURSE sourcefiles "src/*.cpp")

add_executable( main ${sourcefiles} )