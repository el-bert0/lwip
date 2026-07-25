
FreeRTOS Posix port:

We renamed to "arch.orig" because we need to include "netif/tapif.h" but we didn't want to include "arch/cc.h" and "arch/sys_arch.h", because we want to use custom ones.

We want a custom "arch/cc.h" and a custom "arch/sys_arch.h".

Info here:

- https://www.nongnu.org/lwip/2_0_x/group__sys__layer.html
- https://lwip.fandom.com/wiki/Porting_for_an_OS

We can find FreeRTOS "arch/sys_arch.h" file in "lwip/contrib/ports/freertos/include",
while "arch/cc.h" is missing.

pico-sdk define a custom "arch/cc.h" in "pico-sdk/src/rp2_common/pico_lwip/include". Take a look!

Info here:
- https://www.raspberrypi.com/documentation/pico-sdk/high_level.html#group_pico_async_context