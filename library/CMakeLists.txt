
add_library(libraryInterface INTERFACE)

target_include_directories(libraryInterface
    INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}
)


add_library(library1
    library1.cpp
)

target_link_libraries(library1
    PUBLIC libraryInterface
)


add_library(library2
    library2.cpp
)

target_link_libraries(library2
    PUBLIC libraryInterface
)
