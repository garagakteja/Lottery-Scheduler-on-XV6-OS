# Lottery-Scheduler-on-XV6-OS


Implementation and testing of the lottery scheduling algorithm for processes - a randomized algorithm that allows processes to receive a proportional share of the CPU without explicitly tracking how long each process has been run.


Specifically, building modified version of the xv6 shell such that:
1. Each struct proc has an additional field, tickets, that tracks how many tickets it has.
2. New processes are assigned 20 lottery tickets when they are created.
3. When the scheduler runs, it picks a random number between 0 and the total number of tickets. It then uses the algorithm described in class to loop over runnable processes and pick the one with the winning ticket.
4. User processes have a new system call, settickets, that allows a process to specify how many lottery tickets it wants. 
