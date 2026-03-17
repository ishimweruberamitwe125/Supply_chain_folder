# Predictive Risk & Optimization for U.S. Critical Manufacturing Supply Chains

**Data-driven tools to support industrial stability, continuity planning, and national security in critical manufacturing supply chains.**

This repository contains a practical, quantitative framework for **predictive risk and optimization** in U.S. semiconductor and defense-related manufacturing supply chains. It is intended as a **usable reference for supply chain professionals across industries, semiconductor OEMs, tiered suppliers, and policymakers** who want to understand and redesign ordering and inventory strategies for greater resilience.

---

## Purpose & Industrial Significance

This work sits at the intersection of **operations research**, **predictive risk modeling**, and **critical manufacturing management**. The goal is to move beyond abstract theory and demonstrate how multi-product inventory models can directly inform:

- **Identification of chokepoints** and single points of failure in multi-product, multi-supplier networks  
- **Forecasting the propagation of disruptions** through ordering and inventory dependencies  
- **Continuity planning** via optimized order policies and aggregation strategies that reduce cost *and* vulnerability  
- **Strengthening critical manufacturing resilience**, industrial stability, and national security

Disruptions in semiconductor and defense supply chains have direct implications for U.S. technological competitiveness, military readiness, and economic security. This project contributes to **data-driven decision support** that helps reduce reliance on fragile sourcing patterns and improves the stability of critical manufacturing systems.

From an industry perspective, this repository can be used as a **template and sandbox** for anyone working in supply chain, including semiconductor OEMs and their suppliers, to:

- Translating real demand, cost, and lead-time data into optimization models  
- Stress-testing existing sourcing policies under hypothetical disruption scenarios  
- Communicating trade-offs between cost efficiency, redundancy, and continuity to technical and non-technical stakeholders  

---

## Project Objectives

| Objective | Description |
|-----------|-------------|
| **Optimization of ordering & inventory** | Develop and compare sourcing strategies (independent, full aggregation, tailored aggregation) to minimize total cost while maintaining service levels. |
| **Chokepoint identification** | Use multi-product ordering models to reveal dependencies on common ordering costs and shared suppliers that can become chokepoints under disruption. |
| **Continuity-oriented design** | Design order policies that support continuity planning by balancing efficiency with redundancy and diversification. |
| **Quantitative resilience metrics** | Derive and compare total annual costs and order frequencies across strategies to quantify the impact of optimization on supply chain performance. |

---

## Repository Contents

### Multi-Product Supply Chain Optimization: EOQ & Tailored Aggregation

**Notebook:** `Multi-Product-Supply-Chain-Optimization-EOQ-Tailored-Aggregation.ipynb`

This notebook implements and compares three sourcing strategies for a multi-product supply chain, using **Economic Order Quantity (EOQ)** and **tailored aggregation** methods. The analysis is directly applicable to critical manufacturing contexts (e.g., semiconductor components, defense-related parts) where:

- Multiple products share **common ordering costs** (e.g., single supplier, shared logistics)
- **Product-specific ordering and holding costs** vary by item
- **Optimization** reduces total cost and supports more resilient, predictable ordering behavior

#### Strategies Implemented

1. **Independent sourcing**  
   Each product is ordered using its own EOQ. Total cost reflects no coordination; useful as a baseline and for identifying high-cost, high-frequency chokepoints.

2. **Full aggregation**  
   All products are ordered on a common frequency to amortize common ordering cost. Reduces total cost versus independent sourcing and decreases coordination complexity.

3. **Tailored aggregation**  
   Products are grouped by order frequency multiples (\(m_i\)) so that high-frequency items order every cycle and lower-frequency items order every \(m_i\) cycles. This strategy:
   - **Minimizes total annual cost** (ordering + holding) while preserving coordination benefits  
   - **Supports continuity planning** by making order patterns explicit and adaptable to disruption scenarios  
   - **Reveals chokepoints** through the dependence on common ordering cost and the impact of changing parameters  

#### Relevance to Critical Supply Chain Resilience

- **Chokepoints:** The common ordering cost in the model represents a shared resource (supplier, shipment, facility). Optimizing around it highlights where single points of failure exist.  
- **Disruption propagation:** Changing demand (\(D\)), costs, or lead times in the notebook allows analysis of how disruptions propagate through order frequencies and total cost.  
- **Continuity planning:** Tailored aggregation provides a structured, quantitative basis for deciding *how often* to order each product and how to adjust policies when suppliers or logistics are disrupted.  
- **Industrial stability:** Lower total cost and more predictable ordering support stable operations and reduce pressure on fragile links in semiconductor and defense supply chains.

---

## Technologies & Methods

- **Python** (NumPy, Pandas) for data handling and numerical computation  
- **Economic Order Quantity (EOQ)** and multi-product extensions  
- **Tailored aggregation** algorithm (order frequency multiples, optimal \(n\) and \(m_i\))  
- **Tabulate** for clear presentation of results  
- **Jupyter Notebook** for reproducible analysis and documentation  

---

## How to Run

1. Clone or download this repository.  
2. Install dependencies (e.g., `numpy`, `pandas`, `tabulate`).  
3. Open `Multi-Product-Supply-Chain-Optimization-EOQ-Tailored-Aggregation.ipynb` in Jupyter or VS Code.  
4. Run all cells to reproduce the comparison of independent, aggregated, and tailored aggregation strategies.  

---

## Connection to National Security & Critical Manufacturing

Resilient U.S. semiconductor and defense-related manufacturing supply chains require:

- **Identification of chokepoints** — where single suppliers or shared logistics create systemic risk  
- **Forecasting of disruption propagation** — how shocks in one product or supplier affect others  
- **Continuity planning** — pre-defined, optimized policies that can be adjusted when disruptions occur  
- **Industrial stability** — cost-effective, predictable operations that reduce vulnerability to geopolitical and logistical shocks  

This project demonstrates **optimization systems** that support these goals through rigorous, quantitative modeling of multi-product ordering and aggregation, with direct applicability to critical manufacturing and national security priorities.

---

## Author

**David Ishimwe Ruberamitwe**  

