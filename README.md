# UCSDx - ALGS201x
My solutions to University of California San Diego's Data Structure Fundamentals' programming assignments

## Programming Assingments

### 1. [Check brackets in code](https://github.com/KennethSee/UCSDx---ALGS201x/blob/master/check_brackets.py)

#### Problem Introduction
In this problem you will implement a feature for a text editor to find errors in the usage of brackets in the code.

#### Problem Description
**Task.** Your friend is making a text editor for programmers. He is currently working on a feature that will find errors in the usage of different types of brackets. Code can contain any brackets from the set []{}(), where the opening brackets are [,{, and ( and the closing brackets corresponding to them are ],}, and ).
For convenience, the text editor should not only inform the user that there is an error in the usage of brackets, but also point to the exact place in the code with the problematic bracket. First priority is to find the first unmatched closing bracket which either doesn’t have an opening bracket before it, like ] in ](), or closes the wrong opening bracket, like } in ()[}. If there are no such mistakes, then it should find the first unmatched opening bracket without the corresponding closing bracket after it, like ( in {}([]. If there are no mistakes, text editor should inform the user that the usage of brackets is correct.

Apart from the brackets, code can contain big and small latin letters, digits and punctuation marks. More formally, all brackets in the code should be divided into pairs of matching brackets, such that in each pair the opening bracket goes before the closing bracket, and for any two pairs of brackets either one of them is nested inside another one as in (foo[bar]) or they are separate as in f(a,b)-g[c]. The bracket [ corresponds to the bracket ], { corresponds to }, and ( corresponds to ).

**Input Format.** Input contains one string 𝑆 which consists of big and small latin letters, digits, punctuation marks and brackets from the set []{}(). Constraints. The length of 𝑆 is at least 1 and at most 105.

**Output Format.** If the code in 𝑆 uses brackets correctly, output “Success" (without the quotes). Otherwise, output the 1-based index of the first unmatched closing bracket, and if there are no unmatched closing brackets, output the 1-based index of the first unmatched opening bracket.

**Memory Limit.** 512MB

### 2. [Compute tree height](https://github.com/KennethSee/UCSDx---ALGS201x/blob/master/tree_height.py)

#### Problem Introduction
Trees are used to manipulate hierarchical data such as hierarchy of categories of a retailer or the directory structure on your computer. They are also used in data analysis and machine learning both for hierarchical clustering and building complex predictive models, including some of the best-performing in practice algorithms like Gradient Boosting over Decision Trees and Random Forests. In the later modules of this course, we will introduce balanced binary search trees (BST) — a special kind of trees that allows to very efficiently store, manipulate and retrieve data. Balanced BSTs are thus used in databases for efficient storage and actually in virtually any non-trivial programs, typically via built-in data structures of the programming language at hand.

In this problem, your goal is to get used to trees. You will need to read a description of a tree from the input, implement the tree data structure, store the tree and compute its height.

#### Problem Description
**Task.** You are given a description of a rooted tree. Your task is to compute and output its height. Recall that the height of a (rooted) tree is the maximum depth of a node, or the maximum distance from a leaf to the root. You are given an arbitrary tree, not necessarily a binary tree.

**Input Format.** The first line contains the number of nodes 𝑛. The second line contains 𝑛 integer numbers from −1 to 𝑛 − 1 — parents of nodes. If the 𝑖-th one of them (0 ≤ 𝑖 ≤ 𝑛 − 1) is −1, node 𝑖 is the root, otherwise it’s 0-based index of the parent of 𝑖-th node. It is guaranteed that there is exactly one root. It is guaranteed that the input represents a tree. Constraints. 1 ≤ 𝑛 ≤ 105.

**Output Format.** Output the height of the tree.

**Memory Limit.** 512MB

### 3. [Convert array into heap](https://github.com/KennethSee/UCSDx---ALGS201x/blob/master/build_heap.py)

#### Problem Introduction
In this problem you will convert an array of integers into a heap. This is the crucial step of the sorting algorithm called HeapSort. It has guaranteed worst-case running time of 𝑂(𝑛 log 𝑛) as opposed to QuickSort’s average running time of 𝑂(𝑛 log 𝑛). QuickSort is usually used in practice, because typically it is faster, but HeapSort is used for external sort when you need to sort huge files that don’t fit into memory of your computer.

#### Problem Description
**Task.** The first step of the HeapSort algorithm is to create a heap from the array you want to sort. By the way, did you know that algorithms based on Heaps are widely used for external sort, when you need to sort huge files that don’t fit into memory of a computer?
Your task is to implement this first step and convert a given array of integers into a heap. You will do that by applying a certain number of swaps to the array. Swap is an operation which exchanges elements 𝑎𝑖 and 𝑎𝑗 of the array 𝑎 for some 𝑖 and 𝑗. You will need to convert the array into a heap using only 𝑂(𝑛) swaps, as was described in the lectures. Note that you will need to use a min-heap instead of a max-heap in this problem.

**Input Format.** The first line of the input contains single integer 𝑛. The next line contains 𝑛 space-separated integers 𝑎𝑖.

**Constraints.** 1 ≤ 𝑛 ≤ 100 000; 0 ≤ 𝑖, 𝑗 ≤ 𝑛 − 1; 0 ≤ 𝑎0, 𝑎1, . . . , 𝑎𝑛−1 ≤ 109. All 𝑎𝑖 are distinct.

**Output Format.** The first line of the output should contain single integer 𝑚 — the total number of swaps. 𝑚 must satisfy conditions 0 ≤ 𝑚 ≤ 4𝑛. The next 𝑚 lines should contain the swap operations used to convert the array 𝑎 into a heap. Each swap is described by a pair of integers 𝑖, 𝑗 — the 0-based indices of the elements to be swapped. After applying all the swaps in the specified order the array must become a heap, that is, for each 𝑖 where 0 ≤ 𝑖 ≤ 𝑛 − 1 the following conditions must be true:

1. If 2𝑖 + 1 ≤ 𝑛 − 1, then 𝑎𝑖 < 𝑎2𝑖+1.
2. If 2𝑖 + 2 ≤ 𝑛 − 1, then 𝑎𝑖 < 𝑎2𝑖+2.

Note that all the elements of the input array are distinct. Note that any sequence of swaps that has length at most 4𝑛 and after which your initial array becomes a correct heap will be graded as correct.

**Memory Limit.** 512MB.

### 4. [Parallel processing](https://github.com/KennethSee/UCSDx---ALGS201x/blob/master/job_queue.py)

#### Problem Introduction
In this problem you will simulate a program that processes a list of jobs in parallel. Operating systems such as Linux, MacOS or Windows all have special programs in them called schedulers which do exactly this with the programs on your computer.

#### Problem Description
**Task.** You have a program which is parallelized and uses 𝑛 independent threads to process the given list of 𝑚 jobs. Threads take jobs in the order they are given in the input. If there is a free thread, it immediately takes the next job from the list. If a thread has started processing a job, it doesn’t interrupt or stop until it finishes processing the job. If several threads try to take jobs from the list simultaneously, the thread with smaller index takes the job. For each job you know exactly how long will it take any thread to process this job, and this time is the same for all the threads. You need to determine for each job which thread will process it and when will it start processing.

**Input Format.** The first line of the input contains integers 𝑛 and 𝑚. The second line contains 𝑚 integers 𝑡𝑖 — the times in seconds it takes any thread to process 𝑖-th job. The times are given in the same order as they are in the list from which threads take jobs. Threads are indexed starting from 0.

**Constraints.** 1 ≤ 𝑛 ≤ 105; 1 ≤ 𝑚 ≤ 105; 0 ≤ 𝑡𝑖 ≤ 109.

**Output Format.** Output exactly 𝑚 lines. 𝑖-th line (0-based index is used) should contain two spaceseparated integers — the 0-based index of the thread which will process the 𝑖-th job and the time in seconds when it will start processing that job.

**Memory Limit.** 512MB.

### 4. [Phone Book](https://github.com/KennethSee/UCSDx---ALGS201x/blob/master/phone_book.py)

#### Problem Introduction
In this problem you will implement a simple phone book manager.

#### Problem Description
**Task.** In this task your goal is to implement a simple phone book manager. It should be able to process the following types of user’s queries:
∙ *add number name*. It means that the user adds a person with name name and phone number number to the phone book. If there exists a user with such number already, then your manager has to overwrite the corresponding name.
∙ *del number*. It means that the manager should erase a person with number number from the phone book. If there is no such person, then it should just ignore the query.
∙ *find number*. It means that the user looks for a person with phone number number. The manager should reply with the appropriate name, or with string “not found" (without quotes) if there is no such person in the book.

**Input Format.** There is a single integer 𝑁 in the first line — the number of queries. It’s followed by 𝑁 lines, each of them contains one query in the format described above.

**Constraints.** 1 ≤ 𝑁 ≤ 10<sup>5</sup>. All phone numbers consist of decimal digits, they don’t have leading zeros, and each of them has no more than 7 digits. All names are non-empty strings of latin letters, and each of them has length at most 15. It’s guaranteed that there is no person with name “not found".

**Output Format.** Print the result of each find query — the name corresponding to the phone number or “not found" (without quotes) if there is no person in the phone book with such phone number. Output one result per line in the same order as the find queries are given in the input.

**Memory Limit.** 512MB.

### 5. [Hashing with chains]()

#### Problem Introduction
In this problem you will implement a hash table using the chaining scheme. Chaining is one of the most popular ways of implementing hash tables in practice. The hash table you will implement can be used to implement a phone book on your phone or to store the password table of your computer or web service (but don’t forget to store hashes of passwords instead of the passwords themselves, or you will get hacked!).

#### Problem Description
**Task.** In this task your goal is to implement a hash table with lists chaining. You are already given the number of buckets 𝑚 and the hash function. It is a polynomial hash function
<br>![alt text](https://imgur.com/3QPBxvj)<br>
where 𝑆[𝑖] is the ASCII code of the 𝑖-th symbol of 𝑆, 𝑝 = 1 000 000 007 and 𝑥 = 263. Your program should support the following kinds of queries:
∙ *add string* — insert string into the table. If there is already such string in the hash table, then just ignore the query.
∙ *del string* — remove string from the table. If there is no such string in the hash table, then just ignore the query.
∙ *find string* — output “yes" or “no" (without quotes) depending on whether the table contains string or not.
∙ *check 𝑖* — output the content of the 𝑖-th list in the table. Use spaces to separate the elements of the list. If 𝑖-th list is empty, output a blank line.

When inserting a new string into a hash chain, you must insert it in the beginning of the chain. Input Format. There is a single integer 𝑚 in the first line — the number of buckets you should have. The next line contains the number of queries 𝑁. It’s followed by 𝑁 lines, each of them contains one query in the format described above.

**Constraints.** 1 ≤ 𝑁 ≤ 10<sub>5</sub>; 𝑁/5 ≤ 𝑚 ≤ 𝑁. All the strings consist of latin letters. Each of them is non-empty and has length at most 15.

**Output Format.** Print the result of each of the find and check queries, one result per line, in the same order as these queries are given in the input.

**Memory Limit.** 512MB.
