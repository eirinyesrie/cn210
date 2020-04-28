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
<br>การทำงานของคอมพิวเตอร์คำสั่ง I-Type ทำงานดังนี้
![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/p960x960/94928612_2335520910081705_1391097185134706688_o.jpg?_nc_cat=104&_nc_sid=730e14&_nc_ohc=OFtFropaAbcAX_KgZye&_nc_ht=scontent.fbkk12-2.fna&_nc_tp=6&oh=e6e85d2de374a2af7cf7f1637e8b39c2&oe=5ECDC0B6)

* [link : 2nd Homework](https://www.youtube.com/watch?v=7si2xAQyQ2k)

## 3rd HOMEWORK : ความแตกต่างระหว่าง single cycle และ multi cycle

| single cycle | multi cycle |
| ------- | ------- |
|![image](https://scontent.fbkk12-4.fna.fbcdn.net/v/t1.0-9/94442656_2335545196745943_4017612434171756544_n.jpg?_nc_cat=103&_nc_sid=730e14&_nc_ohc=cijODhik3NoAX9LO1F2&_nc_ht=scontent.fbkk12-4.fna&oh=a9d2234ae2bedfc37f7592f03060a1d4&oe=5ECCD2E4)<br>ใน 1 คำสั่งสามารถจบการทำงานภายใน 1 clock|![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/94884180_2335545200079276_170332192436649984_n.jpg?_nc_cat=105&_nc_sid=730e14&_nc_ohc=9yKIl2fOGyIAX-LU3Mp&_nc_ht=scontent.fbkk12-2.fna&oh=453fd1d350e9953b8414725afa24f352&oe=5ECD0109)<br>ใน 1 คำสั่งไม่สามารถจบการทำงานได้ภายใน 1 clock(ขึ้นกับความยากง่ายของคำสั่ง)|
|![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/95258776_2335547863412343_5459161036764479488_n.jpg?_nc_cat=105&_nc_sid=730e14&_nc_ohc=ZzyqqX49_i0AX_p-Ox9&_nc_ht=scontent.fbkk12-2.fna&oh=9525dfe1c02a61a6dd3632866c3366eb&oe=5ECD1389)<br>มี memory 2 ชิ้น(Harvard architecture)|![image](https://scontent.fbkk13-1.fna.fbcdn.net/v/t1.0-9/95056024_2335547856745677_2377260902232621056_n.jpg?_nc_cat=108&_nc_sid=730e14&_nc_ohc=3dhXnWDqYXIAX_SCIaA&_nc_ht=scontent.fbkk13-1.fna&oh=18d7eed15b46e93499c6edb3ed619d6f&oe=5ECC7309)<br>มี memory 1 ชิ้น(Von Neuman architecture)|
|![image](https://scontent.fbkk12-3.fna.fbcdn.net/v/t1.0-9/95494492_2335551273412002_5143926783883608064_n.jpg?_nc_cat=102&_nc_sid=730e14&_nc_ohc=KTZYJt2fcEMAX_Vi3L4&_nc_ht=scontent.fbkk12-3.fna&oh=8eddb70a33865862dba2b2b9bc9d47ca&oe=5ECD1A2C)<br>มี ALU 3 ตัว (2 adders)|![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/94880810_2335551243412005_572084635895332864_n.jpg?_nc_cat=104&_nc_sid=730e14&_nc_ohc=MYExwdOlOYoAX-kSfVB&_nc_ht=scontent.fbkk12-2.fna&oh=66b885fbae17c4110df40874a58fc3b6&oe=5ECCBCDD)<br>มี ALU เพียงตัวเดียว|
|![image](https://scontent.fbkk8-3.fna.fbcdn.net/v/t1.0-9/94768354_2335554010078395_1954068372874330112_n.jpg?_nc_cat=111&_nc_sid=730e14&_nc_ohc=FdCUN35-wioAX9p9PsJ&_nc_ht=scontent.fbkk8-3.fna&oh=dfb1e2a067ec98bb8d79592352d87acd&oe=5ECD2D6C)<br>ไม่มี registor A,B ไว้สำหรับเก็บdataชั่วคราว|![image](https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.0-9/94976779_2335554006745062_3618777841170120704_n.jpg?_nc_cat=106&_nc_sid=730e14&_nc_ohc=uBbcCRvWNXcAX_ARph6&_nc_ht=scontent.fbkk12-1.fna&oh=fbaa5329ba22dddc2e72b75514332485&oe=5ECEBCDF)<br>มี registor A,B ไว้สำหรับเก็บdataชั่วคราว|
|![image](https://scontent.fbkk8-2.fna.fbcdn.net/v/t1.0-9/95159582_2335557786744684_2563854863054143488_n.jpg?_nc_cat=107&_nc_sid=730e14&_nc_ohc=Pr7PEKC4ecQAX_Nvm6F&_nc_ht=scontent.fbkk8-2.fna&oh=0120f01f1638a54b5b3e0eac2acf96ff&oe=5ECFD37E)<br>ไม่มี instruction registor และ data registor|![image](https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.0-9/95379513_2335557780078018_7070447704672829440_n.jpg?_nc_cat=106&_nc_sid=730e14&_nc_ohc=wh99XjMR2kYAX93w8pn&_nc_ht=scontent.fbkk12-1.fna&oh=789445debc02e73b829128acc8fafc93&oe=5ECEB37B)<br>มี instruction registor และ data registor|

* [link : 3rd Homework](https://www.youtube.com/watch?v=-tSL3mxhbcg)

* [link : 4th Homework](https://www.youtube.com/watch?v=WLNe0p6ohww)

* [link : 5th Homework](https://www.youtube.com/watch?v=zwOLIHpMjdo&t=5s)

* [link : 6th Homework]()

* [link : 7th Homework]()
