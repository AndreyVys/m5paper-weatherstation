## Reference
This M5Paper weather station is refered from M5Paper Dashboard by estshorter at his Github:
https://github.com/estshorter/m5paper-dashboard
## Description
![Explain Display](https://user-images.githubusercontent.com/34854662/108235713-aef15d80-7178-11eb-85f6-2d1df97b6e43.png)

## How to use
Change your Wi-Fi parameters in `src/WiFiInfo.h`
constexpr auto SSID = "wifi"; //your SSID
constexpr auto PASS = "12345678"; // your password


Change parameters in `src\main.cpp`

#define timezone  3 //your timezone

see https://openweathermap.org

String LocationCity = "Moscow"; // your city 
String LocationCountry = "RU"; // your country 
String API_Key  = "";
String Language = "ru";
.....

change ntp servers and timezone

constexpr auto NTP_SERVER1 = "0.ru.pool.ntp.org";
constexpr auto NTP_SERVER2 = "1.ru.pool.ntp.org";
constexpr auto NTP_SERVER3 = "2.ru.pool.ntp.org";
constexpr auto TIME_ZONE = "MSK-3";

change description on display

gfx.printf("Москва,Россия\r\n");

Weather, temmperature, humidity, visibility, pressure, wind ... icons are converted to "C" codes and located at:
- `scr/WeatherIcons.c`
- `scr/THPIcons.c`
- `scr/WindIcons.c`
## Buttons
- BtnL: Shutdown
- BtnR: Refresh Weather and display information
- BtnP: Time Synchronization with a NTP server
## Project detail
- Instructables: https://www.instructables.com/M5Paper-Weather-Station/
- YouTube: https://www.youtube.com/watch?v=Mbq6BIsMcAs
