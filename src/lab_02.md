# Lab 2 (Week 4)

## Task 1 – Serial Code - Finding Prime Numbers [*Pre-class activities*]

Write a serial C program to search for prime numbers which are strictly less than an
integer \\((n\\), provided by the user. The program should print to the standard output a
list of all prime numbers found.

### Example

For instance, if the user inputs \\(n\\) as \\(10\\) on the terminal, the prime numbers
being printed are: \\(2, 3, 5, 7\\). (sorted in ascending order). If the value of \\(n\\)
is large (e.g., \\(n = 1,000,000\\)), then the list of prime numbers should be printed to
a text file.

### Hint

- How to check if a number, let's say \\(k\\), is prime? Yes, you can check if \\(k\\) is
  divisible by \\(2\\), by \\(3\\), by \\(4\\), by \\(5\\), ..., by \\(k-1\\).
- However, there is a (slightly) smarter way. Imagine \\(k\\) is not a prime number,
  there must exist two integers \\(m\\) and \\(n\\) such that \\(m\\) times \\(n\\)
  equals \\(k\\). Will both \\(m\\) and \\(n\\) be larger than the square root of
  \\(k\\)? No! If \\(m\\) is larger than the square root of \\(k\\), then \\(n\\) must be
  smaller than the square root of \\(k\\), right?
- In other words, you don't need to check until \\(k – 1)\\) (think what happens when
  \\(k\\) is really large).
- Make sure you know how to use the [`sqrt()`](https://en.cppreference.com/w/cpp/numeric/math/sqrt)
  from the `math.h` header
- Ensure you link the standard math library `libm.so` using the `-l` flag for `gcc` eg.
  `gcc -lm -o task1 task1.c`

> Note the `lib` prefix as well as file extension (`*.so` or `*.a` on Linux) of libraries
> linked by `gcc` (or `clang`) is omitted when using the `-l` flag. Only the library name
> is needed.

Measure the time required to search for prime numbers less than an integer \\(n\\) when
\\(n = 1,000,000\\). You will need to explain your approach, demonstrate and run your
code, and submit the serial code to Moodle in a file `task1.c`.

## Task 2 – POSIX Threads - Finding Prime Numbers

Write a parallel version of your serial code in C utilizing POSIX Threads. In this part,
your team will need to design a parallel partitioning scheme distributing the workload
among the threads, and implement your design in C. After you implement the task, measure
again the time required to search for prime numbers less than an integer \\(n\\) when
\\(n = 10,000,000\\) and compute the speed-up by your parallel implementation.

> Note that the value of \\(n\\) may need to be adjusted to cope with different machine
> architectures.

Make sure you also include information on the number of processors (cores) available in
your machine and the number of threads you have created. Make sure your code can produce
a sorted list of prime numbers (in ascending order).

Common questions you need to consider:

- What is the speed-up? Is it reasonable? Please explain.
- How would the speed-up change when you increase and decrease the number of threads?
  Why?
- How do you distribute the tasks to the threads? Is it a good approach? Please explain.

You will need to explain your approach, demonstrate and run your code, and answer
questions in the presentation (and Q&A) session. Submit your code for this task in a file
`task2.c` to Moodle.

## Task 3 – OpenMP - Finding Prime Numbers

Write a parallel version of your serial code in C utilizing OpenMP. In this part, you
will need to design a parallel partitioning scheme, distributing the workload using
OpenMP, and implement your design in C.

After you implement the task, measure again the time required to search for prime numbers
less than an integer \\(n\\) when \\(n = 10,000,000\\) and compute the speed-up by your
parallel implementation.

> Note that the value of \\(n\\) may need to be adjusted to cope with different machine
> architectures.

Make sure you also include information on the number of processors (cores) available in
your machine and the OpenMP configurations you have used. Make sure your code can produce
a sorted list of prime numbers (in ascending order).

Common questions you need to consider:

- What is the speed-up? Is it reasonable? Please explain.
- How would the speed-up change when you increase and decrease the number of threads in
  OpenMP? Why?
- How do you distribute the tasks to the threads? Is it a good approach? Please explain.
  You will need to explain your approach, demonstrate and run your code, and answer
  questions in the presentation (and Q&A) session. Submit your code for this task in a
  file `task3.c` to Moodle.

## Submission checklist:

- `task1.c`
- `task2.c`
- `task3.c`
- Presentation slides or documents (in pptx, doc or pdf format)
- AI declaration (in PDF), if not already in presentation slides.

