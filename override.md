<div dir="rtl">

# override

## المفهوم
 تعريف الدالة التي ورثها الـ Subclass من الـ Superclass من جديد, هذه الدالة الجديدة تكون مشابهة للدالة الموروثة من حيث الشكل فقط, أي لها نفس الإسم و النوع و عدد الباراميترات, لكن محتواها مختلف.
## مثال
في المثال التالي يمكن اعادة كتابة الدالة `Y` الموروثة من `class A`
</div>

```C#


class B : A
{
    public override void Y()
    {
        // Used when B is referenced through A.
        Console.WriteLine("B.Y");
    }
}
}
```