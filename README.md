# Distributed-Blocking-Hybrid-Flowshop-Scheduling-Problem-with-Transportation-Time-instances
Distributed Blocking Hybrid Flowshop Scheduling Problem with Transportation Time instances 
DBHFSP-E benchmark instance set


This directory contains the 100 benchmark instances used in the computational experiments.
Each instance corresponds to one combination of:
- number of jobs n in {30, 50, 100, 150, 200};
- number of stages s in {2, 4, 6, 8};
- number of factories f in {2, 3, 4, 5, 6}.

The instance identifier uses the format n<N>_s<S>_f<F>. For example, n30_s2_f2 denotes an instance with 30 jobs, 2 stages, and 2 factories.

Generation rule
The instances follow the generation settings reported in the manuscript. For each instance:
- the number of identical parallel machines at each stage is sampled independently from the discrete uniform distribution [2, 6];
- the base processing time p[j,l] of each job j at each stage l is sampled independently from the discrete uniform distribution [1, 30];
- the transportation time between two different global machines is sampled independently from the discrete uniform distribution [1, 10];
- the transportation time from a machine to itself is 0;
- the speed set is {1.0, 1.2, 1.5}.

File format
Each instance file is a plain-text file with four parts:
1. metadata: instance_id, n_jobs, n_stages, n_factories, n_machines, and speed_set;
2. machines_per_stage: stage_id, machine_count, and the global machine IDs belonging to that stage;
3. processing_time_matrix: rows are jobs and columns are stages;
4. transport_time_matrix: rows and columns are global machine IDs.

Machine, job, and stage IDs in the exported files are 1-based for readability. The released files are the exact benchmark instances to be used for reproducing the reported computational experiments.
