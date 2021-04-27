<div dir="rtl">

# continue

## المفهوم
نستخدم الجملة continue لتجاوز تنفيذ كود معين في الحلقة, إذاً نستخدمها لتجاوز جزء من كود الـ scope.


## مثال
هذا المثال يتخطى قيمة 4:

</div>


```C#
for (int i = 0; i < 10; i++) 
{
  if (i == 4) 
  {
    continue;
  }
  Console.WriteLine(i);
}
```
