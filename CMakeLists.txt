cmake_minimum_required(VERSION 3.1)
project(game.libretro.bsnes-mercury-balanced)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(BSNES-MERCURY-BALANCED_LIB NAMES bsnes_mercury_balanced_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(BSNES-MERCURY-BALANCED_CUSTOM_BINARY ${BSNES-MERCURY-BALANCED_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BSNES-MERCURY-BALANCED "")

include(CPack)
