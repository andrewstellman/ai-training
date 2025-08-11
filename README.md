# ai-training

<img width="1287" alt="image" src="https://github.com/user-attachments/assets/9bc4906d-e1ae-43ed-89a2-bc77eba16abb" />

This is the page for my [Prompting Copilot and ChatGPT for Code](https://learning.oreilly.com/live-events/prompting-copilot-and-chatgpt-for-code/0642572004454/0642572004453/) O'Reilly Live Training course.

Here's a PDF of the slide deck:
 * From the 12-Aug-2025 session: [```Copilot and ChatGPT for Java and C# Developers 2025-08-12.pdf```](https://github.com/andrewstellman/ai-training/raw/main/Copilot%20and%20ChatGPT%20for%20Java%20and%20C%23%20Developers%202025-08-12.pdf)
 * From the 16-Apr-2025 session: [```Copilot and ChatGPT for Java and C# Developers 2025-04-16.pdf```](https://github.com/andrewstellman/ai-training/raw/main/Copilot%20and%20ChatGPT%20for%20Java%20and%20C%23%20Developers%202025-04-16.pdf)
 * From the 06-Sep-2024 and 15-Jan-2025 sessions: [```Prompting Copilot and ChatGPT for Code 2024-09-06.pdf```](https://github.com/andrewstellman/ai-training/raw/main/Prompting%20Copilot%20and%20ChatGPT%20for%20Code%202024-09-06.pdf)


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
