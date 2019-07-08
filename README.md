A day of “fishy” school
Small fish are going to school every day. They first arrive at a meeting place (simulate fish
getting to the meeting place by using sleep(random_time)), where they group in, GS, group
size. From there, they will use a manta ray, named Mantis, as way of transportation to get to
the school at a remote reef. Mantis waits until all the fish are gathered together (use busy
waiting). Each of the fish that are already grouped impatiently checks if the number of fish
already gathered is equal to FN (busy waiting); After each check, the fish that just checked
gets lazy and lets another fish do the check (use yield( ) twice).The first fish to find out that they
are all gathered will let Mantis know they are ready to head to the school at the remote reef.
Mantis, whose capacity is MC takes as many groups as it can and transports them to the
classroom at the remote reef. Mantis comes back as many times as needed to transport all the
fish groups. (Simulate waiting for the transport by busy waiting). (you need to find a way of
showing what fish is in each group and what group(s) are currently transported). While riding
Mantis, all fish are dreaming (use sleep of a long time).
Fearful of sharks, Mantis increases its speed to get its task accomplished (speeding
up=increasing priority;use getPriority( ), setPriority( )). Mantis speeds up only for a limited
time. After a very short time, in safe waters, it will reset its priority back to the default one.
Once at the reef Mantis randomly picks one of the fish on its back and interrupts him to let him
know they’ve arrived. The awakened fish will wake up (interrupt) another fish, this process is
repeated until the last fish is awakened (platoon policy) (use interrupt() and isInterrupted()
Have a message inside the catch(InterruptedException e) to check that the thread has been
interrupted, and who interrupted whom).
When Mantis is done transporting fish to school, he will take a break (sleep of a longer time).
When Mantis wakes up, it will join fish N. fish N joins with fish N-1,…. fish 2 joins with fish1. Fish
1 will just terminate. (use join( ) and isAlive())
Using the synchronization tools and techniques learned in class, synchronize the fish thread
and Mantis threads – in the context of the problem described above.
The number of fish should be entered as an argument.
In order to simulate different actions you must pick reasonable intervals of random time. Make
sure that the execution of the entire program is somewhere between 40 seconds and 90
seconds.
