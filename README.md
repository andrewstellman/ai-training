# ai-training

This is the page for my [Prompting Copilot and ChatGPT for Code](https://learning.oreilly.com/live-events/prompting-copilot-and-chatgpt-for-code/0642572004454/0642572004453/) course. It's still under construction!


# Code for the first exercise

## Java version
```Java
public class Greeter {
    public static String greet(String name) {
        if (name == null || name.trim().isEmpty()) {
            return "Hello, stranger!";
        }
        return "Hello, " + name + "!";
    }

    public static void main(String[] args) {
        System.out.println(greet("Alice"));
        System.out.println(greet(""));
        System.out.println(greet(null));
    }
}
```

## C# Version
```csharp
using System;

public class Greeter
{
    public static string Greet(string name)
    {
        if (string.IsNullOrWhiteSpace(name))
        {
            return "Hello, stranger!";
        }
        return $"Hello, {name}!";
    }

    public static void Main(string[] args)
    {
        Console.WriteLine(Greet("Alice"));
        Console.WriteLine(Greet(""));
        Console.WriteLine(Greet(null));
    }
}
```

# Code for the second exercise

## Java version
```Java
public class CustomSorter {
    public static void bubbleSort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n-1; i++) {
            for (int j = 0; j < n-i-1; j++) {
                if (arr[j] > arr[j+1]) {
                    int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                }
            }
        }
    }

    public static void printArray(int[] arr) {
        for (int i : arr) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}
```

## C# version

```csharp
public class CustomSorter
{
    public static void BubbleSort(int[] arr)
    {
        int n = arr.Length;
        for (int i = 0; i < n - 1; i++)
        {
            for (int j = 0; j < n - i - 1; j++)
            {
                if (arr[j] > arr[j + 1])
                {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }

    public static void PrintArray(int[] arr)
    {
        foreach (int i in arr)
        {
            Console.Write(i + " ");
        }
        Console.WriteLine();
    }
}
```
