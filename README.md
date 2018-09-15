# [Codeny.io](https://codenvy.io/dashboard/#)
### Create new workspace  
![img](images/workspace01.PNG)  
![img](images/workspace02.PNG)  
### Setup your workspace  
![img](images/workspace03.PNG)  
![img](images/workspace04.PNG)  
![img](images/workspace05.PNG)  
![img](images/workspace06.PNG)  
![img](images/workspace07.PNG)  
![img](images/workspace08.PNG)  
### Enter your VM  
![img](images/workspace09.PNG)

# [Ionic framework](https://ionicframework.com/getting-started#cli)  
### Install Ionic CLI
```
sudo npm install -g ionic
```

# [.NET Core SDK - Ubuntu 14.04](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-current)
### Register Microsoft key and feed
```
wget -q https://packages.microsoft.com/config/ubuntu/14.04/packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```
### Install .NET SDK
```
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install dotnet-sdk-2.1
* ขั้นตอนสุดท้ายมันจะถาม Y/n ด้วย ให้กด y แล้วกด Enter
```
# ตรวจสอบเวอร์ชันที่ลงด้วย
```
ionic --version
>> 4.1.2 (ควรจะเป็น version นี้หรือมากกว่า)
```
```
dotnet --version
>> 2.1.402 (ควรจะเป็น version นี้หรือมากกว่า)
```
![img](images/workspace10.PNG)  

# กรณีที่ dotnet ได้เป็นตัว preview
* ให้ลบ workspace นั้นๆออกเลย แล้วทำใหม่ตั้งแต่ต้น
![img](images/workspace03.PNG)  
![img](images/workspace11.PNG)  

# ข้อแนะนำ
* หลังจากทำทุกอย่างเสร็จแล้วควรปิดเครื่อง
* ถ้ารู้ว่าจะไม่ได้ใช้เครื่องนานๆและต้องการจะเซฟของในเครื่องไว้ให้ปิดเครื่องด้วย

# ปิดเครื่อง
![img](images/vm01.png)  

# เปิดเครื่อง
![img](images/vm02.png)  

---
# เรื่องอื่นๆ (กำลังทำ)
* [Web API](#)
* [Ionic](#)
* [TDD](#)
* [Git](#)
