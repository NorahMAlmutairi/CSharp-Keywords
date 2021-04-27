<div dir="rtl">

# out

## المفهوم


تقوم كلمة
`out`
بجعل مدخلات الدالة تدخل بالمرجع
(by reference)
وتشبه هذه الكلمة كلمة 
`ref`
والفرق أن 
`out`
لا تطلب من المستدعي تهيئة المتغير قبل إرساله إلى الدالة.

## مثال
لاستخدام كلمة 
`out` ،
يجب على من يقوم بالاستدعاء والدالة المستدعاة القيام بتحديد هذه الكلمة صراحةً ، كما في المثال التالي:

</div>

```C#
public static void Main(){
    int initializeInMethod;
    OutArgExample(out initializeInMethod);
    Console.WriteLine(initializeInMethod);     // value is now 44
}

static void OutArgExample(out int number)
{
    number = 44;
}
```