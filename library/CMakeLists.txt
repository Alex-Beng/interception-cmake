add_library(interception SHARED interception.c)
# install(TARGETS interception DESTINATION ${CMAKE_BINARY_DIR})
install(TARGETS interception DESTINATION lib)
install(FILES interception.h DESTINATION include)

export(TARGETS interception FILE interceptionConfig.cmake)