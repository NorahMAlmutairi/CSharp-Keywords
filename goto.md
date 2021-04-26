<div dir="rtl">

# goto

## Concept 
تنقل عبارة `goto` تحكم البرنامج مباشرة إلى تعليمة معنونة.

الاستخدام الشائع لـ `goto` هو نقل التحكم إلى تسمية حالة تبديل معينة أو التسمية الافتراضية في عبارة `switch`.

تعتبر عبارة `goto` مفيدة أيضًا في الخروج من الحلقات المتداخلة بعمق (nested loops).
## Example 
يوضح المثال التالي استخدام `goto` في عبارة` switch`:

</div>

```C#
class SwitchTest
{
    static void Main()
    {
        Console.WriteLine("Coffee sizes: 1=Small 2=Medium 3=Large");
        Console.Write("Please enter your selection: ");
        string s = Console.ReadLine();
        int n = int.Parse(s);
        int cost = 0;
        switch (n)
        {
            case 1:
                cost += 25;
                break;
            case 2:
                cost += 25;
                goto case 1;
            case 3:
                cost += 50;
                goto case 1;
            default:
                Console.WriteLine("Invalid selection.");
                break;
        }
        if (cost != 0)
        {
            Console.WriteLine($"Please insert {cost} cents.");
        }
        Console.WriteLine("Thank you for your business.");

        // Keep the console open in debug mode.
        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
    }
}
/*
Sample Input:  2

Sample Output:
Coffee sizes: 1=Small 2=Medium 3=Large
Please enter your selection: 2
Please insert 50 cents.
Thank you for your business.
*/
```