# siem-optimization-wazuh-security-onion

## Description

Bachelor's thesis focused on performance optimization of open-source SIEM platforms — Security Onion and Wazuh — in resource-constrained, single-node virtual environments (VMware). Agents were deployed on both Linux (Ubuntu) and Windows 10 endpoints.

## Key optimizations

- Compression: migrated from LZ4 to DEFLATE (`best_compression`), achieving ~20% index size reduction.
- Cluster stabilization: disabled replicas and reduced shard count, restoring GREEN cluster status.
- Query optimization: switched from Query Context to Filter Context, reducing response times up to 5× (from ~13 ms to ~2.4 ms).
- Noise reduction: implemented Wazuh Level 0 suppression rules to drop low-value events before indexing.

## Environment

- Single-node VMware virtual machines
- Agents on Ubuntu (Linux) and Windows 10 endpoints

## Results

Confirmed that a fully operational threat detection environment can be maintained on minimal hardware without compromising detection quality.