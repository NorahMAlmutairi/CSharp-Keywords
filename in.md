<div dir="rtl">

# in

## المفهوم

تقوم كلمة
`in`
بجعل مدخلات الدالة تدخل بالمرجع
(by reference)
ولكن تضمن عدم تغيير قيمة المدخل.
وتشبه هذه الكلمة كلمات مثل 
`out`
و
`ref`
والفرق أن 
`in`
لا تقوم بتغيير القيمة الحقيقية للمدخل خارج الدالة وتضمن عدم حدوث ذلك.

## مثال
في هذا المثال، يتم إدخال مدخل بإستخدام كلمة
`in`
 ، مما يضمن عدم تغيير القيمة.
 وإذا حاول المبرمج تغييرها ، سيتم حدوث خطأ.

</div>

```C#
public static void Main(){
    int readonlyArgument = 44;
    InArgExample(readonlyArgument);         // Call the function
    Console.WriteLine(readonlyArgument);    // value is still 44
}

static void InArgExample(in int number)
{
    number = 19; // Causes an error, as 'number' is readonly!
}
```
