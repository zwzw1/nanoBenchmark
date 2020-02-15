# nanoBenchmark
Benchmark codes in cycles in kernel mode.

1. The benchmark origins from "How to Benchmark Code Execution Times on Intel® IA-32 and IA-64 Instruction Set Architectures" by Gabriele Paoloni.
2. Load  commands: insmod codes_Prcisely.ko . unload commands: rmmod codes_Prcisely.ko
3. output: /var/log/messages
4. Intel(R) Xeon(R) CPU E5-2650 v3 @ 2.30GHz
    benchmark cost: 24~31 cycles
    rdtscp cost: 52~62 cycles with benchmark cost. Hence, rdtsc may use: 21 ~ 38 cycles
   
    Intel(R) Core(TM) i9-7920X CPU @ 2.90GHz
    benchmark cost: 21~29 cycles
    rdtscp cost: 47~57 cycles with benchmark cost. Hence, rdtsc may use aboule: 18 ~ 36 cycles
    
