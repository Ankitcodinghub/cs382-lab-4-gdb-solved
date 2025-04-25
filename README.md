# cs382-lab-4-gdb-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/cs382-lab-4-gdb-solved/

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;128071&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS382 Lab 4-GDB Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">
            
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
            5/5 - (4 votes)    </div>
    </div>
&nbsp;

Starting GDB with your program

● Install gdb-multiarch package:

○ sudo apt-get install gdb-multiarch

● Assemble using –g flag and then link

○ aarch64-linux-gnu-as demo.s -g -o demo.o

○ aarch64-linux-gnu-ld demo.o

● Run your program and wait for GDB to connect using the `–g 1234` flag ○ qemu-aarch64 -g 1234 a.out

● On another terminal window, run gdb and connect to the program

○ gdb-multiarch –nh -q a.out -ex ‘set disassemble-next-line on’

-ex ‘target remote :1234’

-ex ‘set solib-search-path /usr/aarch64-linux-gnu-lib/’ -ex ‘layout regs’

Note: You can find these steps in section B.3.2 of the textbook, backslashes in the final command simply denote new lines.

Interacting with GDB

● Please read section B.3.3 in the textbook (p.184)

● Breakpoints

○ Use b &lt;label&gt; to pause the program when it reaches the label

○ Ex: b _start to pause at the start of the program

● Moving through the program

○ Resume execution using continue or c

○ Step through the program using step or s

● Panel focus

○ Use focus regs to view the values of the registers

○ Use focus asm to go back to the assembly code panel

Printing Memory

● Read section B.3.4 in the textbook

● To print data stored in memory we use the following command:

○ x/&lt;length&gt;&lt;format&gt;&lt;unit&gt; address

● If we wanted to print 5 bytes in character from the label hello: ○ x/5cb &amp;hello

● To print 2 bytes in decimal from the address stored in x10:

○ x/2db $x10

Starter Code

Task Time

● Come up for attendance before leaving

● Task 1: Calculating Dot Product

○ Use the data in “vec1” and “vec2” to calculate the dot product and store it in “dot”

○ Must be able to assemble, link, and execute without error

○ You are allowed to use the MUL instruction as needed

○ Comment every line

● Task 2: Debugging using GDB

○ Look at appendix B.3

○ Write a report about your program from Task 1
