<div dir="rtl">

# base

## المفهوم 
كلمة `base` تستخدم للوصول الى محتويات الـ 
base class من داخل الكلاس الموروث:
* استدعاء دالة على الكلاس الأساسي الذي تم التعديل عليه بواسطة دالة أخرى.
* تحديد أي base class constructor الذي يجب استدعاؤه عند إنشاء `instances` من الكلاس الموروث.

## المثال
في المثال التالي, كلاَ من الكلاس الأساسي `Person` والكلاس الموروث `Employee` لديهم دالة تسمى `Getinfo`.
بإستخدام كلمة `base` من الممكن ان تستدعي دالة `Getinfo` في الكلاس الأساسي من داخل الكلاس الموروث.
</div>


```C#
public class Person
{
    protected string ssn = "444-55-6666";
    protected string name = "John L. Malgraine";

    public virtual void GetInfo()
    {
        Console.WriteLine("Name: {0}", name);
        Console.WriteLine("SSN: {0}", ssn);
    }
}
class Employee : Person
{
    public string id = "ABC567EFG";
    public override void GetInfo()
    {
        // Calling the base class GetInfo method:
        base.GetInfo();
        Console.WriteLine("Employee ID: {0}", id);
    }
}

class TestClass
{
    static void Main()
    {
        Employee E = new Employee();
        E.GetInfo();
    }
}
/*
Output
Name: John L. Malgraine
SSN: 444-55-6666
Employee ID: ABC567EFG
*/
```