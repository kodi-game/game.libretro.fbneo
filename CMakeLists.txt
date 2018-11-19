cmake_minimum_required(VERSION 3.1)
project(game.libretro.fbalpha)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(FBALPHA_LIB NAMES fbalpha_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(FBALPHA_CUSTOM_BINARY ${FBALPHA_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} FBALPHA "")

include(CPack)
