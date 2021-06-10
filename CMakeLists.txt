cmake_minimum_required(VERSION 3.19)
project(npcap_examples)

set(CMAKE_CXX_STANDARD 17)

set(NPCAP_INCLUDE ./Include)
set(NPCAP_LIB ./Lib/x64)
set(PCAP_SRC ./src/pcap)
set(REMOTE_SRC ./src/remote)

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
target_link_libraries(pcap_UDPdump Packet.lib wpcap.lib ws2_32.lib)

add_executable(remote_iflist ${REMOTE_SRC}/iflist/iflist.c)
target_link_libraries(remote_iflist Packet.lib wpcap.lib)

add_executable(remote_misc_basic_dump ${REMOTE_SRC}/misc/basic_dump.c)
target_link_libraries(remote_misc_basic_dump Packet.lib wpcap.lib)

add_executable(remote_misc_basic_dump_ex ${REMOTE_SRC}/misc/basic_dump_ex.c)
target_link_libraries(remote_misc_basic_dump_ex Packet.lib wpcap.lib)

add_executable(remote_misc_readfile ${REMOTE_SRC}/misc/readfile.c)
target_link_libraries(remote_misc_readfile Packet.lib wpcap.lib)

add_executable(remote_misc_readfile_ex ${REMOTE_SRC}/misc/readfile_ex.c)
target_link_libraries(remote_misc_readfile_ex Packet.lib wpcap.lib)

add_executable(remote_misc_savedump ${REMOTE_SRC}/misc/savedump.c)
target_link_libraries(remote_misc_savedump Packet.lib wpcap.lib)

add_executable(remote_misc_sendpack ${REMOTE_SRC}/misc/sendpack.c)
target_link_libraries(remote_misc_sendpack Packet.lib wpcap.lib)

add_executable(remote_PacketDriver_GetMacAddress ${REMOTE_SRC}/PacketDriver/GetMacAddress/GetMacAddress.c)
target_link_libraries(remote_PacketDriver_GetMacAddress Packet.lib wpcap.lib)

add_executable(remote_PacketDriver_TestPacketCapture ${REMOTE_SRC}/PacketDriver/TestPacketCapture/TestPacketCapture.c)
target_link_libraries(remote_PacketDriver_TestPacketCapture Packet.lib wpcap.lib)

add_executable(remote_PacketDriver_TestPacketSend ${REMOTE_SRC}/PacketDriver/TestPacketSend/TestPacketSend.c)
target_link_libraries(remote_PacketDriver_TestPacketSend Packet.lib wpcap.lib)

add_executable(remote_pcap_filter ${REMOTE_SRC}/pcap_filter/pcap_filter.c)
target_link_libraries(remote_pcap_filter Packet.lib wpcap.lib)

add_executable(remote_pcap_fopen ${REMOTE_SRC}/pcap_fopen/pcap_fopen.cpp)
target_link_libraries(remote_pcap_fopen Packet.lib wpcap.lib)

add_executable(remote_pktdump_ex ${REMOTE_SRC}/pktdump_ex/pktdump_ex.c)
target_link_libraries(remote_pktdump_ex Packet.lib wpcap.lib)

add_executable(remote_sendcap ${REMOTE_SRC}/sendcap/sendcap.c)
target_link_libraries(remote_sendcap Packet.lib wpcap.lib)

add_executable(remote_smp_1 ${REMOTE_SRC}/smp_1/smp_1.c)
target_link_libraries(remote_smp_1 Packet.lib wpcap.lib)

add_executable(remote_tcptop ${REMOTE_SRC}/tcptop/tcptop.c)
target_link_libraries(remote_tcptop Packet.lib wpcap.lib)

add_executable(remote_UDPdump ${REMOTE_SRC}/UDPdump/UDPdump.c)
target_link_libraries(remote_UDPdump Packet.lib wpcap.lib)

add_executable(remote_UserLevelBridge ${REMOTE_SRC}/UserLevelBridge/UserBridge.c)
target_link_libraries(remote_UserLevelBridge Packet.lib wpcap.lib)