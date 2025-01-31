# GCD and NSAutoreleasePool Memory Leak in Objective-C

This repository demonstrates a subtle memory leak that can occur in Objective-C when using Grand Central Dispatch (GCD) and `NSAutoreleasePool` without proper consideration. The issue arises from the lifecycle of objects created and used within GCD blocks. 

The `bug.m` file contains code that exhibits the memory leak. The `bugSolution.m` file provides a corrected version with proper memory management within the GCD block, ensuring that objects are released appropriately regardless of the thread context.