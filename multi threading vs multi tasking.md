# Multi-threading vs Multi-Tasking

### Introduction:

There is a lot of misconception regarding what is **Multi-threading** and what is **Multi-tasking**. People seem to confuse both of these concepts.  
In this article I will compare both of these concepts and will help you in understanding, but first we need to define both of these concepts seperately.  

Let us first start with multi-tasking.

## Multi-Tasking:

Imagine that you are working as a seceratory in some office. You have multiple things you have to do currently. You can also call these *things* a **task**.  
Each of these task requires your focus and attention span. Say you have to call and confirm meeting's time, on the other hand you have to book a time slot for your presentation, and you also have to stack some folders. All these jobs or *tasks* you have to do has to be done right now. So what you will do is give each of them some time. You will divide your attention or time to complete these tasks. First you will stack your folders and then quickly respond to email and then do something else. It might be really hard for you but it is really easy for the computer.

When you open a file on the computer and then you open another program, the computer divides the *attention span*. The file and the other program that you have opened is a task. Computer executes these more than one task by giving priority to one task for a specific period of time and then it moves to the other. This is happening so quickly that the user does not even notice. But if the task is really **CPU or IO Intensive** you will start to experience latency issues. That is when youll say that the computer is *Freezing* or *Crashing*.

To sum it up, we can say that, Multi tasking is acheived when the CPU schedules that which task would be running at a given time, and when will the other tasks will get a turn. The act of scheduling or assigning CPU to another task is called **Context switching**. When the context switching is done really quickly, it creates an illusion that the computer is executing both of the tasks in the same time.

## Multi-Threading:

You can imagine multi-threading as diving one task into many parts. While multi-tasking concerns with scheduling two or more than 2 tasks. Multi-threading is concerns with running different parts of the same task concurrently. Keeping up with the seceratory example, say you have to schedule the meeting, you will atleast have to do 2 basic things. First of you will have to find the time slot which is perfect but you will have also have to inform the participants. You can do both of these tasks (Keep in mind these 2 tasks are a part of one main task: Scheduling a meeting) step by step, you cannot perform both of the tasks at the same time. But here comes a computer, once again outperforming a human.

