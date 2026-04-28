SE-2512 TOLENDI ARSEN
What this project is really about

This project is basically an experiment: take a few common algorithms, run them on different kinds of data, and see how they behave in real life — not just on paper.

I implemented:

Bubble Sort (simple but slow)
Quick Sort (fast and widely used)
Linear Search (basic searching)

Then I measured how long they take using System.nanoTime() and compared the results across different array sizes and conditions.

The idea in simple terms

Think of it like this:

Sorting is like organizing a messy bookshelf.
Searching is like finding one specific book.

Some methods are slow but simple (Bubble Sort, Linear Search). Others are smarter and scale better (Quick Sort).

The goal here was to see that difference in action, not just memorize it.

How the algorithms work (quickly)
Bubble Sort

This one is straightforward. It keeps swapping neighbors until everything is in order.

Imagine repeatedly walking past a line of people and swapping anyone standing in the wrong order. It works… but it takes forever if the line is long.

That’s why it’s O(n²) — it gets slow very fast.

Quick Sort

Quick Sort is more strategic. It picks a “pivot” and splits the array into smaller parts, then sorts those parts.

It’s like dividing a messy pile into smaller piles, sorting each one, and combining them.

Most of the time it runs in O(n log n), which is much faster for large data.

Linear Search

This one just checks every element until it finds what you’re looking for.

Like scanning a list from top to bottom.

It works on any data (sorted or not), but it’s not efficient — worst case, it checks everything.

How I tested everything

I didn’t just run the algorithms once. I tested them under different conditions to see patterns.

I used:

Small arrays (10 elements)
Medium arrays (100 elements)
Large arrays (1000 elements)

And for each size:

Random data
Already sorted data

All timing was done using System.nanoTime() so the results are precise.

What actually happened (the interesting part)

Quick Sort was consistently faster than Bubble Sort — especially as the array got bigger.

That’s not surprising, but seeing the numbers makes it real. Bubble Sort starts to struggle badly once you hit large inputs.

Linear Search worked fine for small arrays, but as the size increased, it clearly slowed down since it checks elements one by one.

A few things that stood out

Sorted data made a difference.

Bubble Sort actually got faster on sorted arrays because it can stop early when it detects no swaps. Quick Sort didn’t always benefit as much, depending on how the pivot behaved.

Also, theory mostly matched reality. The Big-O predictions were accurate — but the actual times showed how big the difference really is.

What I learned from this

The biggest takeaway is simple:

Algorithm choice matters a lot.

For small data, it barely matters. For large data, it matters a lot.

Another thing is that real-world performance isn’t just about theory. Implementation details, input data, and even small optimizations can change results.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f8a781d1-ca0d-4109-b93f-c44e9ef561b5" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d638486c-ba66-421a-b1c2-d49cc3e68731" />
