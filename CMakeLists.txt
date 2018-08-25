cmake_minimum_required(VERSION 3.12)
project(CWXSample)

set(CMAKE_CXX_STANDARD 14)

# Created with wxWidgets-3.1.1 using ../configure --enable-debug --with-macosx-version-min=10.10
# Remember to set the environment variable WX_SDK_DIR
message("Building " ${CMAKE_BUILD_TYPE} " version")
set(wxWidgets_CONFIG_EXECUTABLE "$ENV{WX_SDK_DIR}/build-cocoa-debug-latest/wx-config")

find_package(wxWidgets COMPONENTS core base REQUIRED)
include(${wxWidgets_USE_FILE})


add_executable(CWXSample main.cpp)
target_link_libraries(${PROJECT_NAME} ${wxWidgets_LIBRARIES})