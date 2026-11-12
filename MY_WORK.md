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
| **Full Name** | [Mayasah Waleed Alghamdi] |
| **Student ID** | [446052172] |
| **University Email** | [446052172]@std.psau.edu.sa |
| **GitHub Username** | [Mayasah172] |
| **Repository Link** | [(https://github.com/Mayasah172/OS-Assignment3-mayasah-alghamdi)] |
 
---

## 🎥 Video Link

**Video Link**: [https://drive.google.com/file/d/1wfuV9rlwcqkeHa0y31dryDlM1X75JmZn/view?usp=drivesdk]

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

### Entry 1 - [ November 7, 2026]
**What I did**:
Set my student ID 
**Details**:
Added my student ID to the Java code.
**Challenges**:
NO Challenge HERE
**Solution**:
NO Challenge HERE
**Time spent**:
1h
---

### Entry 2 - [November 7, 2026]
**What I did**:
implemented Feature 1.

**Details**:
Protected the Ready Queue using a ReentrantLock.
Used try/finally to ensure the lock is always released.

**Challenges**:
Understanding how to protect the Ready Queue from simultaneous access.
**Solution**:
Used a lock around the queue operations to ensure that only one thread accesses the critical section at a time.
**Time spent**:
 1 h
---

### Entry 3 - [November 7, 2026]
**What I did**:
Implemented Feature 2.
**Details**:
Added separate locks for the shared statistics counters.
Protected the context switch counter.
Protected the completed process counter.
Protected the total service time counter.
Ensured that both reading and updating the counters are protected
**Challenges**:
Understanding how to protect each shared counter independently.
**Solution**:
 Used a separate lock for each counter to protect its updates and reads.
 **Time spent**:
1;30 h
---

### Entry 4 - [November 8, 2026]
**What I did**:
 Implemented Feature 3 With Replaced busy waiting with a Counting Semaphore
**Details**:
Added a Counting Semaphore with an initial value of 0.
Used release() when a process was added to the Ready Queue.
Used acquire() to make CPU threads wait when no process was available.
Added release(totalCPUs) to wake up CPU threads during shutdown.
**Challenges**:
 Understanding how acquire() and release() work together.
 **Solution**:
 Reviewed the semaphore logic and tested the program to check that CPU threads waited correctly and the verification results passed.
 **Time spent**:
1;30 h

---

### Entry 5 -[November 11, 2026]
**What I did**:
Made an update to Feature 3.
**Details**:
Removed the unnecessary null-check branch as required by the README.
Kept the Semaphore implementation.
Ran the program and checked the verification results
**Challenges**:
 Making sure the update did not affect the synchronization.
**Solution**:
Ran the program again and checked that the verification results were successful.

**Time spent**:
1 h
---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: 1 day

**Most challenging part**:
Understanding how multiple CPUs access the shared Ready Queue safely.
**Most interesting learning**:
Learning how a Counting Semaphore prevents busy waiting.
**What I would do differently next time**:
I would read the README carefully before starting and test each feature after implementing it.
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

I learned that synchronization is important when multiple threads access shared data. Without synchronization, race conditions can happen and cause incorrect results. I learned how to use ReentrantLock to protect critical sections in the Ready Queue. I also learned how separate locks can protect shared statistics counters. In Feature 3, I used a Counting Semaphore to make CPU threads wait until a process becomes available. This assignment helped me understand how synchronization improves the correctness of a multithreaded program.
## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

The most challenging part was implementing Feature 3 using a Counting Semaphore. At first, understanding how acquire() and release() work together was difficult. I needed to understand when a CPU should wait and when it should continue processing. I also had to understand how to wake up the CPU threads when all processes were completed. This part required careful attention because an incorrect implementation could cause threads to wait forever. After understanding the logic, I was able to implement and test the feature.

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

I overcame the challenges by reviewing the assignment instructions and understanding the purpose of each feature. I studied how locks and semaphores work before applying them to the code. I implemented the features step by step instead of changing everything at once. After making changes, I ran the program to check the verification results. When I updated Feature 3, I tested the program again to make sure the synchronization still worked correctly. This process helped me understand the code better and identify possible mistakes.
## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

Synchronization is used in many real-world applications, such as banking systems. For example, two users may try to access or update the same bank account at the same time. Without synchronization, the account balance could become incorrect. Locks can protect the account data while a transaction is being processed. Semaphores can also control access to a limited number of resources. This shows why synchronization is important for preventing conflicts and keeping systems reliable.
### Optional: What would you like to learn more about?

I would like to learn more about deadlocks and how to prevent them. I am also interested in understanding how semaphores work in larger systems. I want to practice more examples involving multiple threads and shared resources.
### Optional: How confident do you feel about synchronization concepts now?

Intermediate. I understand the basic concepts of race conditions, critical sections, locks, and semaphores. I can explain how locks protect shared data and how a semaphore controls thread execution. However, I still need more practice with complex synchronization problems and deadlock prevention.
### Optional: Feedback on the assignment

The assignment was useful because it helped me apply synchronization concepts in Java. I learned how race conditions affect program results and how locks can solve these problems. I also understood the importance of using semaphores instead of busy waiting. The practical implementation helped me connect the theoretical concepts to real code.
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
The original program had a race condition because multiple CPU threads could update the same shared counter at the same time. For example, CPU-1 reads contextSwitchCount = 12, then pauses at RaceWindow.pause(). CPU-2 also reads 12 and pauses before writing. CPU-1 writes 13, then CPU-2 writes 13, so one increment is lost and the correct value should be 14. In my original output, context switches were 24 instead of 26, completed processes were 10 instead of 12, and total service time was 88593 instead of 93196. The same bug can happen on a real machine because shared-variable updates are not always atomic, and it is difficult to detect because it depends on thread timing.

Verification block of the **original starter**:
```
 WATCHDOG: the simulation did not finish (33 s). A process was lost, or a CPU is blocked forever, or the 'completed' counter lost an update.

═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected ٢٦       observed ٢٤       ✘ MISMATCH
  Completed processes                    expected ١٢       observed ١٠       ✘ MISMATCH
  Total service time (ms)                expected ٩٣١٩٦    observed ٨٨٥٩٣    ✘ MISMATCH
  Busy-waiting polls (must be 0)         expected ٠        observed ٦٠٩      ✘ MISMATCH
  ✘ At least one check failed (see the ✘ lines above): a race condition or busy waiting is still present.

═══ Process Summary Table (nominal ms) ═══
Process   Priority  Burst       Waiting       Turnaround   
──────────────────────────────────────────────────────────
P1        ٧         ١٠١٩٨       ٧٨٧٤٧         ٨٨٩٤٥        
P2        ١         ٤٢٢٧        ٠             ٠            
P3        ٧         ١٠٠٨٨       ٧٩٢٣٢         ٨٩٣٢٠        
P4        ٦         ٥٢٧٧        ٦٠٧٧٨         ٦٦٠٥٥        
P5        ١         ١٢٠٠٠       ٧٩٥٦٥         ٩١٥٦٥        
P6        ٩         ١٠٣٧٦       ٠             ٠            
P7        ٦         ٥٤٣٠        ٧١١٨٥         ٧٦٦١٥        
P8        ٦         ٥٦٥٧        ٧١٦٦٣         ٧٧٣٢٠        
P9        ٥         ٦٥١٧        ٧٢٤٢٣         ٧٨٩٤٠        
P10       ٦         ٩٩٢٠        ٧٤٣٧٥         ٨٤٢٩٥        
P11       ٣         ٤٧٤٨        ٤٥٧٣٧         ٥٠٤٨٥        
P12       ٨         ٨٧٥٨        ٧٩٦٨٢         ٨٨٤٤٠        

```

Verification block of **my final version**:
```
VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected ٢٦       observed ٢٦       ✔
  Completed processes                    expected ١٢       observed ١٢       ✔
  Total service time (ms)                expected ٩٣١٩٦    observed ٩٣١٩٦    ✔
  Busy-waiting polls (must be 0)         expected ٠        observed ٠        ✔
  ✔ All shared values are consistent.

═══ Process Summary Table (nominal ms) ═══
Process   Priority  Burst       Waiting       Turnaround   
──────────────────────────────────────────────────────────
P1        ٧         ١٠١٩٨       ١٩٨٤٢         ٣٠٠٤٠        
P2        ١         ٤٢٢٧        ٢١٣           ٤٤٤٠         
P3        ٧         ١٠٠٨٨       ١٩٦٨٧         ٢٩٧٧٥        
P4        ٦         ٥٢٧٧        ١٥٤٢٨         ٢٠٧٠٥        
P5        ١         ١٢٠٠٠       ٢٠٠٥٠         ٣٢٠٥٠        
P6        ٩         ١٠٣٧٦       ٢١١٤٩         ٣١٥٢٥        
P7        ٦         ٥٤٣٠        ٢٠٢٣٠         ٢٥٦٦٠        
P8        ٦         ٥٦٥٧        ٢٠٧١٣         ٢٦٣٧٠        
P9        ٥         ٦٥١٧        ٢٠٧٨٣         ٢٧٣٠٠        
P10       ٦         ٩٩٢٠        ٢١٤٣٠         ٣١٣٥٠        
P11       ٣         ٤٧٤٨        ١٥٣٨٢         ٢٠١٣٠        
P12       ٨         ٨٧٥٨        ٢٢٣٤٢         ٣١١٠٠        
```


## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

I used one ReentrantLock for the Ready Queue and a separate lock for each statistics counter. Separate locks allow independent counters to be updated without blocking each other, but they require managing more locks. The Ready Queue has a different lock because it protects different shared data. The locks provide mutual exclusion, and using try/finally ensures that they are released. The default ReentrantLock is not fair, so bounded waiting is not guaranteed.

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| ReadyQueue.add() | lock  |Protects adding processes to the queue and updating the map. |
| ReadyQueue.poll() | lock  | Prevents multiple CPUs from removing the same process. |
| ReadyQueue.processOf() | lock  | Protects access to the process map |
| ReadyQueue.snapshot() | lock  | Protects reading the queue state. |
|Context switch counter| contextSwitchLock  |Prevents lost updates. |
| Completed process counter | completedProcessLock | Protects the shared counter |
| Total service time counter| serviceTimeLock | Protects the shared service time value. |



## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

In the original program, CPUs used busy waiting by repeatedly checking the Ready Queue when no process was available. My original output showed 609 busy-waiting polls, while the required value was zero. In the final program, a Counting Semaphore makes CPU threads wait until a process becomes available. The Semaphore starts at zero because the queue initially has no available processes, and after the initial numProcesses calls to add(), its value equals numProcesses. The last CPU calls release(totalCPUs) to wake up blocked CPUs so they can shut down; otherwise, some CPUs could remain blocked forever.

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
the classical problem is the Producer-Consumer problem. The main thread acts as a producer, while CPU threads act as consumers; CPUs can also act as producers when they re-enqueue unfinished processes.

**Semaphores for a bounded queue (name and initial value)**:
The three semaphores are empty = K, full = 0, and mutex = 1.

**Deadlock scenario and prevention**:
Deadlock can happen if a producer holds the mutex while waiting for an empty slot, preventing the consumer from removing an item To prevent this, we break the hold-and-wait condition by waiting for an empty slot before acquiring the mutex.
## Summary

**Key concepts I understood through these questions:**
1.I understood how race conditions happen when multiple threads access shared data at the same time.
2.I learned how ReentrantLock protects critical sections and prevents lost updates.
3.I understood how Counting Semaphores prevent busy waiting and coordinate CPU threads.

**Concepts I need to study more:**
1.Deadlock conditions and how to prevent them.
2.The Producer-Consumer problem and bounded-buffer synchronization.

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
