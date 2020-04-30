# Multi-threading vs Multi-Tasking

### Introduction:

There is a lot of misconception regarding what is **Multi-threading** and what is **Multi-tasking**. People seem to confuse both of these concepts.  
In this article I will compare both of these concepts and will help you in understanding, but first we need to define both of these concepts seperately.  

Let us first start with multi-tasking.

## Multi-Tasking:

Imagine that you are working as a seceratory in some office. You have multiple things you have to do currently. You can also call these *things* a **task**.  
Each of these task requires your focus and attention span. Say you have to call and confirm meeting's time, on the other hand you have to book a time slot for your presentation, and you also have to stack some folders. All these jobs or *tasks* you have to do has to be done right now. So what you will do is give each of them some time. You will divide your attention or time to complete these tasks. First you will stack your folders and then quickly respond to email and then do something else. It might be really hard for you but it is really easy for the computer.

When you open a file on the computer and then you open another program, the computer divides the *attention span*. The file and the other program that you have opened is a task. Computer executes these more than one task by giving priority to one task for a specific period of time and then it moves to the other. This is happening so quickly that the user does not even notice. But if the task is really **CPU or IO Intensive** you will start to experience latency issues. That is when youll say that the computer is *Freezing* or *Crashing*.