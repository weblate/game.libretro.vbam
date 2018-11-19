cmake_minimum_required(VERSION 3.1)
project(game.libretro.vbam)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(VBAM_LIB NAMES vbam_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(VBAM_CUSTOM_BINARY ${VBAM_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} VBAM "")

include(CPack)
