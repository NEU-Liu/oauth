cmake_minimum_required(VERSION 3.17)
project(oauth)

set(CMAKE_CXX_STANDARD 14)

link_libraries(rt)
link_libraries(nsl)
link_libraries(resolv)
link_libraries(pthread)
link_libraries(crypto)
link_libraries(ssl)
link_libraries(event_core)
link_libraries(event_extra)
link_libraries(event_openssl)
link_libraries(event_pthreads)

add_executable(oauth oauth.c src/apputils.c src/apputils.h src/ns_turn_defs.h src/ns_turn_ioaddr.c src/ns_turn_ioaddr.h src/ns_turn_ioalib.h src/ns_turn_msg.c src/ns_turn_msg.h src/ns_turn_msg_addr.c src/ns_turn_msg_addr.h src/ns_turn_msg_defs.h src/ns_turn_msg_defs_experimental.h src/ns_turn_openssl.h src/ns_turn_utils.c src/ns_turn_utils.h src/stun_buffer.c src/stun_buffer.h)