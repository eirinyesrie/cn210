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
![image](https://scontent.fbkk12-4.fna.fbcdn.net/v/t1.0-9/p960x960/94688618_2335505790083217_3731359078711033856_o.jpg?_nc_cat=110&_nc_sid=730e14&_nc_ohc=_GpoaKJz5C8AX9xzV15&_nc_ht=scontent.fbkk12-4.fna&_nc_tp=6&oh=628c2c1624d81edacf2509a8b09fa69b&oe=5ECED5FB)

* Store Word (sw)
