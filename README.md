# cop4600-project-2--memory-management-layering-solved
**TO GET THIS SOLUTION VISIT:** [COP4600 Project 2- Memory Management & Layering Solved](https://www.ankitcodinghub.com/product/cop4600-p2-memory-management-layering-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;120465&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COP4600  Project 2- Memory Management \u0026amp; Layering Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
<h1>Overview</h1>
Due to your excellent work handling the metadata for project Sky Skink, the great Silurian overload Reptar himself has commissioned your work in designing a new custom Memory Manager application for Reptilian. This new project, deemed <strong><em>Project Repto</em></strong>, is built using functionality from various layers of the OS to avoid human corruption. For extra security, the memory manager will write a log of its state when closed. If all goes well, your manager will be deployed all throughout the great Lizard Legion.

In this project, you will implement a memory manager in C++, whose features include initializing, tracking, allocating, and deallocating sections of memory. You will integrate the memory manager into a console program that we provide. The program will provide some simple unit testing to check for correctness but will <strong>not </strong>check for memory leaks and errors – <em>it is your responsibility to test for leaks/errors and ensure overall correctness! </em>You must also maintain a <u>valid listing of memory holes</u> and <u>combine those holes</u> as appropriate and discussed in the class and text. You’ll then create a short video to demonstrate your code and submit the project via Canvas.

<h1>&nbsp;Structure</h1>
Modern operating systems are often built in layers with specific goals and limited privileges. Layering also facilitates the implementation of recognized standards by separating hardware and OS-specific implementations from generalized API calls. Your memory manager will make use of these standard functions so that it can be used in console applications.

The project is broken into three main parts:

<ul>
<li>Write a memory manager in C++ using basic system functionality.</li>
<li>Integrate the memory manager into the console-based testing program we provide.</li>
</ul>
<strong>Figure 1: Memory manager is instantiated from a console program.</strong>

While exact implementation may vary, <em><u>the library functions must match the signatures laid out in this document.</u></em>

<h2>&nbsp;Specification</h2>
The memory manager will incorporate the following class(es) and function(s).

<u>Memory Manager Class</u>

The Memory Manager will handle the allocation/deallocation of memory and provide details of its state. How the class keeps track of allocation/deallocation is implementation dependent and is left for the student to decide. <strong>MemoryManager.h </strong>and <strong>MemoryManager.cpp </strong>will contain declaration and definition, respectively.

<em>public </em><strong>MemoryManager</strong>(unsigned wordSize, std::function&lt;int(int, void *)&gt; allocator)

Constructor; sets native word size (in bytes, for alignment) and default allocator for finding a memory hole.

<em>public </em><strong>~MemoryManager</strong>()

Releases all memory allocated by this object <strong><em>without leaking memory</em></strong>.

<em>public </em><em>void </em><strong>initialize</strong>(size_t sizeInWords)

Instantiates block of requested size, no larger than 65536 words; cleans up previous block if applicable.

<em>public </em><em>void </em><strong>shutdown</strong>()

Releases memory block acquired during initialization, if any. This should only include memory created for long term use not those that returned such as <em>getList() </em>or <em>getBitmap() </em>as whatever is calling those should delete it instead.

<em>public </em><em>void *</em><strong>allocate</strong>(size_t sizeInBytes)

Allocates a memory using the allocator function. If no memory is available or size is invalid, returns <strong>nullptr</strong>.

<em>public </em><em>void </em><strong>free</strong>(void *address)

Frees the memory block within the memory manager so that it can be reused.

<em>public </em><em>void </em><strong>setAllocator</strong>(std::function&lt;int(int, void *)&gt; allocator)

Changes the allocation algorithm to identifying the memory hole to use for allocation.

<em>public </em><em>int </em><strong>dumpMemoryMap</strong>(char *filename)

Uses standard POSIX calls to write hole list to filename <strong><u>as text</u></strong>, returning <strong>-1 </strong>on error and <strong>0 </strong>if successful.

Format: “[START, LENGTH] – [START, LENGTH] …”, e.g., “<strong>[0, 10] – [12, 2] – [20, 6]</strong>”

<em>public </em><em>void *</em><strong>getList</strong>()

Returns an array of information (<strong><u>in decimal</u></strong>) about holes for use by the allocator function (<em>little-Endian</em>). Offset and length are in <u>words</u>. If no memory has been allocated, the function should return a <strong><em>NULL </em></strong>pointer.

Format: &nbsp;&nbsp; Example: <strong>[3, 0, 10, 12, 2, 20, 6]</strong>

<em>public </em><em>void *</em><strong>getBitmap</strong>()

Returns a bit-stream of bits in terms of an array representing whether words are used (<strong>1</strong>) or free (<strong>0</strong>). The first two bytes are the size of the bitmap (<em>little-Endian</em>); the rest is the bitmap, word-wise.

<strong><em>Note : In the following example B0, B2, and B4 are holes, B1 and B3 are allocated memory.</em></strong>

<strong><em>Hole-0&nbsp;&nbsp;&nbsp; Hole-1&nbsp;&nbsp;&nbsp; Hole-2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ┌─B4─┐&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </em></strong><strong><em>┌ B2┐&nbsp;&nbsp;&nbsp;&nbsp; </em></strong><strong><em>┌───B0 ──┐&nbsp;&nbsp;&nbsp;&nbsp; ┌─Size (4)─┐┌This is Bitmap in Hex┐</em></strong>

<strong><em>Example: </em></strong><strong>[0,10]-[12,2]-[20,6] </strong>[<strong>00000011111100110000000000</strong>] [<strong>0x04</strong>,<strong>0x00,0x00</strong>,<strong>0xCC</strong>,<strong>0x0F</strong>,<strong>0x00</strong>]

<h3>┕<em>─B3─</em>┙ ┕<em>B1</em><sub>┙</sub></h3>
<strong><em>Returned Array: </em></strong>[<strong>0x04</strong>,<strong>0x00,0x00</strong>,<strong>0xCC</strong>,<strong>0x0F</strong>,<strong>0x00</strong>] or [<strong>4</strong>,<strong>0,0</strong>,<strong>204</strong>,<strong>15</strong>,<strong>0</strong>]

<em>public </em><em>unsigned </em><strong>getWordSize</strong>()

Returns the word size used for alignment.

<em>public </em><em>void *</em><strong>getMemoryStart</strong>()

Returns the byte-wise memory address of the beginning of the memory block.

<em>public </em><em>unsigned </em><strong>getMemoryLimit</strong>()

Returns the byte limit of the current memory block.

<strong>Note: The following two functions should not be part of the Memory Manager Class. </strong><u>Memory Allocation Algorithms </u><em>int </em><strong>bestFit</strong>(int sizeInWords, void *list)

Returns <strong>word offset </strong>of hole selected by the best fit memory allocation algorithm, and <strong>-1 </strong>if there is no fit.

<em>int </em><strong>worstFit</strong>(int sizeInWords, void *list)

Returns <strong>word offset </strong>of hole selected by the worst fit memory allocation algorithm, and <strong>-1 </strong>if there is no fit.

<u>Testing</u>

Your code must also compile at the command line and function with provided sample files. These sample files cover a base level functionality for the functions above. <strong><em>It is critical that you test for memory leaks and errors! </em></strong>The code we provide will not test for this. Submissions with memory leaks/errors will be marked <strong><u>zero</u> </strong>for functionality.

<h1>&nbsp;Extra Credit</h1>
In the above implementation of MemoryManager.<strong>initialize</strong>(…), you most likely made use of the <strong>new </strong>operator to acquire your initial block of memory. Your job is to now figure out how to allocate your initial block of memory without the use of <strong>new </strong>or any stdlib functions, e.g. malloc, calloc, etc.

<h1>&nbsp;Submissions</h1>
You will submit the following at the end of this project:

<ul>
<li>Report (<strong>txt</strong>) in man format on Canvas, including link to unlisted screencast video</li>
<li>Compressed tar archive (<strong>tgz</strong>) containing source/build files for text program on Canvas</li>
</ul>
<h2>&nbsp;Report</h2>
Your report will explain how you implemented all your functions and tested them. It will describe how testing was performed, any known bugs, and why the output is correct. The report should be created using <strong>man </strong>format saved as a .txt. The report should be no more than 500 words (about two pages in man format), cover all relevant aspects of the project, and be organized and formatted professionally – <strong><em>this is not a memo!</em></strong>

<h2>&nbsp;Screencast</h2>
Students should submit a screencast (with audio) walking through each class and function. It should include showing/demoing your changes in action (no more than 5 minutes). Audio speed-up is prohibited. Video cannot have watermarks and <u>must be unlisted!</u>

<h2>&nbsp;Compressed Archive (MemoryManager.tgz)</h2>
Your compressed tar file should have the following directory/file structure:

MemoryManager.tgz

MemoryManager.tar

MemoryManager (directory) MemoryManager.h

MemoryManager.cpp

Makefile

(Other source files)

To build your program, we will execute these commands:

<h3>$ tar zxvf MemoryManager.tgz $ cd MemoryManager $ make</h3>
<strong>$ </strong><strong>cd ..</strong>

To link against the library, we will execute this command:

<h3>$ c++ -std=c++17 -o program_name sourcefile.c -L ./MemoryManager -lMemoryManager</h3>
Please test your functions before submission! If your code does not compile it will result in <strong><u>zero credit </u></strong>(0, none, goose-egg) for that portion of the project.

<h1>Helpful Links</h1>
You may find these resources useful as you develop and test your memory manager.

<h2>&nbsp;Development</h2>
<a href="https://www.cs.rit.edu/~ark/lectures/gc/03_00_00.html">https://www.cs.rit.edu/~ark/lectures/gc/03_00_00.html </a><a href="https://www.ibm.com/developerworks/library/pa-dalign/index.html">https://www.ibm.com/developerworks/library/pa-dalign/index.html </a><a href="https://en.cppreference.com/w/cpp/utility/functional/function">https://en.cppreference.com/w/cpp/utility/functional/function</a>

<h2>&nbsp;Testing</h2>
<a href="http://valgrind.org/">http://valgrind.org/ </a><a href="https://github.com/catchorg/Catch2">https://github.com/catchorg/Catch2</a>
