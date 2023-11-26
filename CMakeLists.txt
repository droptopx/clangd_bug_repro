cmake_minimum_required(VERSION 3.8)
project(ClangdBugRepro LANGUAGES C OBJC)

add_subdirectory(BadModule)
add_subdirectory(BadApp)
