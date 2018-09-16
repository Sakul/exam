> ## ขั้นตอนทั้งหมด
> *(จะทำวิธีอื่นก็ได้ ผมทำตามนี้แล้วชีวิตดี๊ดี)*  
> 1. ก่อนที่จะทำข้อสอบให้สร้าง workspace เพื่อให้ได้ VM มาก่อน  
> 1. ลง **Ionic CLI, .NET Core** ให้เรียบร้อย  **(ตรวจ version ด้วย)**  
> 1. เมื่อทำที่ว่ามาทั้งหมดเสร็จอย่าพึ่งทำอะไรต่อ ให้ **Stop VM** ก่อนเพื่อให้มันทำ snapshort ไว้รอบนึง  
> 1. ไปตั้งค่า Ports และ Agents แล้ว save ซะ  
> 1. เปิดเครื่องแล้วอยากจะทำอะไรก็ทำ

> ## ข้อแนะนำ
> * ข้อความที่เป็น **สีน้ำเงิน** ในหน้า มันคลิกได้นะ *(เป็น link ไปยัง document โดยตรง)*
> * เครื่องมันดับทุก 10 นาที *(จ่ายเงินถึงจะอยู่ได้นานขึ้น)*
> * ถ้ารู้ว่าจะไม่ได้ใช้เครื่องนานๆ ให้ stop VM ไปก่อน ไม่งั้นงานจะหายหมด  
> * สร้าง Git repo แล้วทำในเครื่องเราให้เสร็จ แล้วใน VM ค่อย clone/pull มาก็ได้
> * ไม่อยากให้ VM ดับ > ให้เข้าไปกดเปิดไฟล์เล่น (ก่อนจะครบ 10 นาที)
> * อยากได้เฉลยจ่ายเงินมา ฮ่าๆ (ล้อเล่นนะผมยังไม่รู้โจทย์เลย)
---
# [Codenvy.io](https://codenvy.io/dashboard/#)
## 1.สร้าง workspace + เข้าใช้งาน  
![img](images/workspace01.PNG)  
![img](images/workspace02.PNG) 
![img](images/workspace09.PNG)

## 2.ติดตั้ง Ionic CLI และ .NET Core
### [2.1.คำสั่งติดตั้ง Ionic CLI](https://ionicframework.com/getting-started#cli) 
```
sudo npm install -g ionic
```
### [2.2.คำสั่งติดตั้ง .NET Core - Ubuntu 14.04](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-current)
```
wget -q https://packages.microsoft.com/config/ubuntu/14.04/packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install dotnet-sdk-2.1
```
> ขั้นตอนสุดท้ายมันจะถาม Y/n ให้กดปุ่ม **Enter** ได้เลย *(ส่วนตัวชอบใส่ y แล้วค่อยกดปุ่ม Enter)*

### 2.3.ตรวจสอบเวอร์ชันหลังลงเสร็จ
```
ionic --version
```
> ควรจะเป็น version 4.1.2 หรือมากกว่า

```
dotnet --version
```
> ควรจะเป็น version 2.1.402 หรือมากกว่า

![img](images/workspace10.PNG)  

### 2.4.กรณีที่ dotnet ได้เป็นตัว preview (ไม่เจอให้ข้ามขั้นตอนนี้เลย ทำบุญมาดีแล้ว)
ให้ลบ workspace นั้นๆออกเลย แล้วทำใหม่ตั้งแต่ต้น (ขั้นตอนการลบอยู่ในรูปถัดไป)
![img](images/workspace03.PNG)  
![img](images/workspace11.PNG)  


## 3.ปิดเครื่อง
![img](images/vm01.png)  

## 4.การตั้งค่า Ports และ Agents
![img](images/workspace03.PNG)  
![img](images/workspace04.PNG)  
![img](images/workspace05.PNG)  
![img](images/workspace06.PNG)  
![img](images/workspace07.PNG)  
![img](images/workspace08.PNG)  

# 5.เปิดเครื่อง
![img](images/vm02.png)  

# เปิด terminal หลายๆตัว
![img](images/terminal.png)  

# Command line (สำหรับ Linux)
เคลียหน้าจอ
```
clear
```
ออกจาก folder 1 step
```
cd ..
```
เข้าไปยัง path ที่กำหนด
```
cd PATH_TO_GO
```
ดูรายชื่อไฟล์+folder
```
dir
```
ดู process ทั้งหมด
```
ps -a
```
ทำลาย process
```
kill -9 PID
```

# การแชร์ workspace
![img](images/workspace03.PNG)  
![img](images/workspace12.PNG)  
![img](images/workspace13.PNG)  

---
# เรื่องอื่นๆ
* [Web API](web-api.md)
* [Ionic](ionic.md)
* [Git](git.md)
* TDD (กำลังทำ)
