cmake_minimum_required(VERSION 3.19)
project(npcap_examples)

set(CMAKE_CXX_STANDARD 17)

set(NPCAP_INCLUDE ./Include)
set(NPCAP_LIB ./Lib/x64)

include_directories(${NPCAP_INCLUDE})
link_directories(${NPCAP_LIB})

add_executable(npcap_examples main.cpp)
target_link_libraries(npcap_examples Packet.lib wpcap.lib)