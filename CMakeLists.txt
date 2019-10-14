cmake_minimum_required(VERSION 3.2)
project (hello)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
set(mylib src/hello.cpp inc)

add_library(mylib STATIC ${mylib})

include_directories(inc)
add_executable(hello src/main.cpp)
target_link_libraries(hello mylib)




#install(TARGETS mylib DESTINATION lib)
#install(FILES mylib.h DESTIONATION include)
#file(GLOB SOURCES "*.cpp")
