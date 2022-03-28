cmake_minimum_required(VERSION 3.5)

project(TestingCMakeInterfacing LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(library)
add_subdirectory(libraryWrapper)

add_executable(TestingCMakeInterfacing
    main.cpp
)

target_link_libraries(TestingCMakeInterfacing
    PRIVATE library2
    PRIVATE libraryWrapper
)


