# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [Yazeed Osama Binsulih] |
| **Student ID** | [445050301] |
| **University Email** | [445050301]@std.psau.edu.sa |
| **GitHub Username** | [yazid9988] |
| **Repository Link** | [Repository Link](https://github.com/yazid9988/OS-Assignment3-Yazeed-Binsulih/tree/main) |
 
---

## 🎥 Video Link

**Video Link**: [video link](https://drive.google.com/file/d/1sbf5g6erT5AmFWKvDlKsGh4y4Dh-3NqM/view?usp=drivesdk)

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [November 8, 2026, 10:00 PM]
**What I did**: Set up the project in VS Code and added my student ID\.

**Details**:
• Downloaded the project from my GitHub repository and opened it in Visual Studio Code.
• Reviewed the project files and prepared the Java source code for development.
• Updated the student ID in SchedulerSimulationSync.java.
**Challenges**: I did not face any major challenges during this step because importing a GitHub repository into Visual Studio Code was a familiar process from a previous assignment.
**Solution**: I followed the same workflow I had used before to open the repository in Visual Studio Code and prepare the project for development.
**Time spent**: 15 minutes 

---

### Entry 2 - [November 11, 2026, 2:50 PM]
**What I did**: Implemented Feature 1 to protect the ReadyQueue using ReentrantLock.

**Details**:
* Reviewed the ReadyQueue operations and identified the places where multiple CPU threads could access the shared queue.
* Added a ReentrantLock to protect access to the ReadyQueue.
**Challenges**: The main challenge was understanding how multiple CPU threads could access the ReadyQueue simultaneously and how this could lead to race conditions or inconsistent queue data.

**Solution**: I reviewed the ReadyQueue methods and protected the shared operations using ReentrantLock. I used try/finally to make sure that the lock was released correctly after each protected operation.

**Time spent**: 45 minutes 

---

### Entry 3 - [November 12,2026, 12:15 PM]
**What I did**: Implemented Feature 2 to protect the shared statistics counters.

**Details**:
* Identified the shared counters used by the CPU threads.
* Added ReentrantLock objects to protect access to the shared counters.
* Protected both reading and updating operations.

**Challenges**: The main challenge was ensuring that multiple threads could not read or update the shared counters in an unsafe way.

**Solution**: I used separate locks for the shared counters and protected the operations that read or update them. I also used try/finally blocks to ensure proper lock release and maintain consistent statistics.

**Time spent**: 30 minutes 

---

### Entry 4 - [November 12,2026, 4:40 PM]
**What I did**: Implemented Feature 3 to replace Busy Waiting with a Counting Semaphore.

**Details**:
* Imported the Java Semaphore class.
* Created a counting semaphore initialized with zero.
* Added release() when a process is added to the ReadyQueue.
* Used acquire() to make CPU threads wait when no process is available.
* Removed the previous busy-waiting mechanism that repeatedly checked whether the queue contained a process.

**Challenges**: The main challenge was understanding how the counting semaphore should coordinate the available processes and CPU threads. Another challenge was handling the shutdown mechanism correctly, because CPU threads waiting on acquire() needed to wake up and terminate when all processes were completed.

**Solution**: I used a counting semaphore initialized to zero. Each new process releases a permit, allowing a waiting CPU thread to continue.

**Time spent**: 50 minutes 

---

### Entry 5 - [November 13, 2026, 10:00 PM]
**What I did**: Tested the program and checked the final verification results.

**Details**:
• Ran the program in Visual Studio Code.
• Reviewed the process summary and the Verification Block.
• Checked the expected and observed values for context switches, completed processes, and total service time.
• Checked that the busy-waiting polls value was zero.
• Reviewed the output to make sure that all verification checks passed.

**Challenges**: The main challenge was ensuring that the three synchronization features worked correctly together and that the program produced consistent results\. I also needed to verify that the synchronization changes did not introduce new concurrency problems.

**Solution**: I examined the program output and compared the expected values with the observed values in the Verification Block. I also reviewed the process summary and checked the busy-waiting polls to confirm that the program behaved as expected.

**Time spent**: 35 minutes 

---

### Entry 6 - [November 14, 2026, 11:00 AM]
**What I did**: Recorded the project demonstration video and prepared the final documentation.

**Details**:
* Prepared a demonstration explaining the main parts of the project.
* Recorded the program execution and displayed the final output.
* Explained the three implemented synchronization features.
* Showed the final verification results.
* Prepared the video link to include in MY_WORK.md.

**Challenges**: The main challenge was organizing the demonstration to explain the implementation clearly while showing the actual program execution and final results within the required video duration.

**Solution**: I organised the demonstration into clear sections, starting with the project overview, followed by the three implemented features, the program execution, and the final verification results.

**Time spent**: 30 minutes 

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [3 hours]

**Most challenging part**: implementing thread synchronization correctly. Understanding how multiple CPU threads access shared resources and ensuring that they do not interfere with each other required careful attention. Using locks and semaphores helped me understand how synchronization prevents race conditions and maintains data consistency.

**Most interesting learning**: how synchronization mechanisms work in real multithreaded programs. I learned the difference between using locks to protect shared data and using semaphores to control thread coordination. This assignment helped me connect the theoretical concepts from the Operating Systems course with practical Java programming.

**What I would do differently next time**: If I worked on this assignment again, I would spend more time planning the program structure before starting the implementation. I would also test each synchronization feature separately before combining everything into one program. This would make debugging easier, help me identify problems earlier, and improve the overall code quality.

---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

Question 1: What did you learn about synchronization?

I learned that race conditions can cause incorrect results when multiple threads access and modify shared data at the same time. Before this assignment, I did not fully understand how easily one thread could overwrite another thread’s update. I also learned that synchronization tools such as locks can protect shared resources. The most important lesson was that a program may appear to work correctly in some runs but still contain synchronization problems. Testing the program multiple times helped me understand the importance of reliable synchronization.

Question 2: What was the most challenging part of this assignment?

The most challenging part was identifying where synchronization was needed and choosing the correct synchronization mechanism for each shared resource. I had to understand how CPU threads interact with the ready queue and shared counters. Another challenge was replacing busy waiting with a semaphore without causing threads to remain blocked. I solved these problems by reviewing the code, understanding the role of each lock and semaphore, and testing the program after making changes. This helped me become more confident in debugging multithreaded programs.

Question 3: How did you overcome the challenges you faced?
I overcame the challenges by studying the starter code and understanding how the CPU threads interact with shared resources. I identified the critical sections and used separate locks to protect shared data. I also replaced busy waiting with a counting semaphore so that CPU threads could wait efficiently for available processes. When I faced problems, I reviewed the synchronization logic and checked how the threads behaved. Finally, I tested the program multiple times to make sure the final results were correct and consistent.

Question 4: Where can synchronization concepts be applied in real-world applications?
Synchronization concepts are used in many real-world applications where multiple threads or processes access shared resources. For example, banking systems use synchronization to prevent incorrect account balances when multiple transactions happen simultaneously. Online booking systems use it to prevent multiple customers from reserving the same seat. Databases use synchronization to maintain data consistency when several users access or update records. These concepts are essential for building reliable applications that handle concurrent operations safely.
## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

[The most challenging part of this assignment was implementing the counting semaphore and understanding how CPU threads should coordinate with the ready queue. At first, I found it difficult to understand how the semaphore controls the availability of processes. Choosing the correct initial value was also important because it had to represent the number of available processes. Another challenge was handling the shutdown mechanism when all processes were completed. I had to understand why CPU threads waiting inside acquire() needed to be released before the program could terminate. This part required careful attention because an incorrect implementation could cause threads to wait indefinitely.]

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

[I overcame these challenges by dividing the assignment into smaller features and working on each one separately. I reviewed the assignment instructions and studied the relevant synchronization concepts from the course materials. I also examined the existing Java code to understand how the ReadyQueue, SharedStats, and CpuWorker classes interact. When I faced difficulties, I reviewed the methods and conditions carefully to understand how the threads communicate with each other. I tested the changes by running the program and examining its console output. I also sought guidance to improve my understanding of the code and the purpose of each synchronization mechanism.]

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

[Synchronization is widely used in real-world applications where multiple users or processes access shared resources. For example, banking systems use synchronization to prevent two transactions from incorrectly modifying the same account balance at the same time. Online booking systems use similar mechanisms to prevent multiple customers from reserving the same seat. Database management systems also use locks to maintain data consistency when several transactions access shared records. Operating systems use synchronization to coordinate processes and manage shared resources safely. These examples helped me understand that the concepts I implemented in this assignment are important in many practical software systems.]

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

[The original program failed the verification checks because of race conditions and busy waiting. The observed values did not match the expected values: context switches were 27 instead of 23, completed processes were 13 instead of 12, and total service time was 81680 ms instead of 55853 ms. For example, CPU-1 reads contextSwitchCount = 12, then CPU-2 reads the same value before CPU-1 updates it. CPU-1 writes 13, and CPU-2 also writes 13, so one increment is lost instead of reaching 14. This can happen on a real machine without RaceWindow.pause() because thread execution can be interrupted and interleaved, and it is difficult to detect because it depends on timing and may not happen in every run.]

Verification block of the **original starter**:
```
[═══ VERIFICATION (expected values are computed from YOUR seed) ═══
Context switches (quanta executed)  expected 23  observed 27  ✘ MISMATCH
Completed processes                 expected 12  observed 13  ✘ MISMATCH
Total service time (ms)             expected 55853 observed 81680  ✘ MISMATCH
Busy-waiting polls (must be 0)       expected 0  observed 153  ✘ MISMATCH
✘ At least one check failed (see the ✘ lines above): a race condition or busy waiting is still present.]
```

Verification block of **my final version**:
```
[═══ VERIFICATION (expected values are computed from YOUR seed) ═══
Context switches (quanta executed)  expected 23  observed 23  ✔
Completed processes                 expected 12  observed 12  ✔
Total service time (ms)             expected 55853  observed 55853  ✔
Busy-waiting polls (must be 0)       expected 0  observed 0  ✔
All shared values are consistent.]
```

**Explanation of the timeline:**
[CPU-1 reads contextSwitchCount = 12, then CPU-2 reads the same value before CPU-1 updates it. CPU-1 writes 13, and CPU-2 also writes 13, so one increment is lost instead of reaching 14. This can also happen on a real machine without RaceWindow.pause() because thread execution can be interrupted and interleaved at any time. It is difficult to detect because the problem depends on timing and may not occur in every execution.]

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

[I used one separate ReentrantLock for each of the three statistics: contextLock, completedLock, and serviceLock. This allows independent statistics to be updated concurrently without blocking each other, although it requires managing more locks. The ready queue uses its own lock because it protects different shared data (list and map), and separating it avoids unnecessary contention between queue operations and statistics updates. The locks provide mutual exclusion by allowing only one thread at a time to enter each protected critical section, and the finally blocks ensure that locks are released. This supports progress, but the default ReentrantLock is not fair, so a waiting thread is not guaranteed to acquire the lock within a bounded time and could experience long waiting.]

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| [e.g., `ReadyQueue.poll()`] | [lock name] | [reason] |
| [contextSwitchCount – incrementContextSwitch() / getContextSwitchCount()] | [contextLock] | [Prevents lost updates and protects reading the counter.] |
| [completedProcessCount – incrementCompletedProcess() / getCompletedProcessCount()] | [completedLock] | [Prevents lost updates when multiple processes finish.] |
| [totalServiceTime – addServiceTime() / getTotalServiceTime()] | [serviceLock] | [Prevents incorrect updates to the shared total.] |
| [ReadyQueue.add()] | [lock] | [Protects adding processes to the shared queue and map.] |
| [ReadyQueue.poll()] | [lock] | [Prevents multiple CPUs from removing the same process.] |
| [ReadyQueue.processOf()] | [lock] | [Protects access to the shared map.] |
| [ReadyQueue.snapshot()] | [lock] | [Protects reading the queue and map consistently.] |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

[In the starter version, CPUs repeatedly checked the ready queue when it was empty, causing busy waiting and wasting CPU time. In my starter run, the number of busy-waiting polls was 153. In the final version, I used a counting semaphore initialized to 0 because no processes were available initially; its value represents the number of available processes, and after the initial numProcesses add calls, its value becomes 12. When the queue is empty, a CPU blocks in acquire() instead of continuously checking the queue. At the end, the last CPU calls release(totalCPUs) to wake all waiting CPUs so they can terminate; otherwise, they could remain blocked forever.]

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
[The classical problem is the Producer–Consumer Problem. The main thread acts as a producer when it adds initial processes, and CPU threads act as consumers when they remove processes from the ready queue. CPUs can also act as producers when they re-enqueue unfinished processes.]

**Semaphores for a bounded queue (name and initial value)**:
[* empty = K: represents the available slots in the queue.
* full = 0: represents the occupied slots in the queue.
* mutex = 1: ensures mutual exclusion when accessing the queue.]

**Deadlock scenario and prevention**:
[A deadlock can occur if a producer acquires the mutex before waiting for an empty slot. If the queue is full, the producer holds the mutex while waiting, and a consumer cannot acquire the mutex to remove an item and create a free slot. This violates the hold-and-wait condition. To prevent deadlock, wait for an empty slot before acquiring the mutex, and release the mutex before waiting for another semaphore.]

## Summary

**Key concepts I understood through these questions:**
1. Race conditions and how synchronization prevents lost updates when multiple threads access shared variables.
2. The use of separate locks to protect critical sections and provide mutual exclusion.
3. The difference between busy waiting and semaphores, and how the Producer–Consumer problem relates to process scheduling.

**Concepts I need to study more:**
1. Deadlock conditions and different ways to prevent deadlocks.
2. Semaphore behavior, lock fairness, and bounded waiting.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [ ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [ ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [ ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [ ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [ ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [ ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [ ] **The four verification lines are ✔ in 5 consecutive runs**
- [ ] Every lock is released in a `finally` block
- [ ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [ ] Each feature has clear comments

**Commits**
- [ ] **At least 4 meaningful commits, ideally 7 or more**
- [ ] **One commit per feature**
- [ ] Commits are spread over **different dates** (not all in the last hour)
- [ ] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ ] Full name and student ID filled in at the top
- [ ] Development log has **5+ entries** on different dates
- [ ] Reflection: 4 questions, 5-7 sentences each
- [ ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [ ] No `[...]` placeholders left
- [ ] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
