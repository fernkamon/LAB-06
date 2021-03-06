#ใบงานที่ 6
##เรื่อง การใช้งานคำสั่ง Console.Read() และ Console.ReadLine()
##วัตถุประสงค์
1). เพื่อให้นักศึกษาบอกชื่อ method ที่ใช้ในการรับค่าตัวอักษรพื้นฐานในภาษา C# ได้

2). เพื่อให้นักศึกษาสามารถใช้คำสั่งรับค่าตัวอักษรได้
##ความรู้เบื้องต้น
คำสั่งที่ใช้รับค่าตัวอักษรทางอินพุตมาตรฐานของ C# คือ ```Console.Read()``` และ ``` Console.ReadLine()``` โดยทั้งสองจะมีข้อแตกต่างกันคือ ```Read()``` จะอ่านตัวอักษร ส่วน ```ReadLine()``` จะอ่านสตริง จนกว่าจะกด Enter ในการรับค่าด้วย ```Read()``` และ ```ReadLine()``` จะรับเฉพาะค่า ASCII เท่านั้น หากต้องการรับค่าตัวเลข จะต้องมีการแปลง ASCII ของตัวเลขที่พิมพ์เข้ามาให้เป็นค่าตัวเลข (การรับอักษร “22” จะไม่ได้หมายถึงค่าตัวเลข 22) 

##ลำดับขั้นการทดลอง

1). สร้าง Project ตั้งชื่อเป็น Lab6 เพื่อทดลองการใช้งานคำสั่ง ```Console.ReadLine()``` และ ```Console.ReadLine()```

2). โปรแกรมสำหรับรับตัวอักษรจากคีย์บอร์ด 

  2.1). แก้ไขโปรแกรมให้เป็นดังรูป

 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic1.png)

  2.2).	โปรแกรม และบันทึกผลที่ได้

    เมื่อพิมพ์ตัวอักษรใดไป แล้วกด ENTER ตัวอักษรนั้นก็จะปรากฎ ออกมาที่อีกบรรทัด ตามที่เขียนไว้ ดังนี้
    
![](https://github.com/fernkamon/LAB-06/blob/master/imgs/1.JPG)

###คำถาม 6.1 ถ้าพิมพ์ตัวอักษรจำนวนหลายๆ ตัวแล้วกด Enter จะได้ผลอย่างไร ทำไมจึงเป็นเช่นนั้น

      ออกมาแค่ตัวอักษรเดียว เพราะ char นั้นจะเก็บค่าแค่ 1 ตัวเท่านั้น ดังรูปต่อไปนี้
      
  ![](https://github.com/fernkamon/LAB-06/blob/master/imgs/2.JPG)

###คำถาม 6.2 ในบรรทัดที่ 11 ซึ่งมีโปรแกรมเป็น ```ch = (char)Console.Read();```  นั้น ถ้าตัด ```(char)``` ออกไป จะเกิดอะไรขึ้น ให้อธิบายประกอบ

    เกิด error ขึ้น เนื่องจากว่า ไม่ทราบว่าจะเเปลงให้เป็นชนิด int หรือ char กันแน่ ดังรูปนี้
    
  ![](https://github.com/fernkamon/LAB-06/blob/master/imgs/error.JPG) 


3).	โปรแกรมสำหรับรับ string จากคีย์บอร์ด
 
 3.1).	แก้ไขโปรแกรมให้เป็นดังรูป

 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic2.png)
 
 3.2).	โปรแกรม และบันทึกผลที่ได้

      สามารถที่จะพิมพ์ข้อความได้ยาวขึ้น ดังนี้
 
 ![](https://github.com/fernkamon/LAB-06/blob/master/imgs/string.JPG)
 

4).	โปรแกรมสำหรับรับค่าตัวเลข เนื่องจากคำสั่ง ```Read()``` และ ```ReadLine()``` จะรับเฉพาะตัวอักษร การรับตัวเลข เราต้องใช้เมธอด TryParse() มาช่วยแปลงค่า

4.1).	แก้ไขโปรแกรมให้เป็นดังรูป
 
 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic3.png)

4.2).	รัน โปรแกรม โดยป้อนตัวเลขใดๆ และบันทึกผลที่ได้

![](https://github.com/fernkamon/LAB-06/blob/master/imgs/num.JPG)

###คำถาม 6.3 ถ้าเราป้อนตัวอักษรลงไปแทนที่ตัวเลข จะเกิดอะไรขึ้น มีวิธีการป้องกันหรือแก้ไขอย่างไร

       โปแกรมจะ error ถึงแม้ว่ารันผ่านแต่ข้อมูลก็จะไม่ได้ตามที่ต้องการ อาจจะใช้วิธีการป้องกันโดยการบอกให้ป้อนแต่ตัวเลขเท่านั้น 

5).	โปรแกรมสำหรับรับค่าตัวเลข แต่ในบางกรณีที่ผู้ใช้ป้อนตัวอักษร จะทำให้เกิด error และทำให้โปรแกรม hang ได้ จึงต้องมีการป้องกันโดยใช้ประโยค ```try{…} catch{…}```  (ประโยค ```try{…} catch{…}``` นี้จะศึกษารายละเอียดภายหลัง)

  5.1).	แก้ไขโปรแกรมให้เป็นดังรูป

  ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic4.png)

  5.2).	รัน โปรแกรม โดยป้อนตัวเลขใดๆ และบันทึกผลที่ได้

        ป้อน INPUT ได้ถึง 2ครั้ง และยังสามารถนำเลขจาก INPUT ทั้ง 2 ครั้ง มาทำการ บวกกันได้ด้วย ดังรูป
        
  ![](https://github.com/fernkamon/LAB-06/blob/master/imgs/add.JPG)

###คำถาม 6.4 ถ้าเราป้อนตัวอักษรลงไปแทนที่ตัวเลข จะเกิดอะไรขึ้น เหมือนหรือต่างจากโปรแกรมก่อนหน้านี้อย่างไร

          จะปรากฎข้อความ error แล้วจบการทำงาน ดังรูปต่อไปนี้
          
  ![](https://github.com/fernkamon/LAB-06/blob/master/imgs/no1.JPG)
  
  ![](https://github.com/fernkamon/LAB-06/blob/master/imgs/no2.JPG)

##แบบฝึกหัด ให้เขียน code ในการรับค่าอินพุตต่อไปนี้และแสดงออกหน้าจอให้ถูกต้อง
``` Name :  (ป้อนชื่อของนักศึกษา). ```

``` Lastname : (ป้อนนามสกุลนักศึกษา).```

``` ID : (ป้อนรหัสนักศึกษา).```

``` GPA : (ป้อนเกรดเฉลี่ยนักศึกษา โดยมีทศนิยมสองหลัก).```

        Code

```
    using System;


namespace Lab6
{
    class Program
    {
        static void Main(string[] args)
        {
            try
            {
                string str;
                Console.Write("Please enter Name : ");
                str = Console.ReadLine();

                Console.Write("Please enter Lastname : ");
                str = Console.ReadLine();

                Console.Write("Please enter ID : ");
                int val1 = Convert.ToInt32(Console.ReadLine());

                Console.Write("Please enter GPA : ");
                double val2 = Convert.ToDouble(Console.ReadLine());

                Console.WriteLine("----------------------------------------------------");
                Console.WriteLine("Name : " + str);
                Console.WriteLine("Lastname : " + str);
                Console.WriteLine("ID : " + val1);
                Console.WriteLine("GPA :  "+ val2);
            }
            catch (Exception e)
            {
                Console.WriteLine("Error : " + e.ToString());
            }
        }
    }
}
```

![](https://github.com/fernkamon/LAB-06/blob/master/imgs/student.JPG)
      
