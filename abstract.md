<div dir="rtl">

# abstract

## المفهوم
 أسلوب يستخدم لإخفاء تفاصيل تنفيذ البرنامج. لتطبيق مفهوم الـ Abstraction نستخدم الكلمة `abstract` للدوال والكلاس 

 * `abstract class` : هو كلاس مقيد لا يمكن انشاء كائن منه و للوصول له يجب ان تكون موروثة من كلاس اخر.

 * `abstract method` : يمكن استخدامها داخل الـ abstract class ولا تحتوي على محتوى.

## مثال
  يجب على كلاس `Square` أن يوفر تنفيذاً لدالة `GetArea` لأنها مشتقة من كلاس `Shape`. 
</div>

```C#
abstract class Shape
{
    public abstract int GetArea();
}

class Square : Shape
{
    int side;

    public Square(int n) => side = n;

    // GetArea method is required to avoid a compile-time error.
    public override int GetArea() => side * side;

    static void Main()
    {
        var sq = new Square(12);
        Console.WriteLine($"Area of the square = {sq.GetArea()}");
    }
}
// Output: Area of the square = 144
```