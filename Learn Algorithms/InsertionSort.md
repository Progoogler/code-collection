
# Insertion Sort 
Insertion Sort is an elementary sorting algorithm that performs particularly fast for:

  1. Nearly sorted arrays.
  2. Arrays with 20 or less items.

It's a stable algorithm with low overhead compared to sorting algorithms with better worst case asymptotic
runtime complexities such as Merge Sort or Quick Sort.

Note: Due to the properties mentioned above and its tight loop that accesses memory in increasing order only, Insertion Sort
is often used as the recursive base case for higher overhead divide-and-conquer algorithms when theproblem size is small. 
I.e, the last remaining 20 items to be sorted in a Merge Sort.

Copy and paste the code snippet below into your browser console to watch it in action.

```javascript
"use strict";

const swap = (a,m,n) => {
  let temp = a[m];
  a[m] = a[n];
  a[n] = temp;
};

const insertionSort = array => {
	let index,
	    len = array.length;

	for (let j = 1; j < len; j++) {
		if (array[j] < array[j-1]) {
			index = j;
			while (array[index] < array[index-1]) {
        console.log(array)
				swap(array, index, index-1);
				index -= 1;
			}
		}
	}
	return array;
};

var arr = [];
for (let n = 0; n <= 10; n++) {
	arr.push(Math.ceil(Math.random() * 100));
}
insertionSort(arr);
```