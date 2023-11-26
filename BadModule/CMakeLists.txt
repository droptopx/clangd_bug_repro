cmake_minimum_required(VERSION 3.8)

set(MODULE_NAME BadModule)

file(GLOB TARGET_HEADER_FILES "./*.h")
file(GLOB TARGET_MODULE_MAP "./module.modulemap")

add_library(
    ${MODULE_NAME}
    SHARED
    ${TARGET_HEADER_FILES}
    ${TARGET_MODULE_MAP}
)

set_target_properties(${MODULE_NAME} PROPERTIES LINKER_LANGUAGE C)

target_include_directories(${MODULE_NAME} INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}")
