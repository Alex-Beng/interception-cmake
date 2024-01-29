add_library(interception SHARED interception.c)
# install(TARGETS interception DESTINATION ${CMAKE_BINARY_DIR})
install(TARGETS interception DESTINATION lib)
install(FILES interception.h DESTINATION include)
install(FILES interception.h DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

export(TARGETS interception FILE interceptionConfig.cmake)