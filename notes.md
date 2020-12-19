####Notes
- to prevent compilation error i commented out line 46 and "alarm( seconds );" line in library/timing.c\
    i think mbedtls_timing_hardclock will work in kolibri\
    but if not so TODO is to rewrite timing.c such way that ll work in kolibri

- to prevent compilation error i uncommented line #define MBEDTLS_NO_PLATFORM_ENTROPY in include/mbedtls/config.h\
    i think it will work, cause it seems like mbedtls can work even without platform specific entropy sources.
    upd: seems not )) it doesnt work and gives error CTR_DRBG - The entropy source failed ..

- to prevent compilation error i commented out #define MBEDTLS_FS_IO in include/mbedtls/config.h

- following functions deleted because they are NOT neccesary for programs/ssl_client1.c
    - mbedtls_net_bind
    - mbedtls_net_accept
    - mbedtls_net_poll
    - mbedtls_net_set_block
    - mbedtls_net_set_nonblock
    - mbedtls_net_usleep
    - mbedtls_net_recv_timeout


####Other:\

- Order in which you list libs in ldflags matter !