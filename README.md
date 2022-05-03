# cmake

### 외부 라이브러리 참조

<pre>
<code>
find_library(
    LIBSODIUM
    NAMES libtest.so
    HINTS /home/educafe/prj/src/host/ProtectionService/socket/src
    REQUIRED)

target_link_libraries(${PROJECT_NAME} ${LIBSODIUM})
</code>
</pre>

### 공유라이브러리 생성
<pre>
<code>
cmake_minimum_required(VERSION 3.16)
project(test)
set(CMAKE_BUILD_TYPE Release)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
add_library(test SHARED tcp/tcp_client.cpp tcp/tcp_server.cpp net/node.cpp net/socket_manager.cpp)
</code>
</pre>

## 공유라이브러리 포함하여 코드 빌드하기
