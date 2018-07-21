Add your answers to the Algorithms exercises here.

Max Washington

# Analysis of Algorithms

## Exercise I.

### a)

```
a = 0;
while (a < n * n * n)
  a = a + n * n;
```

I think it would be O(n), because it takes n operations for a to equal n<sup>3</sup>.
Answer: O(n)
### b)

```
// input array is of length n
i = array.length - 1;
while (array[i] > x && i >= 0)
  i = i/2;
```

With each pass `i` is being halved so the number of interation would have to be better then O(n).
Answer: O(log n)

### c)

```
sum = 0;
for (i = 0; i < Math.sqrt(n) / 2; i++)
  for ( j = i; j < 8 + i; j++)
    for (k = j; k < 8 + j; k++)
      sum++;
```

This one is a little confusing to me. I would guess the overall this would run in O(n<sup>½</sup>), since its being halved with each loop. But loops two and three I think would run in constant time O(n)
Answer: O(n<sup>½</sup>)
### d)

```
sum = 0;
  for (i = 1; i < n; i *= 2)
    for (j = 0; j < n; j++)
      sum++;
```


Ok so I know for sure the second loop is in constant time but the first one... I not so sure. 
Answer: First loop: log n * n? Second loop O(n)

### e)

```
sum = 0;
  for (i = 0; i < n; i++)
    for (j = i + 1; j < n; j++)
      for (k = j + 1; k < n; k++)
        for (l = k + 1; l < 10 + k; l++)
          sum++;
```

Its the ones with muliple loops that confuse me a bit. I know the second and third are constant time but the last and the first have me stooped.
Answer: O(n<sup>?</sup>)


### f) 

```
bunnyEars = function (bunnies) { // here bunnies === n
  if (bunnies === 0) return 0;
  return 2 + bunnyEars(bunnies-1);
}
```

One operation per bunny good sir.
Answer: O(n). 

### g)

```
search = function (array, arraySize, target) { // here arraySize === n
  if (arraySize > 0) {
    if (array[arraySize-1] === target) return true;
    else return search(array, arraySize-1, target);
  }
  return false;
}
```

Answer: O(n).

## Exercise II:

a)   Given an array `a` of `n` numbers, design a linear running time algorithm to find the maximum value of `a[j] - a[i]`, where `j ≥ i`.

Not sure

b) Suppose that you have an `n`-story building and plenty of eggs.  Suppose also that an egg is broken if it is thrown off floor `f` or higher, and unbroken otherwise.  Devise a strategy to determine the value of `f` such that the number of dropped eggs is minimized.

We went over this in the lecture I will have to rewatch it.

## Exercise III.

Below is the the pseudo-code for the Quicksort algorithm:

```
function quicksort(array)
  if length(array) <= 1
    return array
  select and remove a pivot element pivot from array
  create empty lists less and greater
  for each x in array
    if x <= pivot then append x to less
    else append x to greater
  return concatenate(quicksort(less), list(pivot), quicksort(greater))
```

a)   Suppose we implement quicksort so that the pivot is always chosen to be the first element of the array.
What is the running time of this algorithm on an input array that is already sorted?  Why?

O(<sup>2</sup>)

b)   Suppose we implement quicksort so that the pivot is always magically chosen to be the median element
of the array.  What is the running time of this algorithm?  Why?

Im not sure 