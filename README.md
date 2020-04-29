# CN210 : computer architecture

## 1st HOMEWORK : Jump format (J-format)

<br>**รูปแบบของ j-format**

| Op Code | Address |
| ------- | ------- |
|6 bits|26 bits|

* Op Code(Operation Code) : Op Code ของ J-format คือ **000010**
* Address หรือ jump target address : จะเป็นตำแหน่งที่เราจะกระโดดไปทำงานหลังจากที่เราแปลง 32 bits เป็น 26 bits <br>

**วิธีการเขียนคำสั่ง jump** <br>
แบ่งเป็น 2 ส่วนคือ Op Code และ Address โดย Op Code ของคำสั่ง jump คือ **000010** ส่วนAddressเราต้องทำการแปลงจาก 32 bits มาเป็น 26 bits เสียก่อนโดยทำดังนี้
![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-0/p480x480/94701495_2335369096763553_3772555361337212928_o.jpg?_nc_cat=104&_nc_sid=730e14&_nc_ohc=NWmD8ESa498AX-Z6-lB&_nc_ht=scontent.fbkk12-2.fna&_nc_tp=6&oh=aa35d2b4e85b2fc966ddcc303e13e192&oe=5ECBF73A)
* step 1 : แปลงจากเลขฐาน 16 เป็นเลขฐาน 2
* step 2 : ทำการตัด 2 bit สุดท้ายและ 4 bit ด้านหน้าทิ้งเนื่องจาก 2 bitสุดท้ายจะเป็น 00 เสมอและ 4 bit ด้านหน้ามีโอกาสน้อยมากที่ค่าจะเปลี่ยน ทำให้สามารถตัดทิ้งได้เพราะไม่ส่งผลอะไร <br>

เมื่อแปลงจาก 32 bits เป็น 26 bits แล้ว ให้นำ Op Code และ Address(26 bits) มารวมกันแล้วแปลงเป็นเลขฐาน 2 ดังรูป 
![image](https://scontent.fbkk8-2.fna.fbcdn.net/v/t1.0-0/p480x480/94519391_2335385786761884_110292784476323840_o.jpg?_nc_cat=107&_nc_sid=730e14&_nc_ohc=5hnIpx9pSGoAX9Ibi2y&_nc_ht=scontent.fbkk8-2.fna&_nc_tp=6&oh=d305892999f80f1747bc7dec163759ba&oe=5ECC443F) 
<br>

* [link : 1st Homework](https://www.youtube.com/watch?v=skleZIstKQc)

## 2nd HOMEWORK : การทำงานของคอมพิวเตอร์

<br>**J-Type**
<br>การทำงานของคอมพิวเตอร์คำสั่ง Jump ทำงานดังนี้
![image](https://scontent.fbkk9-2.fna.fbcdn.net/v/t1.0-9/p960x960/94644736_2335460750087721_2265015393695301632_o.jpg?_nc_cat=109&_nc_sid=730e14&_nc_ohc=9vbuAWyqfv0AX8ySHIn&_nc_ht=scontent.fbkk9-2.fna&_nc_tp=6&oh=368b8931d8a7a597a7a822b55c757a83&oe=5ECD1619)

<br>**I-Type**
<br>การทำงานของคอมพิวเตอร์คำสั่ง I-Type ทำงานดังนี้
* Load Word (lw)
![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/p960x960/95024979_2335509466749516_471561458908397568_o.jpg?_nc_cat=104&_nc_sid=730e14&_nc_ohc=DsDhUrofu1oAX_jJfOR&_nc_ht=scontent.fbkk12-2.fna&_nc_tp=6&oh=150340915e1b5155dcafdb080dbaed29&oe=5ECD7C6C)

* Store Word (sw)
![image](https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.0-9/p960x960/95063997_2335509456749517_7434998807860871168_o.jpg?_nc_cat=106&_nc_sid=730e14&_nc_ohc=k7lL8p8qw3oAX8TQHRC&_nc_ht=scontent.fbkk12-1.fna&_nc_tp=6&oh=0dfb0f52369f67fdb76e6060572cbaac&oe=5ECE8A8A)

<br>**R-Type**
<br>การทำงานของคอมพิวเตอร์คำสั่ง R-Type ทำงานดังนี้
![image](https://scontent.fbkk8-4.fna.fbcdn.net/v/t1.0-9/p960x960/94562331_2335916676708795_7406510573254344704_o.jpg?_nc_cat=100&_nc_sid=730e14&_nc_ohc=apEwrjWmyaYAX-we3MM&_nc_ht=scontent.fbkk8-4.fna&_nc_tp=6&oh=bb2a3ff7a0b9b765b57c77fcf8fcdd6b&oe=5ECDB751)

* [link : 2nd Homework](https://www.youtube.com/watch?v=7si2xAQyQ2k)

## 3rd HOMEWORK : Difference between single cycle and multi cycle

| single cycle | multi cycle |
| ------- | ------- |
|![image](https://scontent.fbkk12-4.fna.fbcdn.net/v/t1.0-9/94442656_2335545196745943_4017612434171756544_n.jpg?_nc_cat=103&_nc_sid=730e14&_nc_ohc=cijODhik3NoAX9LO1F2&_nc_ht=scontent.fbkk12-4.fna&oh=a9d2234ae2bedfc37f7592f03060a1d4&oe=5ECCD2E4)<br>ใน 1 คำสั่งสามารถจบการทำงานภายใน 1 clock|![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/94884180_2335545200079276_170332192436649984_n.jpg?_nc_cat=105&_nc_sid=730e14&_nc_ohc=9yKIl2fOGyIAX-LU3Mp&_nc_ht=scontent.fbkk12-2.fna&oh=453fd1d350e9953b8414725afa24f352&oe=5ECD0109)<br>ใน 1 คำสั่งไม่สามารถจบการทำงานได้ภายใน 1 clock(ขึ้นกับความยากง่ายของคำสั่ง)|
|![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/95258776_2335547863412343_5459161036764479488_n.jpg?_nc_cat=105&_nc_sid=730e14&_nc_ohc=ZzyqqX49_i0AX_p-Ox9&_nc_ht=scontent.fbkk12-2.fna&oh=9525dfe1c02a61a6dd3632866c3366eb&oe=5ECD1389)<br>มี memory 2 ชิ้น(Harvard architecture)|![image](https://scontent.fbkk13-1.fna.fbcdn.net/v/t1.0-9/95056024_2335547856745677_2377260902232621056_n.jpg?_nc_cat=108&_nc_sid=730e14&_nc_ohc=3dhXnWDqYXIAX_SCIaA&_nc_ht=scontent.fbkk13-1.fna&oh=18d7eed15b46e93499c6edb3ed619d6f&oe=5ECC7309)<br>มี memory 1 ชิ้น(Von Neuman architecture)|
|![image](https://scontent.fbkk12-3.fna.fbcdn.net/v/t1.0-9/95494492_2335551273412002_5143926783883608064_n.jpg?_nc_cat=102&_nc_sid=730e14&_nc_ohc=KTZYJt2fcEMAX_Vi3L4&_nc_ht=scontent.fbkk12-3.fna&oh=8eddb70a33865862dba2b2b9bc9d47ca&oe=5ECD1A2C)<br>มี ALU 3 ตัว (2 adders)|![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/94880810_2335551243412005_572084635895332864_n.jpg?_nc_cat=104&_nc_sid=730e14&_nc_ohc=MYExwdOlOYoAX-kSfVB&_nc_ht=scontent.fbkk12-2.fna&oh=66b885fbae17c4110df40874a58fc3b6&oe=5ECCBCDD)<br>มี ALU เพียงตัวเดียว|
|![image](https://scontent.fbkk8-3.fna.fbcdn.net/v/t1.0-9/94768354_2335554010078395_1954068372874330112_n.jpg?_nc_cat=111&_nc_sid=730e14&_nc_ohc=FdCUN35-wioAX9p9PsJ&_nc_ht=scontent.fbkk8-3.fna&oh=dfb1e2a067ec98bb8d79592352d87acd&oe=5ECD2D6C)<br>ไม่มี register A,B ไว้สำหรับเก็บdataชั่วคราว|![image](https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.0-9/94976779_2335554006745062_3618777841170120704_n.jpg?_nc_cat=106&_nc_sid=730e14&_nc_ohc=uBbcCRvWNXcAX_ARph6&_nc_ht=scontent.fbkk12-1.fna&oh=fbaa5329ba22dddc2e72b75514332485&oe=5ECEBCDF)<br>มี register A,B ไว้สำหรับเก็บdataชั่วคราว|
|![image](https://scontent.fbkk8-2.fna.fbcdn.net/v/t1.0-9/95159582_2335557786744684_2563854863054143488_n.jpg?_nc_cat=107&_nc_sid=730e14&_nc_ohc=Pr7PEKC4ecQAX_Nvm6F&_nc_ht=scontent.fbkk8-2.fna&oh=0120f01f1638a54b5b3e0eac2acf96ff&oe=5ECFD37E)<br>ไม่มี instruction register และ data register|![image](https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.0-9/95379513_2335557780078018_7070447704672829440_n.jpg?_nc_cat=106&_nc_sid=730e14&_nc_ohc=wh99XjMR2kYAX93w8pn&_nc_ht=scontent.fbkk12-1.fna&oh=789445debc02e73b829128acc8fafc93&oe=5ECEB37B)<br>มี instruction register และ data register|

* [link : 3rd Homework](https://www.youtube.com/watch?v=-tSL3mxhbcg)

## 4th HOMEWORK : Load Word(lw) in multi cycle

<br>**1. T1 : Instruction Fetch**
![image](https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.0-9/95146561_2335873790046417_3881369577552084992_n.jpg?_nc_cat=106&_nc_sid=730e14&_nc_ohc=bQhlIXrbGSkAX_1mBXD&_nc_ht=scontent.fbkk12-1.fna&oh=44f0742f398d5bf694b2a8f263f3d90c&oe=5ECD1FB2)
* อ่านค่า PC ชี้ไป Address ใดใน memory แล้วนำไปเก็บไว้ที่ Instruction Register
* นำ PC ไปที่ ALU เพื่อ +4 และส่งค่ากลับมาที่ PC เพื่อเก็บค่าของตำแหน่งที่จะทำงานตำแหน่งถัดไป

<br>**2. T2 : Instruction Decode and Register Fetch**
![image](https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.0-9/95092403_2335875320046264_2074752388341694464_o.jpg?_nc_cat=106&_nc_sid=730e14&_nc_ohc=3nTKYFuO8TEAX_-BWJg&_nc_ht=scontent.fbkk12-1.fna&oh=203746dfe2003bd7be461293f5b3f902&oe=5ECD3930)
* นำdataที่ $rs ไปเก็บไว้ที่ A และ นำdataที่ $rt ไปเก็บไว้ที่ B
* นำค่า offset ไป sign extend จะเปลี่ยนจาก 16 bit เป็น 32 bit และ shift ไปทางด้านซ้าย 2 ตำแหน่ง และ บวกกับค่า PC ที่ ALU และนำผลลัพธ์ที่ได้ไปเก็บไที่ ALUOut

<br>**3. T3 : Memory Address Calculation**
![image](https://pbs.twimg.com/media/EWwBeHhXgAErqu4?format=jpg&name=small)
* นำค่าที่เก็บไว้ที่ A มาบวกกับ offset แล้วเก็บผลลัพธ์ที่ได้ไว้ใน ALUout

<br>**4. T4 : Memory Access**
![image](https://pbs.twimg.com/media/EWwCmY3XkAQwPXl?format=jpg&name=small)
* นำค่าที่เก็บไว้ที่ Memory ที่ตำแหน่ง ALUOut ไปเก็บไว้ที่ Memory Data Register(MDR)

<br>**5. T5 : Write-back Step**
![image](https://pbs.twimg.com/media/EWwCiiAXsAQ4reR?format=jpg&name=small)
* นำค่าจาก Memory Data Register(MDR) ไปเก็บไว้ที่ $rt 

[link : 4th Homework](https://www.youtube.com/watch?v=WLNe0p6ohww)

## 5th HOMEWORK : Branch on Equal (Beq) on Multi Cycle

![image](https://pbs.twimg.com/media/EWwF1JIXsAUbkhh?format=jpg&name=small)
<br>**1. T1 : Instruction Fetch**
* อ่านค่า PC ชี้ไป Address ใดใน memory แล้วนำไปเก็บไว้ที่ Instruction Register
* นำ PC ไปที่ ALU เพื่อ +4 และส่งค่ากลับมาที่ PC เพื่อเก็บค่าของตำแหน่งที่จะทำงานตำแหน่งต่อไป

<br>**2. T2 : Instruction Decode & Register Fetch**
* นำข้อมูลที่ $rs ไปเก็บไว้ที่ A นำข้อมูลที่ $rt ไปเก็บไว้ที่ B

<br>**3. T3 : Branch Completion**
* นำค่าที่ A และ B มาเปรียบเทียบกัน หากเท่ากันจะส่งผลลัพธ์ไปเก็บใน ALUout ถ้าไม่เท่ากันจะข้ามไปทำคำสั่งถัดไป

[link : 5th Homework](https://www.youtube.com/watch?v=zwOLIHpMjdo&t=5s)

## 6th HOMEWORK : Control Signal R-format

<br>**1. T1 : Fetch**
![image](https://scontent.fbkk12-4.fna.fbcdn.net/v/t1.0-9/95136916_2335890060044790_3569810957683130368_o.jpg?_nc_cat=103&_nc_sid=730e14&_nc_ohc=bCKuBZuwXHgAX_VYrxU&_nc_ht=scontent.fbkk12-4.fna&oh=3befa3bc19dabb42088d7d431ee480b5&oe=5ED01957)
* 1.MemRead = 1 : จะไปสั่งงานในส่วนMemory
* 2.IorD = 1 : อ่านว่าปัจจุบัน PC ชี้ไปที่ Address ใดใน Memory
* 3.IRWrite = 1 : จะนำค่าที่ไปนำมาจาก Memory ในตำแหน่ง PC ไปใส่ไว้ใน Instruction Register
* 4.ALUScrA = 0 : Mux เลือกค่าจาก 0 ซึ่งคือ PC
* 5.ALUScrB = 1 : Mux เลือกค่าจาก 1 ซึ่งคือ 4
* 6.ALUOP = ADD : จะสั่งให้ นำค่า PC มาบวกกับ 4 และส่งผลไปที่ ALUOut
* 7.PCSource = 1 : จะส่งค่าจากALUOut ไปที่ Mux
* 8.PCWrite = 1 : จะส่งค่าPC+4 ไปที่ PC

<br>**2. T2 : Decode**
![image](https://scontent.fbkk9-2.fna.fbcdn.net/v/t1.0-9/95026710_2335890050044791_6759203184352165888_o.jpg?_nc_cat=109&_nc_sid=730e14&_nc_ohc=_KMvX2CEBNMAX9PBD4u&_nc_ht=scontent.fbkk9-2.fna&oh=24c64cad9f0409dda3babc810c3e3ac6&oe=5ECEFD0D)
* 1.ALUScrA = 0 : Mux เลือกค่าจาก 0 ซึ่งคือ PC
* 2.ALUScrB = 3 : Mux เลือกค่าจาก 3 ซึ่งคือ offset
* 3.ALUOP = 0 : จะทำการadd ค่าPC กับ offset และไปเก็บที่ ALUOut

<br>**3. T3 : ExecALU**
![image](https://scontent.fbkk8-2.fna.fbcdn.net/v/t1.0-9/95247599_2335890040044792_4188088258904719360_o.jpg?_nc_cat=107&_nc_sid=730e14&_nc_ohc=FjQEoc4w8HEAX_p5Pkn&_nc_ht=scontent.fbkk8-2.fna&oh=1ce2dfdebc624dbdd58a21f32a7e6f2a&oe=5ECFA9B6)
* 1.ALUSrcA = 1 : Mux เลือกค่าจาก 1 ซึ่งคือ register rs
* 2.ALUSrcB = 0 : Mux เลือกค่าจาก 0 ซึ่งคือ register rt
* 3.ALUOP = 2 : เป็นคำสั่งที่ต้องการจะคำนวณ เมื่อคำนวณเสร็จแล้วจะเก็บผลลัพธ์ไว้ที่ ALUOut

<br>**4. T4 : WrReg**
![image](https://scontent.fbkk13-1.fna.fbcdn.net/v/t1.0-9/95129905_2335890110044785_2171385102347534336_o.jpg?_nc_cat=108&_nc_sid=730e14&_nc_ohc=wyNnhmXzf1MAX9aNBX4&_nc_ht=scontent.fbkk13-1.fna&oh=85e746c8319becf6da3c05eb1bbc3768&oe=5ECE2AA8)
* 1.MemtoReg = 0 : จะดึงค่าจากALUOut ผ่านทาง Mux
* 2.RegDst = 1 : จะนำตัว register rd มารอรับข้อมูลจาก ALUOut
* 3.RegWrite = 1 : นำค่าALUOut ไปเก็บใน register rd ที่มารอรับข้อมูล

[link : 6th Homework]()

## 7th HOMEWORK : Pipelining
<br>**Pipelining** คือ การนำคำสั่งหลายๆคำสั่งมาทำงานพร้อมกัน ไม่ต้องรอจนกว่าคำสั่งก่อนหน้าจะทำงานเสร็จ โดยใช้วิธีการเคลื่อนย้ายที่ซ้อนกัน (Over lapped) ของคำสั่ง ไปยังกระบวนการหรือขั้นตอนทางเลขคณิต โดยตัวประมวณผลเพื่อทำงานตามคำสั่ง <br>

เราจะยกตัวอย่างเพื่อเปรียบเทียบให้เข้าใจได้ง่ายยิ่งขึ้นโดยใช้วิธีการซักผ้าในการอธิบาย

<br>**การทำงานแบบ Sequential ทำ 4 ครั้งใช้เวลารวม 8 ชั่วโมง**
![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/p960x960/95176917_2335899283377201_9038357790774525952_o.jpg?_nc_cat=105&_nc_sid=730e14&_nc_ohc=zpEbE3Rfke4AX9fQtjV&_nc_ht=scontent.fbkk12-2.fna&_nc_tp=6&oh=f1a5e37adb43d564bb61dc3fb593ec2a&oe=5ECDC26E)

<br>**การทำงานแบบ Pipelined ทำ 4 ครั้งใช้เวลารวม 3.5 ชั่วโมง**
![image](https://scontent.fbkk13-1.fna.fbcdn.net/v/t1.0-9/p960x960/95047693_2335899290043867_8496841686960308224_o.jpg?_nc_cat=108&_nc_sid=730e14&_nc_ohc=j_90qfNTNWwAX9wrfXU&_nc_ht=scontent.fbkk13-1.fna&_nc_tp=6&oh=2375a29dc623701699bdf56ab61935d3&oe=5ECF21BD)

* [link : 7th Homework]()
