project(game.libretro.beetle-lynx)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(libretro-beetle-lynx REQUIRED)

set(DEPLIBS beetle-lynx)
set(BEETLE_LYNX_CUSTOM_BINARY ${BEETLE_LYNX_LIB}
                              ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX} beetle-lynx)

build_addon(${PROJECT_NAME} BEETLE_LYNX DEPLIBS)
