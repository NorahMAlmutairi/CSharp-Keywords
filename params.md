<div dir="rtl">

# params

## المفهوم 
تستخدم كـ `parameter`  وتأخذ عدد من الـ `arguments`.  مفيدة عندما يكون عدد الـ `parameters` المستخدمة غير معلومة
, أيضاً عند استخدام الـ `object parameter` فهو يقبل اي نوع من البيانات وأي عدد من `arguments`.
## مثال 
المثال التالي يوضح طريقة استخدام الـ `params`:

</div>

```C#
    // function containing params parameters
    public static int Add(params int[] ListNumbers)
    {
        int total = 0;
          
        // foreach loop
        foreach(int i in ListNumbers) 
        {
            total += i;
        }
        return total;
    }

static void Main(string[] args)
{
      
    // Calling function by passing 5
    // arguments as follows
    int y = Add(12,13,10,15,56);
      
    // Displaying result
    Console.WriteLine(y);
}


```