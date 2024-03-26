#CMake version
cmake_minimum_required(VERSION 3.29.0)

#set language standard
set(CMAKE_CXX_STANDARD 11)

#set project name
project(compilelualib)

#add source
aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR}/luasource luafilesource)

#add target

add_library(lualib ${luafilesource})

target_include_directories(lualib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/luasource)


