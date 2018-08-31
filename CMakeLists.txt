cmake_minimum_required(VERSION 3.1)
project(game.libretro.cannonball)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-cannonball REQUIRED)

set(CANNONBALL_CUSTOM_BINARY ${CANNONBALL_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} CANNONBALL "")

include(CPack)
