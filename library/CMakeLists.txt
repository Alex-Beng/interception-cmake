add_library(interception SHARED interception.c)
target_include_directories(interception PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

set_target_properties(interception PROPERTIES
    PUBLIC_HEADER interception.h
)

install(TARGETS interception
    ARCHIVE DESTINATION lib
    LIBRARY DESTINATION lib
    PUBLIC_HEADER DESTINATION include
)
