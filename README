# การใช้งาน Express.js

## 1. Express.js คืออะไร?
Express.js เป็นเฟรมเวิร์กสำหรับสร้างเว็บเซิร์ฟเวอร์บน Node.js โดยช่วยให้สามารถจัดการเส้นทาง (routing), middleware และการจัดการกับคำขอ (request) ได้สะดวกและมีประสิทธิภาพ

## 2. การกำหนดเส้นทาง (Routing)
- `app.get()`: ใช้กำหนดเส้นทางสำหรับ HTTP GET
- `app.post()`: ใช้กำหนดเส้นทางสำหรับ HTTP POST

ตัวอย่าง:
```js
app.get("/", (req, res) => {
  res.send("Welcome to Express");
});
```

## 3. การจัดการข้อมูลฟอร์ม
- ใช้ `body-parser` ในการแปลงข้อมูลที่ส่งมาจากฟอร์มให้สามารถอ่านได้จาก `req.body`

ตัวอย่าง:
```js
const bodyParser = require("body-parser");
app.use(bodyParser.urlencoded({ extended: true }));
```

## 4. การส่งข้อมูลไปยัง View (Template Engine)
- ใช้ `res.render()` เพื่อเรนเดอร์ไฟล์ `.ejs` พร้อมส่งข้อมูลไปยังเทมเพลต

ตัวอย่าง:
```js
res.render("index.ejs", { numberOfLetters: 10 });
```

## 5. การคำนวณข้อมูลจากฟอร์ม
- รับข้อมูลจากฟอร์ม (เช่น `fName` และ `lName`) แล้วคำนวณจำนวนตัวอักษรรวม จากนั้นส่งผลลัพธ์ไปยังหน้าเว็บ

ตัวอย่าง:
```js
app.post("/", (req, res) => {
  const fName = req.body.fName;
  const lName = req.body.lName;
  const numberOfLetters = fName.length + lName.length;
  res.render("index.ejs", { numberOfLetters });
});
```

## 6. การตั้งค่าเซิร์ฟเวอร์
- ใช้ `app.listen()` เพื่อเริ่มต้นเซิร์ฟเวอร์ โดยสามารถระบุพอร์ตที่ต้องการให้เซิร์ฟเวอร์รัน

ตัวอย่าง:
```js
app.listen(3000, () => {
  console.log("Server is running on port 3000");
});
```
