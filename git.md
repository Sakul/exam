# Git

## Clone Git repository
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
