##### Notes
- to prevent compilation error i commented out line 46 and "alarm( seconds );" line in library/timing.c\
    i think mbedtls_timing_hardclock will work in kolibri\
    but if not so TODO is to rewrite timing.c such way that ll work in kolibri

- in include/mbedtls/config.h
    - uncommented:\
              MBEDTLS_TEST_NULL_ENTROPY\
              MBEDTLS_NO_DEFAULT_ENTROPY_SOURCES\
              MBEDTLS_NO_PLATFORM_ENTROPY
    - commented out:\
              MBEDTLS_FS_IO

- following functions deleted because they are NOT neccesary for programs/ssl_client1.c
    - mbedtls_net_bind
    - mbedtls_net_accept
    - mbedtls_net_poll
    - mbedtls_net_set_block
    - mbedtls_net_set_nonblock
    - mbedtls_net_usleep
    - mbedtls_net_recv_timeout


##### Other:
- Order in which you list libs in ldflags matter !
