cmake_minimum_required(VERSION 3.5)
project(RMdemo)

set(CMAKE_CXX_STANDARD 11)


include_directories(${PROJECT_SOURCE_DIR}/include)
include_directories(${PROJECT_SOURCE_DIR}/libBase/include)
include_directories(${PROJECT_SOURCE_DIR}/libHardWare/serialPort/include)
include_directories(${PROJECT_SOURCE_DIR}/libHardWare/usbCapture/include)



ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libBase)
ADD_SUBDIRECTORY(${PROJECT_SOURCE_DIR}/libHardWare)

AUX_SOURCE_DIRECTORY(${PROJECT_SOURCE_DIR}/src DIR_SRCS)
add_executable(example ${DIR_SRCS})

target_link_libraries(example Base)
target_link_libraries(example SerialPort UsbCapture)
target_link_libraries(example pthread)


find_package( OpenCV REQUIRED)
target_link_libraries(example  ${OpenCV_LIBS})














