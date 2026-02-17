# Performance Troubleshooting

**Scenario:**  
User reports computer feels slow during multitasking.

**Date:**  
2/16/2026

**Initial Hypothesis:**  
Potential high CPU, memory, or disk utilization causing resource bottleneck.

**Baseline Metrics:**  
CPU:  14%
Memory: 81% 
Disk:  1%

**Stress Test Performed:**  
Opened 15 Chrome tabs and streamed a YouTube video to simulate heavy multitasking.

**Observed Metrics Under Load:**  
CPU:  4%
Memory:  86%
Disk:  0%

**Analysis:**
CPU utilization decreased under load, indicating CPU was not the bottleneck.
Memory usage increased from 81% to 86%, suggesting limited available RAM during multitasking.
Disk usage remained minimal, ruling out storage-related performance issues.

**Actions Taken:**  
Closed unused applications and browser tabs.

**Post-Action Metrics:**  
CPU:  8%
Memory:  55%
Disk:  0%

**Conclusion:**  
Performance degradation during multitasking was primarily memory-related. Reducing active applications significantly improved available memory and overall system responsiveness.

**What I Learned:**  
Evaluating each resource independently (CPU, memory, disk) is critical before assuming the cause of system slowdown. Memory saturation can impact responsiveness even when CPU and disk usage remain low.
