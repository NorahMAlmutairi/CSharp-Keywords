# as

## Concept 
The `as` operator explicitly converts the result of an expression to a given reference or nullable value type. If the conversion is not possible, the `as` operator returns `null`. Unlike a cast expression, the `as` operator never throws an exception.

## Example 
The following example demonstrates the usage of the `as` operator:

```C#
IEnumerable<int> numbers = new[] { 10, 20, 30 };
IList<int> indexable = numbers as IList<int>;
if (indexable != null)
{
    Console.WriteLine(indexable[0] + indexable[indexable.Count - 1]);  // output: 40
}
```
