# Objective-C Core Foundation Memory Leak

This repository demonstrates a common memory leak in Objective-C when working with Core Foundation objects.  Specifically, it highlights the importance of manually releasing Core Foundation objects using `CFRelease`.  Failure to do so leads to memory leaks, gradually degrading application performance and potentially causing crashes.

## The Bug

The `bug.m` file contains code that creates a `CFStringRef` but fails to release it. This omission results in a memory leak.

## The Solution

The `bugSolution.m` file shows the corrected code. It properly releases the `CFStringRef` using `CFRelease`, preventing the memory leak.

## How to Reproduce

1. Clone this repository.
2. Open the project in Xcode.
3. Run the `bug.m` example to observe the memory leak (using Instruments to verify).
4. Run the `bugSolution.m` example to see the corrected behavior.

## Lesson Learned

Always remember to release Core Foundation objects using `CFRelease` to prevent memory leaks.  This is crucial for writing stable and efficient Objective-C applications.