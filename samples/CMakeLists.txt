# 递归搜索当前目录下的所有源文件
file(GLOB_RECURSE SAMPLE_SOURCES *.c *.cpp *.cc *.h *.hpp *.hh)
list(REMOVE_ITEM SAMPLE_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/utils.c)
list(REMOVE_ITEM SAMPLE_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/utils.h)

# 输出所有的源文件
# message(STATUS "SAMPLE_SOURCES: ${SAMPLE_SOURCES}")

foreach(SAMPLE_SRC ${SAMPLE_SOURCES})
    get_filename_component(SAMPLE_NAME ${SAMPLE_SRC} NAME_WE)

    add_executable(${SAMPLE_NAME} ${SAMPLE_SRC} utils.c)
    target_link_libraries(${SAMPLE_NAME} interception)
    
endforeach(SAMPLE_SRC )


