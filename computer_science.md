# Computer Science

### Solve number 8 from 10 digit to 2 digit system and from 2 digit to 10 digit. 
- TODO:answer

### How work HTTP caching?
We always must return Last-Modified or ETag Headers for clients.
If response body on server not changed we must return HTTP status - 304 Not Modified
If body changed we must return HTTP status - 200 Not Modified
 
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

### What is DNS and how does it works.
The Domain Name Systems (DNS) is the phonebook of the Internet. Humans access information online through domain names, like nytimes.com or espn.com. Web browsers interact through Internet Protocol (IP) addresses. DNS translates domain names to IP addresses so browsers can load Internet resources. 
For example:

If you enter in browser domain example.com
DNS resolver make request to DNS servers and find DNS record with his domain and redirect to IP of Server.

### Do you can do ipv4 addressing.
- TODO:answer

### What is UUID?
Universally unique identifier (UUID) is a 128-bit number used to identify information in computer systems