# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:

## C Program to create new process using Linux API system calls fork() and getpid() , getppid() and to print process ID and parent Process ID using Linux API system calls


pid_t process_id;

//variable to store parent function's process id

pid_t p_process_id;

//getpid() - will return process id of calling function

process_id = getpid();

//getppid() - will return process id of parent function

p_process_id = getppid();

//printing the process ids//printing the process ids

printf("The process id: %d\n",process_id);

printf("The process id of parent function: %d\n",p_process_id);

return 0; }










##OUTPUT

<img width="854" height="62" alt="319454984-d24beae3-3302-41af-881e-30172c3510e1" src="https://github.com/user-attachments/assets/547db892-9714-4a48-a7e1-afbe8e785e7a" />







## C Program to execute Linux system commands using Linux API system calls exec() , exit() , wait() family





    printf("Running ps with execlp\n");
    
    execl("ps", "ps", "ax", NULL);
    
    wait(&status);
    
    if (WIFEXITED(status))
    
            printf("child exited with status of %d\n", WEXITSTATUS(status));
            
    else
    
            puts("child did not exit successfully\n");
            
    printf("Done.\n");

    printf("Running ps with execlp. Now with path specified\n");
    
    execl("/bin/ps", "ps", "ax", NULL);
    
    wait(&status);
    
    if (WIFEXITED(status))
    
            printf("child exited with status of %d\n", WEXITSTATUS(status));
            
    else
    
            puts("child did not exit successfully\n");
            
    printf("Done.\n");
    
    exit(0);}




















##OUTPUT




<img width="855" height="193" alt="319455196-98132d53-20dd-4faa-bf2e-54d7196c174e" src="https://github.com/user-attachments/assets/74dd8a93-3f5a-4974-adb0-f61d9aca431b" />














# RESULT:
The programs are executed successfully.
