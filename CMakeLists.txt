cmake_minimum_required(VERSION 3.14)
project(interception)

# 编译选项
option(INTERCEPTION_WITH_SAMPLE "Build interception with sample" ON)

# 设置include目录
include_directories(library)

add_subdirectory(library)

if (INTERCEPTION_WITH_SAMPLE)
    include_directories(samples)
    add_subdirectory(samples)
endif()