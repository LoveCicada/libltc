cmake_minimum_required(VERSION 3.10)

# 项目信息
project(libltc VERSION 1.3.2 LANGUAGES C)

# 设置静态库输出目录
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

# 添加源文件
set(SOURCES
    src/decoder.c
    src/encoder.c
    src/ltc.c
    src/timecode.c
)

# 添加头文件目录
include_directories(${CMAKE_SOURCE_DIR}/include)

# 生成静态库
add_library(ltc STATIC ${SOURCES})

# 安装目标
install(TARGETS ltc
    ARCHIVE DESTINATION lib
)

# 安装头文件
install(DIRECTORY include/
    DESTINATION include
    FILES_MATCHING PATTERN "*.h"
)
