<div style="text-align: justify">

# **Relevant research papers for fingerprinting workloads in OpenShift clusters**

This document will provide an understanding of various research articles related to fingerprinting workloads. Here is the [google docs](https://docs.google.com/document/d/120fm-EnnM8bmvku9POaDKTb-9dbkqwV_bnIRnIpyDMk/edit) link of the document.

## **[Autonomic characterization of workloads using workload fingerprinting:](https://ieeexplore.ieee.org/document/7015482)**

In this paper the author developed a workload/phase detection model that uses machine learning methodology to classify the workload behavior into various phases of workload operation. The paper describes workload fingerprinting methodology involving two step process that can be summarized as:

1. Workload detection - Identifying the type of workload.

2. Phase detection - Identifying distinct phases for a given type of workload.

Workload execution is typically characterized by many different features ranging from cache, behavior, CPU utilization, memory bandwidth, I/O bandwidth and so on. The workload detection process uses a supervised classification process to train a model that detects the type of workload using reduced feature sets. The learning process infers the underlying relationship between the observed feature and a target workload type variable which is a subject of prediction. Adaboost algorithm is used to synthesize workload detection models.



Phase detection in a workload acts as an essential ingredient that captures time varying behavior of dynamically adaptable systems. A phase is a stage of execution in which a workload demonstrates similar power, temperature, resource utilization and performance characteristics. K-means clustering is used to partition d-dimensional features into k clusters such that each emission belongs to the clusters with the nearest mean.


<table>
  <tr>
   <td><strong>Event Counter</strong>
   </td>
   <td><strong>Significance (%)</strong>
   </td>
  </tr>
  <tr>
   <td>FREERUN_CORE_ENERGY_STATUS
   </td>
   <td>51.677
   </td>
  </tr>
  <tr>
   <td>OFFCORE_REQUEST.ALL_DATA_RD
   </td>
   <td>23.775
   </td>
  </tr>
  <tr>
   <td>LONGEST_LAT_CACHE.MISS
   </td>
   <td>7.226
   </td>
  </tr>
  <tr>
   <td>CYCLE_ACTIVITY.CYCLES_LID_PENDING
   </td>
   <td>6.227
   </td>
  </tr>
  <tr>
   <td>UOPS_ISSUED.CORE_STALL_CYCLES
   </td>
   <td>3.881
   </td>
  </tr>
  <tr>
   <td>SCY
   </td>
   <td>2.655
   </td>
  </tr>
  <tr>
   <td>UOPS_RETIRED.STALL_CYCLES
   </td>
   <td>2.606
   </td>
  </tr>
  <tr>
   <td>CPU_CLK_UNHALTED.THREAD
   </td>
   <td>0.962
   </td>
  </tr>
</table>


TABLE I: SINGLE WORKLOAD CASE: RELATIVE SIGNIFICANCE OF OBSERVED EVENTS FOR WORKLOAD IDENTIFICATION

They developed a workload/phase detection model that uses machine learning methodology to classify the workload behavior into various phases of workload operation. The first part of the methodology comprises workload detection that uses weak classifiers as in Adaboost. The algorithm provides the two outputs. First, identify the most significant events in identifying the workload and second, model to classify the workload based on hardware events. The bagging algorithm identifies nine events with non-zero importance in workload classification, listed in Table I. Once the workloads are identified, the second part of the methodology uses variants of k-means clustering to synthesize distinctive phases (or behaviors) within workloads. The workload-phase feature acts as an additional vector in addition to existing features that improves training models used for service-level-objective (SLO) related control processes (Load Allocation, Re-balancing, Resource-Provisioning, Contention-Avoidance). Results demonstrate a high degree of accuracy (99%) in workload identification and 97.15% accuracy in resource forecasting.



## **[Fingerprinting anomalous computation with RNN for GPU-accelerated HPC machine:](https://sc19.supercomputing.org/proceedings/src_poster/poster_files/spostg129s2-file2.pdf)**

The paper presented a ML based automatic illicit workload detection framework for GPU accelerated HPC systems such as Summit. Illicit workloads include, exploiting systems for bitcoin mining, brute force password cracking, and GPU-inflated denial of service (DoS) attack. They collected as many features as possible to identify the characteristic of GPC-accelerated HPC workload. It presented an ML framework for classifying GPGPU workloads based on their microarchitectural and system behavior, and collected the multiple types of workload behavioral data from multiple sources, viz., microarchitectural events behavior, data movement behavior, and resources utilization behavior.

The analysis was done on labelled data, ANN achieved the highest accuracy (98%), while 76% and 88% for KNN and SVM, respectively. Memory access patterns show the most significant difference among workloads. The execution-related factors such as SM occupancy, instruction-replay, etc. are also good indicators for application discrimination. The models trained with data-movement are slightly more accurate than others.

## **[I/O workload fingerprinting in the genetic-library:](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.504.3994&rep=rep1&type=pdf)**

This paper talks about disk scheduling and the effect of workload fingerprinting in performance tuning. It serves as a good example of improvement in the performance of different types of workload due to fingerprinting. The paper describes how to create an I/O workload fingerprint and its use in both I/O schedulers, and in the genetic library. Main focus of the paper is on the application of fingerprinting in the genetic library. Paper distinguished different types of workload based on characteristics such as type (read/write), size (small/large), pattern (sequential/random) and using these categories they constructed a fingerprint. The main purpose of I/O workload fingerprinting is to converge on optimal turntables quicker during a changing work-load. To test how well it performed a [flexible file system benchmark](https://sourceforge.net/projects/ffsb/) was used. The FFSB is a versatile benchmark which is able to simulate almost any I/O workloads. As a conclusion, workloads based on sequential read and sequential write converged with an 89% and 97% reduction in time, respectively. Random read/ random write converged with a 61% and 19% reduction in time, respectively.

## **[VM and workload fingerprinting for software defined datacenters:](https://dspace.mit.edu/handle/1721.1/85425)**

It is a thesis from MIT (2013). It serves the purpose of explaining some basic theoretical concepts and strategies with regards to workload fingerprinting, namely, the Pearson correlation coefficient, principal component analysis, K- Means clustering, logistic regression, entropy, relative entropy, Silverman’s test for multimodality, bayesian inference and so on.

In this thesis, fingerprints are used to represent the relationships (neighborhoods of similarity) between VMs based on the telemetry. There are two categories of data: metadata (e.g. total number of CPUs for the VM, VM friendly name, VM host name, VM resource pool name, host computing and memory resources, host vendor, the number of VMs of the host, the resource pool computing and memory resources, etc), and performance metrics which captures the effect of workload on the virtual machine (e.g, _cpu.usage.average_ denotes the average CPU usage in the sample period). The results are then exploited for explaining performance variations (explaining why VMs expected to be similar are behaving as if they are different), and for obtaining hints regarding placement and co-location. They design the number of fingerprints so that they are easy to compute and scale linearly with the number of performance metrics considered, not the number of machines. In addition, they also used K-Means for clustering and Logistic Regression for classification.

</div>
