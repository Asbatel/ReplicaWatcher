# **System Call Update: Debian Buster to Bullseye in PHP Apache**

This example underscores the significant yet subtle impacts that even minor updates in the base operating system can have on system calls within a PHP Apache environment. Specifically, it highlights the transition from `nanosleep` to `clock_nanosleep` system calls after upgrading from Debian Buster to Debian Bullseye. This change, while reflective of kernel and library updates between Debian versions, serves as a poignant example of how such updates can inadvertently affect anomaly-based Intrusion Detection Systems (IDS), potentially leading to false positives.

## **Key Change**

After updating the base OS, `nanosleep` system calls are replaced by `clock_nanosleep`, reflecting kernel and library updates between Debian versions.

## **Sysdig Captures**

### **Debian Buster - `nanosleep` Usage**

![nanosleep in Debian Buster](https://github.com/Asbatel/ReplicaWatcher/tree/master/normalityshift/buster.png)

*Sysdig capture showing `nanosleep` system calls in Debian Buster.*

### **Debian Bullseye - `clock_nanosleep` Usage**

![clock_nanosleep in Debian Bullseye](https://github.com/Asbatel/ReplicaWatcher/tree/master/normalityshift/bullseye.png)

*Sysdig capture showing `clock_nanosleep` system calls in Debian Bullseye.*


