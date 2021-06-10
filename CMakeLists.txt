cmake_minimum_required(VERSION 3.19)
project(npcap_examples)

set(CMAKE_CXX_STANDARD 17)

set(NPCAP_INCLUDE ./Include)
set(NPCAP_LIB ./Lib/x64)
set(PCAP_SRC ./src/pcap)

include_directories(${NPCAP_INCLUDE})
link_directories(${NPCAP_LIB})

add_executable(npcap_examples main.cpp)
target_link_libraries(npcap_examples Packet.lib wpcap.lib)

add_executable(pcap_basic_dump ${PCAP_SRC}/basic_dump/basic_dump.c)
target_link_libraries(pcap_basic_dump Packet.lib wpcap.lib)

add_executable(pcap_basic_dump_ex ${PCAP_SRC}/basic_dump_ex/basic_dump_ex.c)
target_link_libraries(pcap_basic_dump_ex Packet.lib wpcap.lib)

add_executable(pcap_iflist ${PCAP_SRC}/iflist/iflist.c)
target_link_libraries(pcap_iflist Packet.lib wpcap.lib)

add_executable(pcap_pcap_filter ${PCAP_SRC}/pcap_filter/pcap_filter.c)
target_link_libraries(pcap_pcap_filter Packet.lib wpcap.lib)

add_executable(pcap_pktdump_ex ${PCAP_SRC}/pktdump_ex/pktdump_ex.c)
target_link_libraries(pcap_pktdump_ex Packet.lib wpcap.lib)

add_executable(pcap_readfile ${PCAP_SRC}/readfile/readfile.c)
target_link_libraries(pcap_readfile Packet.lib wpcap.lib)

add_executable(pcap_readfile_ex ${PCAP_SRC}/readfile_ex/readfile_ex.c)
target_link_libraries(pcap_readfile_ex Packet.lib wpcap.lib)

add_executable(pcap_savedump ${PCAP_SRC}/savedump/savedump.c)
target_link_libraries(pcap_savedump Packet.lib wpcap.lib)

add_executable(pcap_sendpack ${PCAP_SRC}/sendpack/sendpack.c)
target_link_libraries(pcap_basic_dump_ex Packet.lib wpcap.lib)

add_executable(pcap_UDPdump ${PCAP_SRC}/UDPdump/UDPdump.c)
target_link_libraries(pcap_UDPdump Packet.lib wpcap.lib)