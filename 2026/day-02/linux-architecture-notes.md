"Everything in linux is either a file or directory"
"Everything starts with a process"
Kernel: It is the main core component it is lies between the shell and the hardware. It controls the activity of other hardware components. The kernel is software that manages communication between the hardware and the system. It cannot directly interact with directories or files. Instead, the kernel handles the communication between the computer system and the hardware.

Shell: It is also software or It can be determined as the interface to the kernel. It takes commands from the user and interprets them. The shell transmits these commands to the kernel, which then performs the requested operations.

init / shell: systemd is a system and service manager for Linux operating systems. When run as first process on boot (as PID 1), it acts as init system that brings up and maintains userspace services. Separate instances are started for logged-in users to start their services.
systemd is usually not invoked directly by the user, but is installed as the /sbin/init symlink and started during early boot.

Process states:
1. Running:
  A process in the running state is either:
    Currently executing on the CPU
    Ready to run and waiting for CPU time
2. Sleeping:
    A sleeping process is waiting for an event to complete, such as:
    
    Input/Output operation
    Signal receipt
    Resource availability
    There are two types of sleep states:
    
    Interruptible Sleep (S):
    Can be woken up by signals
    Most common sleep state
    Uninterruptible Sleep (D):
    Cannot be interrupted by signals
    Usually waiting for hardware conditions

3. Stopped (T)
    A stopped process has been paused by:
    
    A user signal (SIGSTOP)
    Debugging operations

4. Zombie (Z)
    A zombie process is:
    
    A terminated process
    Still has an entry in the process table
    Waiting for its parent to collect its exit status

5. Dead (X)
    A dead process is:
    
    Completely terminated
    Being removed from the process table

Commands I would use daily:
ls
cd
top
chmod
chown
scp
ps -ef
