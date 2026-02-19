# ai-training

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/889c7656-dfce-407a-aba5-508496014004" />

<img width="1287" alt="image" src="https://github.com/user-attachments/assets/9bc4906d-e1ae-43ed-89a2-bc77eba16abb" />

This is the GitHub page for my O'Reilly Live Training courses on AI-assisted coding:

* **[AI-Assisted Coding with Claude and Cursor](https://www.oreilly.com/live-events/ai-assisted-coding-with-claude-and-cursor/0642572272111/)** — Using Claude and the Cursor IDE to write, analyze, and improve code
* **[Prompting Copilot and ChatGPT for Code](https://learning.oreilly.com/live-events/prompting-copilot-and-chatgpt-for-code/0642572004454/0642572004453/)** — Using GitHub Copilot and ChatGPT for Java and C# development

Both courses cover prompt engineering fundamentals, AI-assisted code analysis, refactoring, and test generation. The exercises below work with either course—just choose your preferred language.

---

## Slide Decks

### AI-Assisted Coding with Claude and Cursor
 * From the 25-Feb-2026 session: [```AI-Assisted Coding with Claude and Cursor.pdf```](https://github.com/andrewstellman/ai-training/raw/main/AI-Assisted%20Coding%20with%20Claude%20and%20Cursor%202026-02-25.pdf)

### Prompting Copilot and ChatGPT for Code
 * From the 12-Aug-2025 session: [```Copilot and ChatGPT for Java and C# Developers 2025-08-12.pdf```](https://github.com/andrewstellman/ai-training/raw/main/Copilot%20and%20ChatGPT%20for%20Java%20and%20C%23%20Developers%202025-08-12.pdf)
 * From the 16-Apr-2025 session: [```Copilot and ChatGPT for Java and C# Developers 2025-04-16.pdf```](https://github.com/andrewstellman/ai-training/raw/main/Copilot%20and%20ChatGPT%20for%20Java%20and%20C%23%20Developers%202025-04-16.pdf)
 * From the 06-Sep-2024 and 15-Jan-2025 sessions: [```Prompting Copilot and ChatGPT for Code 2024-09-06.pdf```](https://github.com/andrewstellman/ai-training/raw/main/Prompting%20Copilot%20and%20ChatGPT%20for%20Code%202024-09-06.pdf)

---

# Code for the first exercise

Use this code to practice asking an AI to explain and analyze code.

## Python version
```python
class Greeter:
    @staticmethod
    def greet(name: str | None) -> str:
        if name is None or name.strip() == "":
            return "Hello, stranger!"
        return f"Hello, {name}!"


if __name__ == "__main__":
    print(Greeter.greet("Alice"))
    print(Greeter.greet(""))
    print(Greeter.greet(None))
```

## Java version
```java
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

## C# version
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

---

# Code for the second exercise

Use this code to practice asking an AI for improvements, documentation, and refactoring suggestions.

## Python version
```python
class CustomSorter:
    @staticmethod
    def bubble_sort(arr: list[int]) -> None:
        n = len(arr)
        for i in range(n - 1):
            for j in range(n - i - 1):
                if arr[j] > arr[j + 1]:
                    arr[j], arr[j + 1] = arr[j + 1], arr[j]

    @staticmethod
    def print_array(arr: list[int]) -> None:
        print(" ".join(str(i) for i in arr))


if __name__ == "__main__":
    numbers = [64, 34, 25, 12, 22, 11, 90]
    print("Original array:")
    CustomSorter.print_array(numbers)
    
    CustomSorter.bubble_sort(numbers)
    print("Sorted array:")
    CustomSorter.print_array(numbers)
```

## Java version
```java
public class CustomSorter {
    public static void bubbleSort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
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

    public static void main(String[] args) {
        int[] numbers = {64, 34, 25, 12, 22, 11, 90};
        System.out.println("Original array:");
        printArray(numbers);
        
        bubbleSort(numbers);
        System.out.println("Sorted array:");
        printArray(numbers);
    }
}
```

## C# version
```csharp
using System;

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

    public static void Main(string[] args)
    {
        int[] numbers = {64, 34, 25, 12, 22, 11, 90};
        Console.WriteLine("Original array:");
        PrintArray(numbers);
        
        BubbleSort(numbers);
        Console.WriteLine("Sorted array:");
        PrintArray(numbers);
    }
}
```

---

## Questions or issues?

If you run into any problems with the exercises or have questions about the course, feel free to [open an issue](https://github.com/andrewstellman/ai-training/issues) on this repo.
