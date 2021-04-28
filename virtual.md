<div dir="rtl">

# virtual

## المفهوم
 يتم اضافة كلمة `virtual`  للدالة  الموجودة في superclass  لإمكانية تغيير محتواها في الـ subclass.
## مثال
في المثال التالي تم اضافة كلمة `virtual` لدالة موجودة في superclass للدلالة على امكانية التعديل على محتواها في الـ subclass.
</div>

```C#

class A
{
    public virtual void Y()
    {
        
        Console.WriteLine("A.Y");
    }
}
```