## 基础知识
1. 
2. 
3. 
4. 
## FreeRTOSConfig.h中的相关配置
> configUSE_PREEMPTION  
1. 为1时，RTOS使用抢占式调度器,0时表示时间片调度器。
2. 协作式操作系统是任务主动释放CPU后，切换到下一个任务。任务切换的时机完全取决于正在运行的任务。
> configUSE_PORT_OPTIMISED_TASK_SELECTION

某些运行FreeRTOS的硬件有两种方法选择下一个要执行的任务：通用方法和特定于硬件的方法。
1. 通用方法：
* configUSE_PORT_OPTIMISED_TASK_SELECTION设置为0或者硬件不支持这种特殊方法
* 可以用于所有FreeRTOS支持的硬件
* 完全用c语言实现，效率略低于特殊方法
* 不强制要求限制最大可用优先级数目

2. 特定方法：
* 并非所有硬件都支持
* 必须将configUSE_PORT_OPTIMISED_TASK_SELECTION设置为1
* 依赖一个或多个特定架构的汇编指令(一般是类似计算前导零[CLZ]指令)
* 比通用方法更高效
* 一般强制限定最大可用优先级数目为32

> configUSE_TICKLESS_IDLE
1. 为1时使能低功耗tickless模式，为0时系统节拍tick中断一直运行
2. 


> configUSE_TICK_HOOK
1. 
2. 

> configCPU_CLOCK_HZ
1. 
2. 

> configTICK_RATE_HZ
1. 
2. 

> configMAX_PRIORITIES
1. 
2. 

> configMINIMAL_STACK_SIZE
1. 
2. 

> configTOTAL_HEAP_SIZE
1. 
2. 

> configMAX_TASK_NAME_LEN
1. 
2. 

> configUSE_TRACE_FACILITY
1. 
2. 

> configUSE_STATS_FORMATTING_FUNCTIONS 
1. 
2. 

> configUSE_16_BIT_TICKS
1. 
2. 

> configIDLE_SHOULD_YIELD
1. 
2. 

> configUSE_TASK_NOTIFICATIONS
1. 
2. 

> configUSE_MUTEXES
1. 
2. 

> configUSE_RECURSIVE_MUTEXES
1. 
2. 

> configUSE_COUNTING_SEMAPHORES
1. 
2. 

> configUSE_ALTERNATIVE_API
1. 
2. 

> configCHECK_FOR_STACK_OVERFLOW
1. 
2. 

> configQUEUE_REGISTRY_SIZE
1. 
2. 

> configUSE_QUEUE_SETS
1. 
2. 

> configUSE_TIME_SLICING
1. 
2. 

> configUSE_NEWLIB_REENTRANT
1. 
2. 

> configENABLE_BACKWARD_COMPATIBILITY
1. 
2. 

> configNUM_THREAD_LOCAL_STORAGE_POINTERS
1. 
2. 

> configGENERATE_RUN_TIME_STATS
1. 
2. 

> configUSE_CO_ROUTINES
1. 
2. 

> configMAX_CO_ROUTINE_PRIORITIES
1. 
2. 

> configUSE_TIMERS
1. 
2. 

> configTIMER_TASK_PRIORITY
1. 
2. 

> configTIMER_QUEUE_LENGTH
1. 
2. 

> configTIMER_TASK_STACK_DEPTH
1. 
2. 

> configKERNEL_INTERRUPT_PRIORITY、configMAX_SYSCALL_INTERRUPT_PRIORITY和configMAX_API_CALL_INTERRUPT_PRIORITY
1. 
2. 

> configASSERT
1. 
2. 

> INCLUDE Parameters
1. 
2. 

## 