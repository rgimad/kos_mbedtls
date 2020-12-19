- to prevent compilation error i commented out line 46 in library/timing.c
    i think mbedtls_timing_hardclock will work in kolibri
    bit if not so TODO is to rewrite timing.c such way that ll work in kolibri

- to prevent compilation error i uncommented line #define MBEDTLS_NO_PLATFORM_ENTROPY in include/mbedtls/config.h
    i think it will work, cause it seems like mbedtls can work even without platform specific entropy sources.
    
- to prevent compilation error i commented out #define MBEDTLS_NET_C in include/mbedtls/config.h
    TODO rewrite library/net_sockets.c so that it would work in kolibri & uncomment #define MBEDTLS_NET_C in config.h