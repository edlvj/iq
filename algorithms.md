# Algorithms

### What type algoritms do you now?
- Sequence: this type of algorithm is characterized with a series of steps, and each step will be executed one after another.
- Branching: this type of algorithm is represented by the "if-then" problems. If a condition is true, the output will be A, if the condition is false, the output will be B. This algorithm type is also known as "selection type".
- Loop: for this type, the process might be repeatedly executed under a certain condition. It is represented by "while" and "for" problems. But make sure the process will end after a number of loops under the condition. This algorithm type is also known as "repetition type".


### How BST works?
https://ru.wikipedia.org/wiki/%D0%94%D0%B2%D0%BE%D0%B8%D1%87%D0%BD%D0%BE%D0%B5_%D0%B4%D0%B5%D1%80%D0%B5%D0%B2%D0%BE_%D0%BF%D0%BE%D0%B8%D1%81%D0%BA%D0%B0

### How work bubble sort.
The idea is pretty simple: Walk through the list and put two adjacent elements in descending order. But, here’s the kicker: We have to repeatedly walk through the list until there are no longer any swaps to make, meaning, the list is sorter.
```
def bubble_sort(array)
  n = array.length
  loop do
    swapped = false

    (n-1).times do |i|
      if array[i] > array[i+1]
        array[i], array[i+1] = array[i+1], array[i]
        swapped = true
      end
    end

    break if not swapped
  end

  array
end
```

### Write Fibonacci Sequence.
Fibonacci sequence, works such that each number is the sum of the two preceding ones, starting from 0 and 1.
```
def fibo(n, memo = {})
  if n == 0 || n == 1
    return n
  end
  memo[n] ||= fibo(n-1, memo) + fibo(n-2, memo)
end
```

### What is Levenshtein distance?
Levenshtein distance is a string metric for measuring the difference between two sequences. 
Informally, the Levenshtein distance between two words is the minimum number of single-character edits (insertions, deletions or substitutions) required to change one word into the other.

### What is Big O notation? Give an example.
Big O notation is a mathematical way of representing the time complexity of an algorithm. It is typically used to compare the efficiency of different algorithms. For example, if we have two algorithms, one with a time complexity of O(n) and one with a time complexity of O(n^2), then the first algorithm is more efficient.

### What are the main differences between a Heap and a Stack? Which one is faster?
The main difference between a Heap and a Stack is that a Heap is typically used to store data that needs to be accessed quickly, while a Stack is used to store data that needs to be accessed in a specific order. Heaps are typically faster than Stacks.

