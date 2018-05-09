
ping to keep connection alive
-----------------------------

Test library for https://github.com/esp8266/Arduino/issues/2330

It pings the gateway every 5 seconds, and calls `ping_fault()` after 5 minutes of unsuccessful pings.

Usage
-----
* define your own `void ping_fault (void)`
* call `startPingAlive()` from `setup()` after wifi STA is connected.

Notes
-----
* WIP
* src/utility/ping.h constants may be changed
* status can be checked by reading `ping_seq_num_send` and `ping_seq_num_recv` values
* setting `ping_should_stop` to 1 will stop ping (effectively stopped when it is reset to 0)
