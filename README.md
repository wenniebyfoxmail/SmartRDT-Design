# SmartRDT-Design

Semantic and multi-objective design framework for road digital twin configurations.

This repository is a research prototype for exploring how road digital twin systems can be designed from heterogeneous sensing, algorithm, communication, storage, and deployment options. It combines ontology-based component representation with multi-objective optimisation to compare feasible infrastructure monitoring configurations under cost, performance, reliability, latency, disruption, and carbon constraints.

## Research Motivation

Road digital twins need more than a single model or sensor. A practical deployment requires choices across:

- sensing systems such as mobile mapping, UAV, IoT, fibre optic sensing, and low-cost vehicle sensors
- detection and condition-assessment algorithms
- cloud, edge, and hybrid compute deployment
- storage and communication infrastructure
- operational constraints such as inspection cycle, latency, disruption, cost, and carbon emissions

The project investigates how these choices can be encoded and searched systematically rather than selected ad hoc.

## What This Repository Contains

- `main.py` - entry point for running the optimisation workflow
- `ontology_manager.py` - road digital twin component ontology construction
- `optimization_core.py` - multi-objective optimisation logic
- `evaluation.py` - objective and constraint evaluation
- `baseline_methods.py` - baseline strategy comparison
- `visualization.py` - visualisation utilities
- `sensors_data.txt`, `algorithms_data.txt`, `infrastructure_data.txt`, `cost_benefit_data.txt` - component data used by the design search
- `config.json` - default experiment configuration

## Method Overview

The framework maps candidate road digital twin designs into a structured configuration space, evaluates them against engineering objectives, and searches for Pareto-optimal solutions.

Core ideas:

1. Represent digital twin components in an ontology-like structure.
2. Decode candidate solutions into sensor, algorithm, storage, communication, and deployment choices.
3. Evaluate performance, cost, latency, disruption, reliability, and carbon-related criteria.
4. Compare optimised configurations against baseline design strategies.
5. Generate figures and summary reports for analysis.

## Quick Start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

python main.py --config config.json
```

Optional flags:

```bash
python main.py --skip-baselines
python main.py --skip-visualization
python main.py --debug
```

## Why It Matters

This project supports the design side of road digital twins: choosing what to sense, how to process it, where to deploy computation, and how to trade off technical performance against practical infrastructure constraints.

It is part of a broader research direction on road digital twins for infrastructure maintenance, asset and condition identification, and decision support.

## Skills Demonstrated

- digital twin system design
- ontology-inspired data modelling
- multi-objective optimisation
- infrastructure sensing and monitoring
- engineering trade-off analysis
- Python research software development

## Status

Research prototype. The code is intended for experimentation and method development rather than production deployment.
