set(INCLUDES_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../include")

add_library(epoll-shim STATIC epoll.c signalfd.c common.c ../include/sys/eventfd.h)
target_include_directories(epoll-shim PUBLIC "${INCLUDES_DIR}")
