<div dir="rtl">

# ref

## المفهوم


تقوم كلمة
`ref`
بجعل مدخلات الدالة تدخل بالمرجع
(by reference)
وتشبه هذه الكلمة كلمة 
`out`
والفرق أن 
`ref`
تطلب من المستدعي تهيئة المتغير قبل إرساله إلى الدالة.

## مثال
لاستخدام كلمة 
`ref` ،
يجب على من يقوم بالاستدعاء والدالة المستدعاة القيام بتحديد هذه الكلمة صراحةً ، كما في المثال التالي:

</div>

```C#
public static void Main(){
    int number = 1;
    Method(ref number);
    Console.WriteLine(number); // Output: 45
}
static void Method(ref int refArgument)
{
    refArgument = refArgument + 44;
}
```