## General Advice from UB Alumni

#### Good Luck!

#### Start Early
I do not care how well you have done in other courses, or how much better you perform under pressure. If you do not start these assignments as soon as they are released you are highly unlikely to finish them. If you want to succeed and do well in this course it is crucial that you start as soon as possible. Think about it like this, the sooner you get the assignments done, the sooner you will be able to watch netflix and spend time outside drinking celebratory beers.

#### Do the code reading questions 
They will help you get familiar with the resources that you will need to complete each assignment. They are a great introduction to the code base that you will be using thorughout the semester.

#### Design
So much of these assignments, especially ASST2 and ASST3, is based on your design. You need to slow down. Spend a few days on the white board figuring out how you will make the whole assignment work end to end. It is nearly impossible to complete these assignments just hacking for a few nights

#### Go to office hours!
Geoff has one of the best sets of TAs at UB take advantage of them. Go to them early, before the last minute rush Friday at 5pm. This is when they will have time to review your design and sit down and help you debug.

#### Choose your partner wisely
I strongly suggest **NOT** choosing a close friend or roommate as your ops partner. This course is a huge commitment and it is important to keep the relationship professional so that work is getting done and both partners are happy.

If you chose to ignore this, which I am sure many will, I suggest that you make sure that you and your partner can work both inside and outside of the academic world and have similar interests in mind. If you are having problems with your partner, let them know right away that you have a problem. Be constructive and most importantly, be honest. In the event that you are still having trouble with your partner, go to Geoff. He will let you know what action to take going forward.

#### Having trouble where to start?
In the event that this assignment requires you to create and maintain data structures this is the perfect place to start. Construct your data structures and make sure that they are working correctly (maybe with a few test cases) before you start allow your kernel to use them. This seems like common sense but most people forget how easy some of these things can be to do when they are stuck. This practice will have you writing cleaner code with far less bugs.

-------------------------------------------------------------------------------

## ASST 1 | Synchronization Primitives
- Welcome to OS161
- Not sure how much help to give people here, its pretty simple
- `kern/thread/synch.c` and `kern/synchprobs/*` are the main files you will be looking at. `kern/thread/thread.c` is important to look at for a better understanding of the `thread` structure.
- The slides are your friend for this assignment.

#### Locks
- `lock_do_i_hold()` is a private method, it is only to be used by the lock interface.
- Should be very similar to the `semaphore` implementation.

#### CV
- Be very careful with the lock that gets past into `cv_signal)()` `cv_wait()` `cv_broadcast()` if you are putting a thread to sleep, make sure you are not holding the lock.

#### Reader-Writer Locks
- you want to put a priority on writers, that is, if there is a writer thread waiting, no more readers should be allowed access to the `rwlock`. once all readers are done in the critical section, signal a writer into the critical section.
- Once a writer thread is done, if there are writers waiting, signal one into the critical section. otherwise allow the readers into the critical section.

#### Synch Problems
- With whale mating and stoplight I think the best advice that I can give is to read the test code to see how every thread is being executed. I did this with whale mating, I made an incorrect assumption about how the whale threads forked off and my tests were not passing. It wasn't until I read the test cases that I knew what was going wrong with my implementation. Once you know how the code will execute you can then begin to design and implement a solution.
- Whale mating sends out males and females first, then matchmakers.
- For stoplight, think about the conditions that could cause a deadlock in the intersection and then use synch primitives accordingly.
- Use a white board and think. These are great practice problems, and are similar to the ones that you will need to solve in ASST2 and ASST3

-------------------------------------------------------------------------------

## ASST 2 | System Call Interface

#### `open()` & `close()`
- something here

#### `read()` & `write()`
- something here

#### `lseek()`
- something here

#### `dup2()`
- something here

#### `_gcwd()` & `chdir()`
- something here

-------------------------------------------------------------------------------

## ASST 3.1 | Coremap
- something here

-------------------------------------------------------------------------------

## ASST 3.2 | Paging
- something here

-------------------------------------------------------------------------------

## ASST 3.3 | Swapping
- Brijesh is a God!!

-------------------------------------------------------------------------------


