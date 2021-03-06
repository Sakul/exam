# Git

## [สร้าง Git repository](https://github.com/new)
![img](images/git03.PNG)  

## การ logout git ที่อยู่ในเครื่อง
Windows 10 กดปุ่ม Windows แล้วพิมพ์ credential manager *(พิมพ์แค่บางส่วนก็พอ)*  
![img](images/git01.png)  
![img](images/git02.png)  

## Git ignore
กรณียังไม่มีไฟล์ **.gitignore** ให้ใช้คำสั่งด้านล่าง (ถ้ามีแล้วไป copy code ด้านล่าง)
```
copy NUL .gitignore
```
> Copy code จาก [ลิงค์นี้](https://raw.githubusercontent.com/Sakul/exam/master/.gitignore) ไปใส่ในไฟล์ **.gitignore**


## [ตั้งค่าต่างๆ](https://help.github.com/categories/setup)
```
git config user.name "ENTER_YOUR_NAME_HERE"
git config user.email "ENTER_YOUR_EMAIL_HERE"
```
> ถ้าต้องการให้เป็น global ให้ต่อด้วย *--global*  
> ตัวอย่าง: git config --global user.name "sakul"

## Clone Git repository
![img](images/git04.PNG)  
```
git clone ENTER_YOUR_GIT_URL_HERE
```

## เมื่อต้องการ Commit
1.ดูสถานะว่ามีไฟล์อะไรเปลี่ยนบ้าง
```
git status
```
2.1.เพิ่มทุกไฟล์ที่เปลี่ยนลงใน staging area
```
git add .
```
2.2.เพิ่มเฉพาะไฟล์ที่เลือกลงใน staging area
```
git add ENTER_YOUR_FILE_PATH_HERE
```
3.Commit งานเข้าสู่ Repo
```
git commit -am "ENTER_YOUR_MESSAGE_HERE" (add & commit) 
```

## ดูประวัติการ commit
```
git log --oneline --graph 
```

## เมื่อต้องการจะเอางานขึ้น Git repo
1.อัพเดทงานในเครื่องตัวเอง
```
git pull --rebase
```
2.ส่งงานจากเครื่องไปยัง Git repo
```
git push
```

## เมื่อต้องการทำงานกับ branch
สร้าง branch ใหม่ พร้อมกับย้ายไปที่ branch นั้นๆ
```
git checkout -b ENTER_YOUR_NEW_BRANCH_HERE
```
ย้ายไปยัง branch ที่กำหนด
```
git checkout ENTER_BRANCH_NAME_HERE
```
ต้องการดึงไฟล์ที่เลือกจาก branch ที่กำหนด
```
git checkout ENTER_BRANCH_NAME_HERE -- ENTER_FILE_PATH_HERE
```
ต้องการดึงไฟล์ต่างๆจากที่กำหนด
```
git checkout --theirs/ours -- "file*.*"
```
ทำการรวม branch (ต้อง checkout ไปที่ branch หลักก่อน แล้วค่อย merge branch ที่จะรวมเข้ามา)
```
git merge --no-ff ENTER_BRANCH_NAME_HERE (don't forget to checkout to your base branch before do it) 
```
 

## อื่นๆ
กำหนดให้ directory นั้นๆเป็น repo
```
git init
```
ทำงานกับ branch (ปรกติเราจะไม่ค่อยได้ใช้แล้ว)
```
git branch 
```
