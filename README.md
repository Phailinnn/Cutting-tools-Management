<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ระบบเบิกวัสดุ</title>
  <script src="https://cdn.rawgit.com/davidshimjs/qrcodejs/gh-pages/qrcode.min.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      margin: 0;
      padding: 0;
    }

    form {
      max-width: 400px;
      margin: 0 auto;
      background-color: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    h2 {
      text-align: center;
      margin-bottom: 20px;
    }

    label {
      display: block;
      margin-bottom: 5px;
    }

    input[type="text"],
    input[type="password"],
    select {
      width: 100%;
      padding: 10px;
      margin-bottom: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }

    button {
      width: 100%;
      padding: 10px;
      border-radius: 5px;
      border: none;
      background-color: #007bff;
      color: #fff;
      cursor: pointer;
    }

    button:hover {
      background-color: #0056b3;
    }

    #selectedItems div {
      margin-bottom: 5px;
    }

    #qrcode {
      max-width: 400px;
      margin: 20px auto;
      text-align: center;
    }
  </style>
</head>

<body>

    <!-- สร้างฟอร์มสำหรับล็อกอิน -->
    <form id="loginForm" onsubmit="login(event)">
      <h2>เข้าสู่ระบบ</h2>
      <label for="employeeID">รหัสพนักงาน:</label>
      <input type="text" id="employeeID" required>
  
      <label for="password">รหัสผ่าน:</label>
      <input type="password" id="password" required>
  
      <button type="submit">เข้าสู่ระบบ</button>
      <p id="passwordMismatch" style="color: red; display: none;">Password is incorrect</p>
      <p id="employeeIDMismatch" style="color: red; display: none;">employeeID is incorrect</p>
    </form>
    <script>
      function login(event) {
        event.preventDefault(); // ป้องกันการโหลดหน้าเว็บเมื่อกด submit
        var employeeID = document.getElementById('employeeID').value;
        var password = document.getElementById('password').value;
        if (
          employeeID === 'B6308193' && password === '000' ||
          employeeID === 'B6326999' && password === '111' ||
          employeeID === 'B6311452' && password === '222' ||
          employeeID === 'B6305116' && password === '333'
        ) {
          alert('เข้าสู่ระบบสำเร็จ');
          // เพิ่มโค้ดส่วนที่ต้องการให้ทำหลังจากล็อกอินสำเร็จ
        } else {
          alert('รหัสพนักงานหรือรหัสผ่านไม่ถูกต้อง');
        }
      }
    </script>
    
  </body>
  
  </html>
