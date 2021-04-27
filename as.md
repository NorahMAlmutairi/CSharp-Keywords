<div dir="rtl">

# as

## المفهوم 
تقوم كلمة
`as`
بتحويل نتيجة تعبير ما إلى مرجع معين أو نوع بيانات يقبل قيمة
`null`.
إذا لم يكن التحويل ممكناً ، تقوم كلمة 
`as`
بإرجاع قيمة
`null`.
على عكس تغيير هيئة النوع
(casting) ،
لا تقوم كلمة
`as`
بإلقاء خطأ
(exception)
أبداً.

## المثال
يوضح المثال التالي كفية إستخدام كلمة `as`:
</div>

```C#
IEnumerable<int> numbers = new[] { 10, 20, 30 };
IList<int> indexable = numbers as IList<int>;
if (indexable != null)
{
    Console.WriteLine(indexable[0] + indexable[indexable.Count - 1]);  // output: 40
}
```
