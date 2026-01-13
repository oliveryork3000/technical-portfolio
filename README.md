# Technical Portfolio - Operational Logic & Systems Architecture

## Overview
This repository demonstrates architectural patterns for **resource allocation under constraints**—a problem domain common to supply chain operations, data center capacity planning, and cloud infrastructure management. 

The samples illustrate how I balance competing priorities (SLA preservation vs. cost optimization) while enforcing strict governance on AI-augmented decision-making.

## Core Technical Patterns
These samples demonstrate infrastructure-relevant concepts applicable to Technical Program Management at scale:

1. **Multi-Constraint Optimization**: Allocating resources (compute, power, cooling) when multiple physical limits are active simultaneously.
2. **Priority-Based Scheduling**: Workload prioritization frameworks (P0/P1/P2) ensuring SLA-critical jobs survive during capacity shortfalls.
3. **Hybrid Decision Architecture**: Combining deterministic logic (for mathematical correctness) with LLM reasoning (for qualitative trade-off analysis) while preventing hallucinations.
4. **Integrity Validation Layers**: Programmatic safeguards that verify AI outputs haven't drifted from ground truth.

## Why This Matters for Infrastructure Operations
These samples apply operational systems thinking to resource allocation problems. While the original implementations addressed industrial operations, the underlying patterns—constraint optimization, priority-based scheduling, integrity validation—are domain-agnostic and directly applicable to infrastructure operations at scale.

| Concept | Supply Chain / Ops Context | Infrastructure / Data Center Context |
| :--- | :--- | :--- |
| **Constraint** | Limited Inventory / Port Congestion | Power Capacity / Cooling Failure |
| **Allocation** | Customer Segmentation (Contract vs Spot) | Workload Prioritization (Prod vs Batch) |
| **Risk** | Contract Penalties / Churn | SLA Violation / Outage |

## Code Samples

### 1. Hybrid Decision Agent (`product_line_manager_agent.py`)
**Pattern:** Hybrid Intelligence (Deterministic Kernel + LLM Narrative).
* **Use Case:** Allocating scarce resources during a crisis event.
* **Key Feature:** Implements an "Integrity Layer" that allows Python to validate LLM outputs, preventing hallucinations in critical allocation math.
* **Relevance:** Critical for automating incident response playbooks where human-readable explanation is required but mathematical precision is non-negotiable.

### 2. Capacity Allocation Simulator (`capacity_allocation_simulator.py`)
**Pattern:** Multi-constraint Optimization.
* **Use Case:** Simulating workload placement across zones with limited Power (kW) and Cooling (Tons).
* **Key Feature:** Prioritization logic that sacrifices "Best Effort" (P2) workloads to preserve "Critical" (P0) SLAs during physical constraint events.

## When These Patterns Apply
**Hybrid Decision Architecture** is useful when:
- Decisions require both mathematical precision AND qualitative judgment.
- Human stakeholders need explainable reasoning for automated recommendations.
- The cost of error is high (SLA penalties, outages, financial impact).

**Multi-Constraint Optimization** is useful when:
- Resources have multiple competing limits (power AND cooling, bandwidth AND compute).
- Trade-offs exist between utilization and reliability.
- Workload priorities are heterogeneous (production vs. research vs. batch).

**Real-world analogues:**
- Data center capacity allocation during power/cooling failures
- Cloud resource scheduling across availability zones
- Network bandwidth allocation during DDoS mitigation


## Contact
**Oliver York** 
[LinkedIn](https://www.linkedin.com/in/oliver-york/)
```
