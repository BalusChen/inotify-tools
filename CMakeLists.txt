cmake_minimum_required(VERSION 3.7)
project(inotify_tools C)

set(CMAKE_C_STANDARD 11)

include_directories(libinotifytools/src)
include_directories(libinotifytools/src/inotifytools)
include_directories(src)

add_executable(inotify_tools
        config.h
        libinotifytools/src/inotifytools/inotify-nosys.h
        libinotifytools/src/inotifytools/inotifytools.h
        libinotifytools/src/example.c
        libinotifytools/src/inotifytools.c
        libinotifytools/src/inotifytools_p.h
        libinotifytools/src/redblack.c
        libinotifytools/src/redblack.h
        libinotifytools/src/test.c
        src/common.c
        src/common.h
        src/inotifywait.c
        src/inotifywatch.c)
