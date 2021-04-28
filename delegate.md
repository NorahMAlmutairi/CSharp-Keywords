<div dir="rtl">

# delegate

## المفهوم
  عبارة عن كائن يقوم بمهمة المؤشرات  فهو نوع بيانات ذات القيمة المرجعية يشير الى دالة أي مرجع للدالة بمعنى أخر هو  مفوض للدالة فبدلا من أن يقوم البرنامج مناداة الدالة فان المفوض أو التفويض `delegate` هو من يقوم من مناداة الدالة بطريقة غير مباشرة.
## مثال
في المثال التالي تم انشاء التفويض `delegate` للدالة بالمرجع بحيث تأخذ `parameter` لعدد صحيح وتعيد لنا قيمة لعدد صحيح.

</div>

```C#
using System;

delegate int NumberChanger(int n);
namespace DelegateAppl
{
   class TestDelegate
   {
      static int num = 10;
      public static int AddNum(int p)
      {
         num += p;
         return num;
      }

      public static int MultNum(int q)
      {
         num *= q;
         return num;
      }
      public static int getNum()
      {
         return num;
      }

      static void Main(string[] args)
      {
         //انشاء مثيلات التفويض
         NumberChanger nc1 = new NumberChanger(AddNum);
         NumberChanger nc2 = new NumberChanger(MultNum);
         //استدعاء الدوال عن طريق التفويض
         nc1(25);
         Console.WriteLine("Value of Num: {0}", getNum());
         nc2(5);
         Console.WriteLine("Value of Num: {0}", getNum());
         Console.ReadKey();
      }
   }
}
```