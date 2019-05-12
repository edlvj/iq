# Algorithms

### What type algoritms do you now?
- Sequence: this type of algorithm is characterized with a series of steps, and each step will be executed one after another.
- Branching: this type of algorithm is represented by the "if-then" problems. If a condition is true, the output will be A, if the condition is false, the output will be B. This algorithm type is also known as "selection type".
- Loop: for this type, the process might be repeatedly executed under a certain condition. It is represented by "while" and "for" problems. But make sure the process will end after a number of loops under the condition. This algorithm type is also known as "repetition type".

        - logo_asset = asset_path('beautsi_logo.png')
        = wicked_pdf_image_tag(logo_asset)


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