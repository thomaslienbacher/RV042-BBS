cmake_minimum_required(VERSION 3.25)
project(RouterBBSCMake C)

set(CMAKE_C_STANDARD 11)

set(CMAKE_C_COMPILER /home/thomas/Projects/Router_RV042/armeb-linux-musleabi-cross/bin/armeb-linux-musleabi-gcc)

set(CMAKE_C_FLAGS "-Os -pedantic -static -march=armv4 -mbe32 -marm -mbig-endian -mabi=apcs-gnu -mfloat-abi=soft -Xassembler -meabi=5 -Wl,--verbose")

link_directories(bbs "/home/thomas/Projects/Router_RV042/musl/lib")
link_directories(bbs "/home/thomas/Projects/Router_RV042/musl")

add_executable(bbs src/mail.c src/bbs.c src/admin.c
        src/banish.c
        src/bbs.c
        src/board.c
        src/command.c
        src/command2.c
        src/dbase.c
        src/editor.c
        src/mail.c
        src/message.c
        src/resolve.c
        src/user.c)
