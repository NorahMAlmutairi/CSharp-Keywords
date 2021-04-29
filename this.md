<div dir="rtl">

# this

## المفهوم 
كلمة `this` تشير إلى الـ `instance` الحالي ويتم استخدامه ايضاً للتمييز بين `method parameter` و `class field` إذا كان لهم نفس الأسم.

## مثال 
في هذا المثال يوجد سجل من الطلاب : id , name , subject , age
وللإشارة إلى حقول البيانات من ال `class` نفسه يجب ان نستخدم كلمة `this`.

</div>

```C#
public Student(int id, String name, int age, String subject) {
   this.id = id;
   this.name = name;
   this.subject = subject;
   this.age = age;
} 
```