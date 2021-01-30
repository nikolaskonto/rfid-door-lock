# rfid-door-lock
simple rfid-controlled relay
I got the code from https://arduinogetstarted.com/tutorials/arduino-rfid-nfc-relay . 
For some reason, i cannot still understand, HIGH and LOW settings in the code are totally mixed up. I want the relay not to be under current when not working, extending its life. So when the code said HIGH, I replaced it with LOW and vice-versa
  Typical pin layout used:
  -----------------------------------------------------------------------------------------
           MFRC522      Arduino       Arduino   Arduino    Arduino          Arduino
          Reader/PCD   Uno           Mega      Nano v3    Leonardo/Micro   Pro Micro
 Signal      Pin          Pin           Pin       Pin        Pin              Pin
  -----------------------------------------------------------------------------------------
 RST/Reset   RST          9             5         D9         RESET/ICSP-5     RST
 SPI SS      SDA(SS)      10            53        D10        10               10
 SPI MOSI    MOSI         11 / ICSP-4   51        D11        ICSP-4           16
 SPI MISO    MISO         12 / ICSP-1   50        D12        ICSP-1           14
 SPI SCK     SCK          13 / ICSP-3   52        D13        ICSP-3           15

RELAY IN - > A5
