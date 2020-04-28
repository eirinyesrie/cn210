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
![image](https://www.google.com/search?q=johnny+depp&sxsrf=ALeKk02KMWnxFPvlXciSgnS4rODQ3VPzGA:1588082755892&source=lnms&tbm=isch&sa=X&ved=2ahUKEwiIqaekpYvpAhV7zDgGHYX4AcwQ_AUoAXoECBgQAw&biw=1536&bih=754#imgrc=qU3mhXexz2T2HM)

