# Performance Troubleshooting

**Scenario:**  
User reports computer feels slow during multitasking.

**Date:**  
2/16/2026

**Initial Hypothesis:**  
High CPU, memory, or disk utilization.

**Baseline Metrics:**  
CPU:  14%
Memory: 81% 
Disk:  1%

**Stress Test Performed:**  
Opened 15 Chrome tabs and streamed YouTube video.

**Observed Metrics Under Load:**  
CPU:  4%
Memory:  86%
Disk:  0%

**Actions Taken:**  
Closed unused applications and browser tabs.

**Post-Action Metrics:**  
CPU:  8%
Memory:  55%
Disk:  0%

**Conclusion:**  
System slowdown correlated with increased memory usage during heavy multitasking.

**What I Learned:**  
Task Manager performance metrics help identify resource bottlenecks and confirm whether slowdown is resource-related.
