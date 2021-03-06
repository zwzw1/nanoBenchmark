# nanoBenchmark
Benchmark codes in cycles in kernel mode.

1. The benchmark origins from "How to Benchmark Code Execution Times on Intel® IA-32 and IA-64 Instruction Set Architectures" by Gabriele Paoloni.
2. Load  commands: insmod codes_Prcisely.ko . unload commands: rmmod codes_Prcisely.ko
3. output: /var/log/messages
4.  Intel(R) Xeon(R) CPU E5-2650 v3 @ 2.30GHz
    benchmark cost: 24 ~ 31 cycles
    rdtscp cost: 52 ~ 62 cycles with benchmark cost. Hence, rdtsc may use: 28 ~ 31 cycles
   
    Intel(R) Core(TM) i9-7920X CPU @ 2.90GHz
    benchmark cost: 21 ~ 29 cycles
    rdtscp cost: 47 ~ 57 cycles with benchmark cost. Hence, rdtsc may use aboule: 26 ~ 28 cycles
    
    Intel(R) Xeon(R) CPU E7-4809 v2 @ 1.90GHz
    benchmark cost: 48 ~ 52 cycles
    rdtscp cost: 84 ~ 88 cycles with benchmark cost. Hence, rdtsc may use aboule: 36  cycles
    
5. another benchmark : just use cycles between two consecutive calls

   In kernel mode counts:
   
       Intel(R) Xeon(R) CPU E5-2650 v3 @ 2.30GHz    28 cycles
       
       Intel(R) Core(TM) i9-7920X CPU @ 2.90GHz     28 cycles
       
       Intel(R) Xeon(R) CPU E7-4809 v2 @ 1.90GHz    40~45 cycles
       
   In user mode counts:
   
       Intel(R) Xeon(R) CPU E5-2650 v3 @ 2.30GHz    35 cycles
       
       Intel(R) Core(TM) i9-7920X CPU @ 2.90GHz     40 cycles
       
       Intel(R) Xeon(R) CPU E7-4809 v2 @ 1.90GHz    72 cycles   
       
