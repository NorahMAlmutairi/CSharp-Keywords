<div dir="rtl">

# private

## المفهوم
المتغيرات و الدوال التي يتم تعريفها كـ `private` يمكن الوصول لها فقط من داخل class الذي تم تعريفها فيه.
## مثال
المتغير `i` يمكن الوصول له فقط من داخل الـ class الذي تم تعريفه فيه.

ملاحظة : المتغير أو الدالة الذي لا يتم تحديد نوع الوصول له يصبح `private` بشكل تلقائي.
</div>

```C#
class Employee
{
    private int i;
    double d;   // private access by default
}
```