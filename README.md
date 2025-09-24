# Process Scheduling Simulator  

This project is a **university assignment** about simulating **process scheduling in multitasking operating systems** using **priority queues**.  

The base code was originally developed by **Erwin Meza Vega <emezav@gmail.com>**.  
My role is to **fix and extend the implementation**, ensuring that the scheduling strategies (FIFO, SJF, SRT, RR) work correctly.  

---

##  Process Scheduling  

In a multitasking operating system, processes appear to be executed simultaneously. In reality, the available CPUs must be shared among a large number of processes, each running for a certain time slice before being preempted to allow others to execute.  

The goal of this project is to simulate the **process scheduling task** in an operating system by implementing the primitives needed to support process scheduling using **priority queues**.  

---

##  Program Input  

The simulator reads its configuration from **standard input** (or a configuration file) and supports three types of commands:  

- **DEFINE** → Defines simulation parameters (queues, scheduling strategy, quantum).  
- **PROCESS** → Defines process arrivals.  
- **START** → Signals the end of configuration and starts the simulation.  

---

##  Running the Simulator  

### Linux  

```bash
./scheduler config_file
./scheduler < config_file
./scheduler test/caso_1_fifo.txt
./scheduler test/caso_1_rr.txt
./scheduler test/caso_1_sjf.txt
./scheduler test/caso_1_srt.txt





