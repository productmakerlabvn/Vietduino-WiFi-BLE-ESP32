# Mạch Vietduino Wifi BLE ESP32 (Arduino Compatible)

![](/image/vietesp_01.jpg)

## Giới thiệu

Mạch Vietduino Wifi BLE ESP32 (Arduino Compatible) được nghiên cứu và và sản xuất bởi MakerLab.vn dựa trên Module Wifi BLE SoC ESP32 ESP-WROOM-32E từ chính hãng Espressif với các ưu điểm vượt trội:

1. Thiết kế với hình dạng và các chân tín hiệu được sắp xếp để có độ tương đồng về chức năng cao nhất với quy chuẩn Arduino.
1. Sử dụng mạch nguồn xung giảm áp với ưu điểm là hiệu suất chuyển đổi cao, toả nhiệt thấp, tiết kiệm năng lượng, dải điện áp đầu vào cấp cho mạch rộng từ 6~24VDC với dòng đầu ra lớn: 5VDC/Max 1500mA, 3.3VDC / Max 700mA.
1. Bổ sung thêm các chân cấp nguồn POWER+ 5VDC giúp dễ dàng cấp nguồn cho nhiều thiết bị khác nhau.
1. Sử dụng IC chuyển đổi USB-UART CH340 được nhập khẩu chính hãng cho độ ổn định và độ bền cao.
1. Chức năng cách ly nguồn cổng USB tự động khi cấp nguồn ngoài từ chân Vin hoặc giắc DC giúp bảo vệ cổng USB máy tính của bạn an toàn hơn.

## Thông số kỹ thuật

<table><thead>
  <tr>
    <th>Model</th>
    <th>Mạch Vietduino Wifi BLE ESP32 (Arduino Compatible)</th>
  </tr></thead>
<tbody>
  <tr>
    <td>CPU and On­Chip Memory</td>
    <td>ESP32-D0WD-V3 embedded, Xtensa dual-core 32-bit LX6 microprocessor, up to 240 MHz<br>448 KB ROM<br>520 KB SRAM<br>16 KB SRAM in RTC</td>
  </tr>
  <tr>
    <td>Power Supply</td>
    <td>Power Input:<br>DC Plug: 6~24VDC, Current &gt; 500mA<br>USB-C: 5VDC, Current &gt; 500mA<br>Power Output:<br>5VDC: Max 1500mA<br>3.3VDC: Max 700mA</td>
  </tr>
  <tr>
    <td>Interface</td>
    <td>SD card, UART, SPI, SDIO, I2C, LED PWM, Motor PWM, I2S, IR, pulse counter, GPIO, capacitive touch sensor, ADC, DAC, Two-Wire Automotive Interface (TWAI®, compatible with ISO11898-1)</td>
  </tr>
  <tr>
    <td>Wifi</td>
    <td>802.11b/g/n<br>Bit rate: 802.11n up to 150 Mbps<br>A-MPDU and A-MSDU aggregation<br>0.4 µs guard interval support<br>Center frequency range of operating channel: 2412 ~ 2484 MHz</td>
  </tr>
  <tr>
    <td>Bluetooth</td>
    <td>Bluetooth V4.2 BR/EDR and Bluetooth LE specification<br>Class-1, class-2 and class-3 transmitter<br>AFH<br>CVSD and SBC</td>
  </tr>
  <tr>
    <td>Integrated Components on Module</td>
    <td>40 MHz crystal oscillator<br>4MB (XXN4) / 16MB (XX0H28) SPI flash</td>
  </tr>
  <tr>
    <td>Antenna</td>
    <td>PCB (WROOM-32E) / IPEX (WROOM-32UE)</td>
  </tr>
  <tr>
    <td>Button</td>
    <td>Reset</td>
  </tr>
  <tr>
    <td>Led</td>
    <td>TX / RX / IO18</td>
  </tr>
  <tr>
    <td>Programmer</td>
    <td>USB-UART CH340 Included</td>
  </tr>
  <tr>
    <td>Packet</td>
    <td>Arduino Packet</td>
  </tr>
</tbody></table>

## Kích thước

![](/image/vietesp_02.jpg)
Vietduino Wifi BLE ESP32 (Arduino Compatible)

## Hình ảnh

![](/image/vietesp_03.jpg)
Vietduino Wifi BLE ESP32 Front and Back

## Hướng dẫn sử dụng với phần mềm Arduino

### Hướng dẫn sử dụng phần mềm Arduino cơ bản

1) Giới thiệu về Arduino

2) Ngôn ngữ lập trình Arduino

3) Cách cài đặt phần mềm Arduino IDE

4) Cách cài đặt Driver và nạp chương trình cho mạch Arduino / Arduino Compatible

5) Cách cài đặt các thư viện phần cứng Arduino Library

6) Cách sử dụng Serial Monitor & Serial Plotter trên phần mềm Arduino

Hướng dẫn kết nối và nạp chương trình cho Mạch Vietduino Wifi BLE ESP32 trên phần mềm Arduino:

1) Kết nối máy tính: Kết nối Mạch Vietduino Wifi BLE ESP32 với máy tính bằng cáp USB-C sẽ thấy Led nguồn PWR trên mạch phát sáng.

![](/image/vietesp_04.jpg)
Vietduino ESP32 WROOM-32E connect with the computer
2) Cài đặt Driver: Mạch Vietduino Wifi BLE ESP32 mà một mạch Arduino Compatible (tương thích Arduino) sử dụng IC nạp chương trình và giao tiếp máy tính CH340, các bạn có thể tham khảo Hướng dẫn cài đặt Driver cho các mạch sử dụng IC giao tiếp USB-UART CH34x - MakerLab Wiki.

3) Cấu hình mạch trên phần mềm Arduino: Để cấu hình mạch trên phần mềm Arduino chúng ta cần làm các bước sau:

- Copy đường link sau và dán vào mục File > Preferences > Additional boards manager URLs (trên Windows) hoặc Arduino IDE > Settings > Additional boards manager URLs (trên MacOS) sau đó nhấn OK:

    <https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json>

![](/image/vietesp_05.png)

Add URL Vietduino ESP32 Board on Arduino  

- Tiếp theo chọn Tools > Board > Boards Manager..., tìm từ khoá ESP32 sẽ thấy mục "esp32 by Espressif Systems", nhấn Install và chờ đợi cho đến khi cài đặt hoàn tất:

![](/image/vietesp_06.png)

Install Vietduino ESP32 Board

- Sau khi cài đặt hoàn tất, tắt và khởi động lại phần mềm Arduino, sau đó thiết lập Board tại Tools > Board > esp32 > ESP32 Dev Module và Port (cổng kết nối) cho mạch, nếu không xác định được cổng kết nối có thể ngắt kết nối mạch và kết nối lại đồng thời kiểm tra phần Port để thấy cổng kết nối mới của mạch xuất hiện:

![](/image/vietesp_07.png)

Vietduino ESP32 Board and Port  

> **Các thiết lập mặc định để nạp chương trình của mạch sẽ như hình dưới đây:
thumb Lưu ý quan trọng!!!:**  
Upload Speed với hệ điều hành Windows có thể chọn 912600, với MacOS hoặc các hệ điều hành khác nếu có báo lỗi khi nạp chương trình chọn 115200.  
Flash Size nếu ký hiệu trên Module WROOM-32E là "XXN4" chọn 4MB, nếu ký hiệu là "XX0H28" chọn 16MB.

![](/image/vietesp_08.png)
Vietduino ESP32 Board Default Configuration  

- Sau khi đã hoàn thành các thiết lập cơ bản bạn có thể nạp chương trình Blink sau vào mạch để test bằng cách nhấn vào nút Upload hoặc chọn Sketch > Upload sẽ thấy Led được kết nối với chân IO18 trên mạch chớp tắt 1 giây 1 lần:

```ino
/*
  Blink
  Turns an LED_BUILTIN on IO18 of Vietduino ESP32 for one second, then off for one second, repeatedly.
*/
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN on IO18 as an output.
  pinMode(18, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(18, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(18, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}
```

![](/image/vietesp_09.png)
Upload Blink on Vietduino ESP32

## Nhà phân phối

Có thể mua Mạch Vietduino Wifi BLE ESP32 tại các nhà phân phối sau:

- [Hshop.vn - Điện tử & Robot.](hshop.vn)
