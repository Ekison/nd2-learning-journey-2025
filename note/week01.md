# week01

## ND2025 Course Materials
https://drsanti.github.io/kmutt-non-degree-2025/

## Figma to flutter
- 01: https://youtu.be/bDqXbptippg
- วิดีโอนี้เป็นการสอนพื้นฐานการเปลี่ยนงานออกแบบจาก Figma ไปเป็นโค้ด Flutter (Figma-to-Flutter) โดยเน้นการสร้าง UI หน้า Sign up และ Sign in อย่างง่ายครับ
สรุปเนื้อหาสำคัญจากวิดีโอ:

    แนวคิดในการออกแบบ [00:41]: ผู้สอนเน้นการสร้าง UI ที่มีความซับซ้อนกว่าปกติเล็กน้อยเพื่อฝึกการเขียนโค้ด เช่น การใช้ Gradient (การไล่เฉดสี) ในช่อง Input Box และปุ่มกด แทนที่จะใช้สีพื้นธรรมดา เพื่อให้เห็นวิธีการจัดการใน Flutter

    การตั้งค่าเฟรมใน Figma [02:07]: เริ่มต้นสร้างเฟรมโดยเลือกขนาดของ iPhone 14/15 Pro และออกแบบในลักษณะ Dark Mode (พื้นหลังสีดำ) [02:29]

    การสร้างหน้า Sign up [02:52]: ประกอบด้วยส่วนประกอบหลัก: โลโก้ (สมมติ), ช่องกรอก Email, Username, Password, และ Confirm Password (Password Again) [04:59]

    ใช้ฟีเจอร์ Auto Layout ใน Figma เพื่อช่วยจัดการระยะห่างและการจัดวางองค์ประกอบให้อยู่กึ่งกลาง [03:43]
    การสร้างหน้า Sign in [07:28]: คัดลอกโครงสร้างจากหน้า Sign up มาปรับลดช่องกรอกข้อมูลให้เหลือเพียง Email และ Password [08:13]

    เทคนิคการออกแบบเพื่อการเขียนโปรแกรม (Responsive Design) [05:46]:

    การกำหนดค่า Fill Container เพื่อให้ UI ปรับขนาดตามความกว้างของหน้าจออุปกรณ์ที่เปลี่ยนไปได้โดยอัตโนมัติ [06:03]

    การตั้งค่า Margin และ Padding เช่น กำหนดระยะห่างจากขอบจอ 32 หน่วย และระยะห่างระหว่างคอมโพเนนต์ 28 หน่วย [06:48]
    เน้นย้ำเรื่องการออกแบบให้เป็น Relative (สัมพันธ์กัน) แทนการใช้ค่า Absolute เพื่อให้โปรแกรมฉลาดพอที่จะจัด Layout เองบนอุปกรณ์ที่หลากหลาย [09:39]

    เป้าหมายถัดไป [10:19]: การนำงานออกแบบทั้ง 2 หน้านี้ไปสร้างเป็น Component และฟีเจอร์จริงในโปรเจกต์ Flutter เพื่อให้สามารถรันบน Simulator ได้ [10:43]
  
- 02: https://youtu.be/X-vU_YXlrAQ
วิดีโอนี้เป็นการสอนขั้นตอนการเขียนโค้ด Flutter เพื่อเปลี่ยนงานออกแบบจาก Figma ให้กลายเป็นแอปพลิเคชันจริง โดยเน้นที่การสร้างหน้า Sign in และการทำ Custom UI ครับ
สรุปเนื้อหาสำคัญจากวิดีโอ:

    แนวคิดการเขียนโค้ด [01:00]:ผู้สอนแนะนำให้มองผลลัพธ์ให้เสร็จก่อนเริ่มเขียน (Object-Oriented Thinking) โดยแยกแยะองค์ประกอบ เช่น Background, Body, และ Widget ต่างๆ
    เน้นการเขียนโค้ดจากไฟล์ว่าง (ไม่ใช้ Template) เพื่อฝึกทักษะและความจำ [09:09]

    การตั้งค่าโครงสร้างพื้นฐาน [04:14]: เริ่มต้นสร้างฟังก์ชัน main และเรียกใช้ MaterialApp พร้อมตั้งค่าหน้าแรกเป็น Sign in form
     ใช้ Scaffold และ SafeArea เพื่อจัดวางองค์ประกอบให้อยู่ในพื้นที่ที่เหมาะสมของหน้าจอ [08:11]

    การจัดการ Theme และ Background [10:05]:
    ปรับแต่ง ThemeData ให้เป็น Dark Mode โดยจัดการผ่านส่วนกลางของแอป (Global Theme) เพื่อให้ง่ายต่อการแก้ไขในอนาคต [11:05]
    การปรับสีพื้นหลัง (Scaffold Background Color) ให้ใกล้เคียงกับใน Figma [12:46]

    การสร้าง Custom Input Field (Gradient Border) [16:42]:
    เนื่องจาก TextField มาตรฐานของ Flutter ไม่รองรับขอบสี Gradient จึงต้องสร้าง Widget ขึ้นมาใหม่เอง
      ใช้ Container เป็นตัวหุ้ม (Wrapper) และใส่ BoxDecoration เพื่อสร้าง Linear Gradient ที่ขอบ [20:25]
    ใช้ TextFormField ไว้ข้างใน และปรับแต่ง InputDecoration โดยการเอาเส้นขอบเดิมออก (Border: none) [28:45]
    เพิ่มความยืดหยุ่นโดยการรับค่า hintText ผ่าน Constructor เพื่อให้นำไปใช้ซ้ำได้ทั้งหน้า Email และ Password [30:52]

    การจัด Layout และระยะห่าง [31:53]:
    ใช้ SizedBox เพื่อกำหนดระยะห่าง (Gap) ระหว่างองค์ประกอบต่างๆ ตามที่วัดค่าได้จาก Figma (เช่น 28 หน่วย)
    ใช้ Padding แบบ Symmetric เพื่อจัดระยะห่างด้านซ้ายและขวาของฟอร์มให้สมดุล [33:31]

    การบ้านและขั้นตอนถัดไป [35:19]:
    ผู้สอนมอบหมายให้ลองสร้างหน้า Sign up เองโดยการใช้ Widget ที่สร้างไว้ซ้ำ และลองทำปุ่มกด (Button)
    ในวิดีโอถัดไปจะสอนการปรับโค้ดให้เป็นมืออาชีพมากขึ้น (Code Optimization) และการแยกไฟล์ Configuration [35:35]
  
- 03: https://youtu.be/ISmsXjHDe1Q
    วิดีโอนี้เป็นตอนต่อจากการสอน Figma-to-Flutter โดยเน้นไปที่การเฉลยการบ้านและอธิบายระบบ Form Validation และการทำ Responsive UI ครับ
สรุปเนื้อหาสำคัญจากวิดีโอ:

    การทำ Form Validation [04:14]:

        Email Validation: ใช้ Regular Expression (Regex) เพื่อตรวจสอบรูปแบบอีเมลที่ถูกต้อง [05:18]

        Username & Password: ตรวจสอบความยาวขั้นต่ำ (เช่น Username 3 ตัว, Password 5 ตัว) [06:23]

        Password Matching: ในหน้า Sign up มีการตรวจสอบว่ารหัสผ่านทั้งสองช่องต้องตรงกัน [13:29]

        Inactive Button: ปุ่ม Sign up จะไม่ทำงาน (Inactive) จนกว่าข้อมูลทุกช่องจะถูกต้องตามเงื่อนไข [07:43]

    การปรับแต่ง Custom UI ขั้นสูง [18:19]:

        Prefix Icon: การใส่ไอคอนไว้ด้านหน้าช่อง Input เช่น รูปคน (Username), ซองจดหมาย (Email) [31:41]

        Password Visibility: เพิ่มปุ่ม "ลูกตา" เพื่อเปิด-ปิดการมองเห็นรหัสผ่าน โดยใช้ onPressed เพื่อสลับค่า (Toggle) และสั่ง setState เพื่อ Rebuild UI [34:09]

        Error Display: หากข้อมูลไม่ถูกต้อง ขอบช่อง Input จะเปลี่ยนเป็นสีแดง และมีข้อความ Error สีแดงแจ้งเตือนด้านล่าง [26:03]

    การทำ Responsive UI (หน้าจอที่ยืดหยุ่น) [10:54]:

        Dynamic Font Size: คำนวณขนาดตัวอักษรตามความกว้างของหน้าจอ (Screen Width) เพื่อให้แอปดูดีในทุกอุปกรณ์ ทั้ง Mobile, Web และ Desktop [23:04]

        Constraint: การจำกัดความกว้างสูงสุด (Max Width) เพื่อไม่ให้องค์ประกอบในหน้าเว็บดูใหญ่จนเกินไป [11:49]

        Scrolling: ใช้ SingleChildScrollView เพื่อให้ผู้ใช้สามารถเลื่อนหน้าจอขึ้นลงได้เมื่อข้อมูลล้นจอ [12:04]

    เทคนิคการเขียนโค้ด (Best Practices) [19:09]:

        Reusable Widget: นำ CustomInputField มาใช้ซ้ำเพื่อลดความซ้ำซ้อนของโค้ด [15:05]

        Final Property: ใช้ final สำหรับตัวแปรที่ไม่มีการเปลี่ยนแปลงค่า เพื่อประสิทธิภาพที่ดีขึ้น [20:15]

        Static Class for Theme: เก็บค่าสีและสไตล์ต่างๆ ไว้ใน Class กลาง เพื่อให้ง่ายต่อการแก้ไขตามความต้องการของ Designer [29:01]

    การนำทาง (Navigation) [15:25]:

        สอนการใช้ Navigator เบื้องต้นเพื่อสลับหน้าไปมาระหว่างหน้า Sign in และ Sign up ผ่านลิงก์ด้านล่างฟอร์ม [15:44]

วิดีโอนี้ช่วยให้เห็นภาพการเปลี่ยนจาก UI สวยๆ ใน Figma มาเป็นโค้ด Flutter ที่ใช้งานได้จริง พร้อมระบบตรวจสอบข้อมูลที่ยืดหยุ่นครับ

## Practical TailwindCSS w. Next.js 14
https://www.youtube.com/watch?v=jJ6YZ_GquOY

วิดีโอนี้เป็นการสอนเขียนโปรแกรมเพื่อสร้างหน้า Login UI โดยใช้ Next.js 14 ร่วมกับ Tailwind CSS โดยอ้างอิงการออกแบบจากโปรแกรม Figma ครับ
สรุปขั้นตอนสำคัญในการสร้างหน้า Login:

    การตั้งค่าเริ่มต้น [01:49]:

        สร้างเพจใหม่โดยเพิ่มโฟลเดอร์ login และไฟล์ page.jsx ในโครงสร้างของ Next.js

        สร้างไฟล์สไตล์แยกเพื่อจัดการ CSS ที่อาจมีการใช้งานซ้ำ

    การสร้างโครงสร้างพื้นฐาน (Layout) [04:29]:

        ใช้ div เป็น Container หลัก กำหนดพื้นหลังเป็นสีม่วงโดยใช้คลาส bg-[#36...] และตั้งค่าความสูงเต็มจอด้วย h-screen [08:14]

        จัดตำแหน่งกล่อง Login ให้อยู่กึ่งกลางหน้าจอด้วย Flexbox (flex, justify-center, items-center) [11:14]

    การออกแบบกล่อง Login (Card) [10:27]:

        สร้างกล่องสีขาว (bg-white) กำหนดมุมให้มีความมน (rounded-md) และเพิ่มเงาเพื่อให้ดูมีมิติ (shadow-md) [12:29]

        เพิ่มระยะห่างภายในกล่องด้วย Padding (p-4 หรือ p-8) [12:59]

    ส่วนประกอบภายในหน้า Login:

        หัวข้อ (Header): ใช้ h1 เขียนคำว่า "Login" ปรับฟอนต์ให้หนาและใหญ่ พร้อมใส่ไอคอนจาก FontAwesome [22:21]

        ช่องกรอกข้อมูล (Input Fields): สร้างช่อง Username และ Password โดยใช้คลาส Tailwind จัดการเส้นขอบ (border-2), ความมน, และระยะ Padding ด้านใน [15:58]

        Remember Me & Forgot Password: จัดการให้อยู่ในแถวเดียวกันโดยใช้ flex และ justify-between เพื่อดันให้ข้อมูลแยกไปอยู่ซ้ายและขวา [27:58]

        ปุ่ม Login: สร้างปุ่มสีม่วงเต็มความกว้าง (w-full) พร้อมใส่เอฟเฟกต์ Hover (เปลี่ยนสีเมื่อนำเมาส์ไปวาง) และ Active (เปลี่ยนสีเมื่อคลิก) [31:20]

    เทคนิคเพิ่มเติม:

        การใช้ htmlFor: เชื่อมต่อ Label กับ Input เพื่อให้สามารถคลิกที่ข้อความแล้ว Cursor ไปปรากฏในช่องกรอกได้ทันที [18:04]

        การจัดการโค้ดให้สะอาด: แนะนำการใช้ @apply ในไฟล์ CSS เพื่อรวมกลุ่มคลาส Tailwind ที่ใช้งานซ้ำๆ (เช่น สไตล์ของช่อง Input) ช่วยให้โค้ดในหน้า JSX อ่านง่ายขึ้น [48:33]

วิดีโอนี้เน้นที่การนำทฤษฎีมาประยุกต์ใช้จริง (Practical) เพื่อให้เห็นภาพการเปลี่ยนจากงานออกแบบ (UI Design) มาเป็นโค้ดที่ใช้งานได้จริงครับ [50:34]

## การติดตั้ง docker และ N8N
- 01 การติดตั้ง Docker Desktop
  - 01 Installation & Testing the Docker Desktop   
    - download โปรแกรม docker desktop จาก website www.docker.com แล้ว save ไฟล์ลงเครื่อง
    - ติดตั้ง docker โดยเลือก option Use WSL2 instead of Hyper-V(recommend)ด้วย แล้วเลือก add shortcut ถ้าต้องการ
    - ทดสอบการใช้งานโดยเปิด cmd ขึ้นมา แล้วพิมพ์คำสั่ง  docker -v ถ้ามี version ของ docker ขึ้นมาก็แสดงว่าสามารถใช้งานโปรแกรมได้
    - เข้าโปรแกรม docker desktop ถ้าโปรแกรมเปิดขึ้นมา ก็แสดงว่าติดตั้งถูกต้อง
    - ไปที่แถบ Docker hub แล้วทดลอง download hello-world มา โดยกดปุ่ม pull images
    - เปิด cmd พิมพ์คำสั่ง docker run hello-world ว่า run ได้หรือไม่
    - ดูคำสั่งทดสอบอื่นๆใน images hello-world ที่หน้า docker hub
  
- 02 การติดตั้ง n8n บน Docker
    - 02 Get Started with n8n in Docker  
        - เข้าดู n8n.io เพื่อดูข้อมูลเกี่ยวกับ n8n
        - เข้า docker desktop ไปที่แถบ docker hub ค้นหา n8n
        - open cmd and type command --> docker volume create n8n_data : this command in create volume and store any data of n8n data
        - type command to terminal 
        	for linux or mac
        	docker run -it --rm \
         	--name n8n \
         	-p 5678:5678 \
         	-v n8n_data:/home/node/.n8n \
         	docker.n8n.io/n8nio/n8n
        
        	in windows : delete \ and make it to single command line: 
        	docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n

        - open n8n by copy url to browser and config n8n ( default port is 5678)
        - next run container by use commend : docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n 
  
- 03 สร้างความคุ้นเคยกับ n8n
  - 03 n8n Working Environment
        - open docker desktop
        - run docker by using cmd : docker run -d --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
        - open n8n in browser and sign in with previous username and password
        - create new workflow at top right side
        - overview n8n page

![plot](./pic/n8n-workflow-example.PNG)

- 04 ลองใช้งาน Google Services

## คำสั่ง docker ที่สำคัญ
- docker volume create n8n_data
- docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n
- docker.n8n.io/n8nio/n8n
