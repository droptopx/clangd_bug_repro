set(NAME BadApp)

file(GLOB TARGET_SOURCE_FILES "./*.m" "./*.c")
file(GLOB TARGET_HEADER_FILES "./*.h")

add_executable(
    ${NAME}
    ${TARGET_SOURCE_FILES}
)

target_compile_options(${NAME} PRIVATE -fmodules)
target_link_libraries(${NAME} BadModule)
# target_include_directories(${NAME} PRIVATE BadModule)
