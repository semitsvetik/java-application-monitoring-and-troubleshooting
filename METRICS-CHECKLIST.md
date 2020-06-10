TIERED METRICS CHECKLIST
========================

Hardware
--------
- [ ] Total RAM: how much total RAM is available on PC and accessible by OS and applications.
- [ ] Total HDD: total volume of hard disk space accessible on PC by OS.

OS
--
- [ ] RAM available for Application: how much RAM is free at this moment (not used by any process).
- [ ] Free HDD: how much hard disk is free.
- [ ] File encoding: what encoding is used when writing to file. Overview -> System properties -> file.encoding. This is to make sure we can read file.

JAVA
--
- [ ] Application portability: can be run on any OS, hardware.
- [ ] Application min and max heap size: how min and max limits of heap size for running application. Can be monitored using VisualVm -> Overview -> JVM arguments -> -Xms128m, -Xmx2048m.
- [ ] The number of threads in application: number of thread launched, number of threads is acceptable, no performance degradation. Threads -> Live threads.
- [ ] Self time %, CPU time: % of overall time of running application on CPU that function consumes CPU. Sampler -> CPU. CPU time - time taken on CPU.
- [ ] Total time %, CPU time: % of overall time of running application on CPU that function and all functions called by this function taken on CPU. Sampler -> CPU. CPU time - time taken on CPU.

General 
--
- [ ] 
