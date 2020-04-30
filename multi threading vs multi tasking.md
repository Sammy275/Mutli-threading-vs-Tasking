# Multi-threading vs Multi-Tasking

### Introduction:

There is a lot of misconception regarding what is **Multi-threading** and what is **Multi-tasking**. People seem to confuse both of these concepts.  
In this article I will compare both of these concepts and will help you in understanding, but first we need to define both of these concepts seperately.  

Let us first start with multi-tasking.

## Multi-Tasking:

Imagine that you are working as a secratory in some office. You have multiple things you have to do currently. You can also call these *things* a **task**.  
Each of these task requires your focus and attention span. Say you have to call and confirm meeting's time, on the other hand you have to book a time slot for your presentation, and you also have to stack some folders. All these jobs or *tasks* you have to do has to be done right now. So what you will do is give each of them some time. You will divide your attention or time to complete these tasks. First you will stack your folders and then quickly respond to email and then do something else. It might be really hard for you but it is really easy for the computer.

When you open a file on the computer and then you open another program, the computer divides the *attention span*. The file and the other program that you have opened is a task. Computer executes these more than one task by giving priority to one task for a specific period of time and then it moves to the other. This is happening so quickly that the user does not even notice. But if the task is really **CPU or IO Intensive** you will start to experience latency issues. That is when you'll say that the computer is *Freezing* or *Crashing*.

To sum it up, we can say that, Multi tasking is acheived when the CPU schedules that which task would be running at a given time, and when will the other tasks will get a turn. The act of scheduling or assigning CPU to another task is called **Context switching**. When context switching is done really quickly, it creates an illusion that the computer is executing both of the tasks in the same time.

## Multi-Threading:

You can imagine multi-threading as dividing one task into many parts. While multi-tasking concerns with scheduling two or more than 2 tasks. Multi-threading is concerns with running different parts of the same task concurrently. Keeping up with the secretory example, say you have to schedule the meeting, you will atleast have to do 2 basic things. First of you will have to find the time slot which is perfect but you will have also have to inform the participants. You can do both of these tasks (Keep in mind these 2 tasks are a part of one main task: Scheduling a meeting) step by step, you cannot perform both of the tasks at the same time. But here comes a computer, once again outperforming a human.

When you execute a program or a task, the computer calls it a **Process**. This process, if programmed suitably can be assigned sub-processes or **Threads**. When you open MS Word document, computer calls it a process. You can do so many things, you can edit, print, save etc. But have you ever noticed that when you are saving a document, you cannot write anything else or when you are writing you can't change the text-color. The computer are just so fast the you cannot notice it but both of these things cannot happen at once. But when you are playing a game, you can hear the sounds, you can see objects, you can run while hearing things. The game is process or a task, the sounds that you hear, the zombies that you shoot, the sprint that you make are all sub-processes.

In multi-threading more than one core of the CPU is used at a time. The executions are happening in parallel. Sometimes these executions depends on the results of other executions. Multi-threading is done when a program is CPU intensive. You can divide a task into multiple threads to quickly perform it.

## Comparison:

* Multi-tasking is done by scheduling tasks and priorotizing them, which is also known as context-switching. Multi-threading is done by involving multiple cores of the CPU.

* Mutlti-tasking is not concerned with cores of the CPU, it can be done by a single core computer too, it is just slow compared to multiple cores. Multi-threading concerns with the cores of the CPU and uses resources.

* Multi-tasking is done by the operating system to handle multiple tasks. While multi multi-threading can be implemented in the program that you are making, as the program you are making is a task so you cannot multi-task it, it doesn't even make sense. Here is the example of creating a thread in Rust:
    use std::thread

    fn main() {  
        let handle = thread::spawn(|| {  
            for i in 1..10 {  
                print("Hello from new thread!!!");  
            }  
        });  

        handle.join().unwrap();  

        print("Hello from main thread");  
    }

* Mutli tasking is concerned with the primary memory or RAM. All the executing tasks are stored on the RAM, thus slowing down the over all speed of the computer if too many tasks are opened at the same time. Mutli threading requires a CPU with multiple cores so the task which is performing multi-threading can ask for the threads from the OS.