# CN210 : computer architecture

## 1st HOMEWORK : Jump format(J-format)
<br>**รูปแบบของ j-format**
|Op Code|Address|
|-----|-----|
|6 bits|26 bits|
* Op Code(Operation Code) : Op Code ของ J-format คือ **000010**
* Address หรือ jump target address : จะเป็นตำแหน่งที่เราจะกระโดดไปทำงานหลังจากที่เราแปลง 32 bits เป็น 26 bits <br>

**วิธีการเขียนคำสั่ง jump** <br>
แบ่งเป็น 2 ส่วนคือ Op Code และ Address โดย Op Code ของคำสั่ง jump คือ **000010** ส่วนAddressเราต้องทำการแปลงจาก 32 bits มาเป็น 26 bits เสียก่อนโดยทำดังนี้
![image](https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-0/p480x480/94701495_2335369096763553_3772555361337212928_o.jpg?_nc_cat=104&_nc_sid=730e14&_nc_ohc=NWmD8ESa498AX-Z6-lB&_nc_ht=scontent.fbkk12-2.fna&_nc_tp=6&oh=aa35d2b4e85b2fc966ddcc303e13e192&oe=5ECBF73A)

