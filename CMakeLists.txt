cmake_minimum_required(VERSION 3.1)
project(game.libretro.bsnes-mercury-balanced)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-bsnes-mercury-balanced REQUIRED)

set(DEPLIBS bsnes-mercury-balanced)
set(BSNES_MERCURY_CUSTOM_BINARY ${BSNES_MERCURY_LIB}
                                ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BSNES_MERCURY DEPLIBS)
