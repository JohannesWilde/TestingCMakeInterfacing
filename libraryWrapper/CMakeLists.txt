
add_library(libraryWrapper
    libraryWrapper.cpp
)

target_include_directories(libraryWrapper
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(libraryWrapper
    PRIVATE libraryInterface
)
