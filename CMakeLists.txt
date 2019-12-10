project(aes_Gladman)



set(aes_Gladman_SRCS
    ${AES_GLADMAN_ROOT}/aes_modes.c
    ${AES_GLADMAN_ROOT}/aescrypt.c
    ${AES_GLADMAN_ROOT}/aeskey.c
    ${AES_GLADMAN_ROOT}/aestab.c
)

if(WIN32)
    list(APPEND aes_Gladman_SRCS ${AES_GLADMAN_ROOT}/aes_ni.c)
endif()

# set lib
add_library(aes_Gladman
    ${aes_Gladman_SRCS}
)

# set_target_properties(aes_Gladman PROPERTIES POSITION_INDEPENDENT_CODE ON)

set(INS_TARGETS
    aes_Gladman
)

# Install
install(TARGETS ${INS_TARGETS}
    RUNTIME DESTINATION bin COMPONENT applications
    LIBRARY DESTINATION lib COMPONENT libraries
    ARCHIVE DESTINATION lib COMPONENT libraries
)
