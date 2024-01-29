add_library(interception SHARED interception.c)
target_include_directories(interception PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})