cmake_minimum_required(VERSION 3.10)
project(DeribitTradingSystem)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)

# Include directories for external libraries
include_directories(include)

# Add source files
set(SOURCES
    src/main.cpp
    src/api_client.cpp
    src/order_manager.cpp
    src/websocket_server.cpp
    src/utils.cpp
)

# Add executable
add_executable(DeribitTradingSystem ${SOURCES})

# Link libraries
find_package(CURL REQUIRED)
target_link_libraries(DeribitTradingSystem CURL::libcurl)
