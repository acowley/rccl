enable_testing()
include_directories(${GOOGLETEST_DIR}/include ${GOOGLETEST_DIR} ${CMAKE_SOURCE_DIR}/inc)

add_executable(rcclUniqueId rcclUniqueId.cpp)
target_link_libraries(rcclUniqueId PUBLIC hip::hip_hcc ${hcc_LIBRARIES} rccl gtest gtest_main)
add_test(rcclUniqueId rcclUniqueId)

add_executable(rcclCommInitRank rcclCommInitRank.cpp)
target_link_libraries(rcclCommInitRank PUBLIC hip::hip_hcc ${hcc_LIBRARIES} rccl gtest gtest_main)
add_test(rcclCommInitRank rcclCommInitRank)
