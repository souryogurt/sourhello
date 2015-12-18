project (hello C)
cmake_minimum_required(VERSION 2.8.9)
set(CMAKE_SHARED_LIBRARY_LINK_C_FLAGS "")

set(hello_SOURCES "src/main.c")

add_subdirectory("sourkode")
include_directories("sourkode/inc")
add_executable(hello ${hello_SOURCES} ${hello_HEADERS})
target_link_libraries(hello sourkode ${SOURKODE_LIBRARIES})
