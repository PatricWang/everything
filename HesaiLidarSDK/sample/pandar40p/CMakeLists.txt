cmake_minimum_required(VERSION 2.8)

find_package(Boost REQUIRED )
find_package(PCL REQUIRED )


set (CMAKE_CXX_STANDARD 11)

include_directories(
	${CMAKE_CURRENT_SOURCE_DIR}/../../include
	${Boost_INCLUDE_DIRS}
    ${PCL_INCLUDE_DIRS}
)


add_executable(pandar40p
	pandar40p.cc
)
target_link_libraries(pandar40p
	${CMAKE_CURRENT_SOURCE_DIR}/../../build/libhesaiLidarSDK.so
	${Boost_LIBRARIES}
	${PCL_LIBS}
)

