project (hello C)
cmake_minimum_required(VERSION 2.8.9)

set(hello_SOURCES "src/main.c")

add_subdirectory("sourkode")
include_directories("sourkode/inc")
add_executable(hello WIN32 ${hello_SOURCES} ${hello_HEADERS})
target_link_libraries(hello sourkode ${SOURKODE_LIBRARIES})
