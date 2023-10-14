cmake_minimum_required(VERSION 3.28.0)

project(c-template VERSION 0.1.0 LANGUAGES C)

include(CTest)
enable_testing()

set(EXECUTABLE_OUTPUT_PATH  ${PROJECT_SOURCE_DIR}/bin)

# Add all files in package
FILE(GLOB package_dir package/*.c package/*.h)
ADD_EXECUTABLE(c-template main.c ${package_dir})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
