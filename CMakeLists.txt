project(game.libretro.bsnes-mercury)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(libretro-bsnes-mercury REQUIRED)

set(DEPLIBS bsnes-mercury)
set(BSNES_MERCURY_CUSTOM_BINARY ${BSNES_MERCURY_LIB}
                           game.libretro.bsnes-mercury${CMAKE_SHARED_LIBRARY_SUFFIX} bsnes-mercury)

		   build_addon(game.libretro.bsnes-mercury BSNES_MERCURY DEPLIBS)
