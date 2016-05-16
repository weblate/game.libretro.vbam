project(game.libretro.vbam)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(Kodi REQUIRED)
find_package(libretro-vbam REQUIRED)

set(DEPLIBS vbam)
set(VBAM_CUSTOM_BINARY ${VBAM_LIB}
                       game.libretro.vbam${CMAKE_SHARED_LIBRARY_SUFFIX} vbam)

build_addon(game.libretro.vbam VBAM DEPLIBS)
