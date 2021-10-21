การติดตั้ง m5stack
เครื่อง Mac จะมีขั้นตอนการติดตั้งที่ต่างจาก window อย่างมากส่วนใหญ่ของการทำงานจะติดตั้งจาก Terminal application
1.ติดตั้ง driver 
-download จาก www.M5stack.com =>download=>จะได้ driver ชื่อ SiLabsUSBDriverDisk.dmg ให้ทำการติดตั้งจนเสร็จ
2. unlock the software driver developer 
-System Preference=>Security & Privacy=>General=>unlock key เป็นการติดตั้ง driver อย่างปลอดภัยที่สุด
3.ติดตั้ง Ardunio IDE 
4.Terminal Application
-คัดลอกคำสั่งไปวางที่ Terminal
mkdir -p ~/Documents/Arduino/hardware/espressif && \
cd ~/Documents/Arduino/hardware/espressif && \
git clone https://github.com/espressif/arduino-esp32.git esp32 && \
cd esp32 && \
git submodule update --init --recursive && \
cd tools && \
python get.py
กด enter
โปรแกรมจะทำการ download และติดตั้ง component ที่จำเป็น เมื่อติดตั้งเสร็จจะปรากฏคำว่า Done เป็นการติดตั้ง libraries อย่างสมบูรณ์
5.เริ่มใช้งาน  Sketch 
-เปิดโปรแกรม Arduino ide =>ป้อนโค้ด

#include <m5stack.h>

void setup() {
M5.begin();
M5.Lcd.print ("HELLO, MacOS");
}

void loop() {

}

6.ตั้งค่า Board 
-Tools=>Board :" M5stack-core-esp32 "
