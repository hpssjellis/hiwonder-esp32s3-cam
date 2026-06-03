# hiwonder-esp32s3-cam
hiwonder-esp32s3-cam-ai-camera and carrier-board v1.0

# ESP32 S3-Cam AI Vision Module 
ESP32-S3 Chip WiFi Real-Time Image Transmission for IoT, AI and Robot Development

https://www.hiwonder.com/products/esp32-cam-ai-vision-module


<img width="682" height="745" alt="esp32s3cam" src="https://github.com/user-attachments/assets/6a8a2783-c68a-4b71-90db-3a1ff7255dfd" />



HiWonder docs

https://docs.hiwonder.com/projects/ESP32-S3/en/latest/index.html


## WiFi Camera
To run the standard example esp32 wifi camera  you need to change

1. esp32 boards  esp32s3 Dev Module
2. example esp32 camera- wifiwebcamera
3. in ```boards_config.h``` activate CAMERA_MODEL_ESP32S3_EYE by uncommenting, make sure the default is commented out
    ``` #define CAMERA_MODEL_ESP32S3_EYE // Has PSRAM```
4. In the main ino switch these lines so JPEG is off and RGB565 is on.

```
    //config.pixel_format = PIXFORMAT_JPEG;  // for streaming
    config.pixel_format = PIXFORMAT_RGB565; // for face detection/recognition
```
This code runs fine. I am a bit worrie dthat JPEG is not a default.





## Camera pins
If you need to know the pins here they are

```
//#if defined(CAMERA_MODEL_ESP32S3_EYE)
#define PWDN_GPIO_NUM  -1
#define RESET_GPIO_NUM -1
#define XCLK_GPIO_NUM  15
#define SIOD_GPIO_NUM  4
#define SIOC_GPIO_NUM  5

#define Y2_GPIO_NUM 11
#define Y3_GPIO_NUM 9
#define Y4_GPIO_NUM 8
#define Y5_GPIO_NUM 10
#define Y6_GPIO_NUM 12
#define Y7_GPIO_NUM 18
#define Y8_GPIO_NUM 17
#define Y9_GPIO_NUM 16

#define VSYNC_GPIO_NUM 6
#define HREF_GPIO_NUM  7
#define PCLK_GPIO_NUM  13

```
