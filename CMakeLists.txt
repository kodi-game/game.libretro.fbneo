cmake_minimum_required(VERSION 3.1)
project(game.libretro.fbalpha)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-fbalpha REQUIRED)

set(FBALPHA_CUSTOM_BINARY ${FBALPHA_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} FBALPHA "")

include(CPack)
