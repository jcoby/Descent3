set(HEADERS Entropy.h Entropystr.h EntropyAux.h)
set(CPPS EntropyBase.cpp EntropyPackets.cpp EntropyRoom.cpp)

set(NETGAME_MODULE entropy)

add_library(${NETGAME_MODULE} SHARED ${CPPS} ${HEADERS})
set_target_properties(${NETGAME_MODULE} PROPERTIES PREFIX "")
set_target_properties(${NETGAME_MODULE} PROPERTIES SUFFIX ".d3m")

target_link_libraries(${NETGAME_MODULE} dmfc)
