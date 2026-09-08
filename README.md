# FreeRTOS with STM32F4

This repository contains my **FreeRTOS programming, RTOS concepts, and practical implementations on STM32F4 microcontrollers**.

The work is based on the Udemy course **"Mastering RTOS: Hands on FreeRTOS and STM32Fx with Debugging"** by FastBit Embedded Brain Academy and Kiran Nayak.

The main objective of this repository is to understand how a **Real-Time Operating System (RTOS)** works on an ARM Cortex-M microcontroller and gain practical experience with **FreeRTOS task management, scheduling, synchronization, inter-task communication, interrupts, and debugging**.

---

## 🎯 Objectives

* Understand Real-Time Operating System concepts
* Understand FreeRTOS architecture
* Run FreeRTOS on STM32F4
* Create and manage multiple tasks
* Understand FreeRTOS scheduling
* Understand task states and priorities
* Learn task synchronization
* Learn inter-task communication
* Understand RTOS interrupt handling
* Understand ARM Cortex-M context switching
* Debug FreeRTOS applications
* Analyze task execution using SEGGER SystemView

---

## 🛠️ Hardware

### Microcontroller

* **STM32F407VG**
* ARM Cortex-M4
* STM32F4 family

### Development Board

The course uses the **STM32F407G-DISC1 Discovery board**. My implementations may also use STM32F407VG-based development hardware.

---

## 💻 Software & Tools

* **STM32CubeIDE**
* **FreeRTOS**
* **ARM GCC**
* **SEGGER SystemView**
* **ST-LINK**
* Embedded C
* Linux / Ubuntu

---

# 📚 Topics Covered

## 1. RTOS Fundamentals

* Real-Time Applications
* Real-Time Operating Systems
* RTOS vs General Purpose Operating Systems
* Task scheduling
* Task switching
* Latency
* Priority inversion
* Multitasking

---

## 2. FreeRTOS Setup

* FreeRTOS kernel
* FreeRTOS source code
* STM32 project configuration
* `FreeRTOSConfig.h`
* FreeRTOS portable layer
* Cortex-M4 GCC port
* Kernel configuration

---

## 3. FreeRTOS Tasks

* Task creation
* Task deletion
* Task priorities
* Task states
* Task delays
* Task scheduling
* Idle Task
* Timer Service Task
* Multiple task execution

Example:

```c
xTaskCreate(
    led_task,
    "LED_Task",
    128,
    NULL,
    2,
    NULL
);
```

---

## 4. FreeRTOS Scheduler

* Scheduler fundamentals
* Preemptive scheduling
* Cooperative scheduling
* Task priorities
* Context switching
* Kernel tick
* Tick frequency
* `SysTick`
* Task switching

---

## 5. Task Notifications

* Task notification concept
* Sending notifications
* Receiving notifications
* Task-to-task signaling
* Lightweight synchronization

---

## 6. Queues

* Queue creation
* Sending data to queues
* Receiving data from queues
* Blocking queues
* Task-to-task communication
* Producer-consumer model

Example:

```c
xQueueSend(queue_handle, &data, portMAX_DELAY);

xQueueReceive(queue_handle, &data, portMAX_DELAY);
```

---

## 7. Semaphores

* Binary semaphore
* Counting semaphore
* Semaphore creation
* Task synchronization
* Interrupt-to-task synchronization
* Event synchronization

---

## 8. Mutex

* Mutual exclusion
* Mutex creation
* Resource protection
* Task synchronization
* Priority inversion
* Protecting shared resources

---

## 9. Interrupts and FreeRTOS

* Interrupt handling
* ISR execution
* Interrupt-safe FreeRTOS APIs
* ISR-to-task synchronization
* Deferred processing
* `FromISR()` APIs
* Interrupt priority configuration

---

## 10. ARM Cortex-M and FreeRTOS

One of the important objectives of this course is understanding the relationship between **FreeRTOS and the ARM Cortex-M architecture**.

Topics include:

* Cortex-M exception model
* Context switching
* `SysTick_Handler`
* `PendSV_Handler`
* `SVC_Handler`
* Supervisor calls
* PendSV
* Stack management
* Exception priorities
* Task stack
* Kernel stack

---

## 11. FreeRTOS Memory Management

* FreeRTOS heap
* Stack management
* Task stack allocation
* Heap configuration
* Memory management concepts
* Stack overflow considerations

---

## 12. FreeRTOS Debugging

### SEGGER SystemView

This repository also covers RTOS debugging and execution tracing using **SEGGER SystemView**.

Topics include:

* RTOS trace
* Task execution monitoring
* Task switching visualization
* Scheduler analysis
* UART-based recording
* Snapshot recording
* Continuous recording
* Debugging task behavior

---

# 📂 Repository Structure

```text
FreeRTOS_STM32F4/
│
├── 01_RTOS_Introduction/
│
├── 02_FreeRTOS_Setup/
│
├── 03_Task_Creation/
│
├── 04_Task_Scheduling/
│
├── 05_Task_States/
│
├── 06_Task_Delay/
│
├── 07_Task_Notification/
│
├── 08_Queue/
│
├── 09_Semaphore/
│
├── 10_Mutex/
│
├── 11_Interrupt_Synchronization/
│
├── 12_Context_Switching/
│
├── 13_ARM_Cortex_M_FreeRTOS/
│
├── 14_FreeRTOS_Memory/
│
├── 15_SEGGER_SystemView/
│
└── README.md
```

---

# 🔧 Example RTOS Application

A typical application in this repository follows this architecture:

```text
                 STM32F407VG
                      │
              ┌───────┴───────┐
              │    FreeRTOS   │
              └───────┬───────┘
                      │
       ┌──────────────┼──────────────┐
       │              │              │
   Task 1          Task 2          Task 3
    LED             UART            Sensor
       │              │              │
       └──────────────┼──────────────┘
                      │
                  Scheduler
                      │
              Context Switching
                      │
              Cortex-M4 CPU
```


---

# 🧪 Practical Exercises

The repository will contain practical implementations such as:

* Multiple LED tasks
* Task scheduling demonstrations
* Task delay examples
* Task notification examples
* Queue-based communication
* Semaphore-based synchronization
* Mutex-based resource protection
* Interrupt-to-task communication
* Context-switching experiments
* FreeRTOS debugging with SystemView

---

# 📖 Learning Resource

**Course:** Mastering RTOS: Hands on FreeRTOS and STM32Fx with Debugging

**Instructor:** FastBit Embedded Brain Academy / Kiran Nayak

**Platform:** Udemy

[Udemy Course](https://www.udemy.com/course/mastering-rtos-hands-on-with-freertos-arduino-and-stm32fx/?utm_source=chatgpt.com)

The course covers FreeRTOS programming and debugging on STM32F4/ARM Cortex-M platforms, including tasks, scheduling, queues, semaphores, mutexes, context switching, interrupt synchronization, and SystemView debugging.

---

# 🚀 Goal

The goal of this repository is to build practical knowledge in:

```text
Embedded C
     ↓
ARM Cortex-M4
     ↓
STM32F407VG
     ↓
FreeRTOS
     ↓
Tasks & Scheduling
     ↓
Synchronization
     ↓
Inter-Task Communication
     ↓
Interrupt Handling
     ↓
RTOS Debugging
     ↓
Embedded Firmware Development
```

This repository is part of my ongoing journey toward becoming a stronger **Embedded Software / Firmware Developer**.

---

## 👨‍💻 Author

**Nilanshu Dashwath**

Embedded Software / Embedded AI Developer

---

⭐ This repository will be continuously updated as I learn, implement, debug, and experiment with FreeRTOS on STM32F4.
