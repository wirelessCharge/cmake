# cmake

## 외부 라이브러리 참조

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
