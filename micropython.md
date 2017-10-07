# Tutorial to read

https://docs.micropython.org/en/latest/esp8266/index.html

## Add to boot.py

## Handy commands:

### Linux

* picocom
  - exit: Ctrl-A-X

```
def do_connect():
    import network
    sta_if = network.WLAN(network.STA_IF)
    if not sta_if.isconnected():
        print('connecting to network...')
        sta_if.active(True)
        sta_if.connect('<essid>', '<password>')
        while not sta_if.isconnected():
            pass
    print('network config:', sta_if.ifconfig())
```    
