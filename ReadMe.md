
#  Dynamic Memory Allocator in C++

![C++ Badge](https://img.shields.io/badge/Language-C++-blue?style=flat-square&logo=c%2B%2B)
![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)
---

This repository showcases a custom Memory Allocator written in C++.It handles:

- 🛠️ **Memory Allocation **
- 🗑️ **Memory Deallocation**

The core data structure is a bitmap*that tracks available memory.

---

##  Features 

###  First Fit Allocation
- **How it works**:  
  Allocates memory by scanning the bitmap from **left to right** until it finds a large enough block.  
- **Failure Case**:  
  If there isn't enough space, the user gets an **"Out of Memory"** notification.  
-  **Efficiency**: Quick but might leave gaps (fragmentation).

###  Best Fit Allocation
- **How it works**:  
  Scans the entire bitmap to find the **smallest block** large enough to fit the requested memory.  
-  **Outcome**: Perfectly fits memory blocks where possible, minimizing wasted space.  
-  **Trade-off**: Takes more time due to full scans.
---

##  Fragmentation 
**Cheese-like gaps** in memory (enough total space but not contiguous) can cause allocation failures. 🧵  

###  Defragmentation
- Rearranges memory to consolidate free blocks.  
- ⚠️ **Note**: This process is time-intensive and best avoided unless necessary.

---

##  Additional Ideas 
-  **Reallocation**: Create a **best-fit memory layout** for better performance.  
-  **Granularity vs. Space**: Balance block size for space efficiency.

---


---

##  Contributing 
 **Join the project!** If you have any suggestions, optimizations, or enhancements, feel free to open a Pull Request or Issue. Every contribution matters!

---


