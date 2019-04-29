# Algorithms

### What type algoritms do you now?
- Sequence: this type of algorithm is characterized with a series of steps, and each step will be executed one after another.
- Branching: this type of algorithm is represented by the "if-then" problems. If a condition is true, the output will be A, if the condition is false, the output will be B. This algorithm type is also known as "selection type".
- Loop: for this type, the process might be repeatedly executed under a certain condition. It is represented by "while" and "for" problems. But make sure the process will end after a number of loops under the condition. This algorithm type is also known as "repetition type".


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

### Please write Fibonacci Sequence.
- TODO:answear