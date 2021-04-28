<div dir="rtl">

# protected

## المفهوم
الدالة أو المتغير الذي يتم تعريفه كـ `protected` يمكن الوصول إليه فقط من الكلاسات الموجودة في نفس الـ package أو من الكلاسات التي ترث منه.

## مثال
في هذا المثال يوجد متغير x وهو  `protected`  يمكن الوصول له من class يرث منه ولكن لا يمكن الوصول له من class اخر.

</div>

```C#
class ClassTest
{
    //Protected variable
    protected int _a;
}

class ClassTest2 : ClassTest
{
    ClassTest2()
    {
        this._a = 10; // can access from this class
    }
}

class ClassTest3
{
    ClassTest3()
    {
        this._a = 10; // can't access from this class
    }
}
         {
```