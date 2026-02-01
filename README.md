# Agentic Health Risk Assessment

Agentic Health Risk Assessment is a scalable, agent-orchestrated health risk evaluation system built using IBM watsonx Orchestrate.
The project demonstrates how multiple specialized agents can collaboratively assess health risk from structured inputs and safely coordinate real-world actions such as appointment booking with explicit user consent.

This repository contains the frontend demonstration layer used for the hackathon. All agent logic, orchestration, and workflows are implemented within IBM watsonx Orchestrate.

---

## Demo Video

Full Project Demonstration (≤ 3 minutes):
https://drive.google.com/file/d/1wwork4tV33NF7f8XowGJayC5Tp0Ft88d/view?usp=sharing

The video demonstrates:
- Agent-based health risk assessment
- Multi-agent orchestration
- Critical condition detection
- Consent-gated appointment booking workflow
- Usage of IBM watsonx Orchestrate preview interface

---

## Problem Statement

Infants, pets, and other dependent individuals cannot clearly communicate early signs of health distress. Caregivers often receive fragmented health indicators such as heart rate, sleep quality, or activity levels without an explainable and reliable way to assess overall risk or determine what action should be taken.

Existing solutions either stop at raw monitoring or rely on opaque AI models that lack transparency, safety boundaries, and controlled escalation mechanisms.

---

## Solution Overview

Agentic Health Risk Assessment is designed as a core agentic intelligence layer rather than a single-purpose application.

- Health data can be provided from any source: sensors, wearables, external systems, or manual input.
- The system is data-source agnostic.
- For this hackathon, the system is demonstrated using structured inputs through the IBM watsonx Orchestrate preview interface.

The focus of the project is to demonstrate agent behavior, orchestration, explainability, and safe action coordination.

---

## System Architecture

Input Data
  -> Context & Normalization Agent
  -> Specialist Analysis Agents
     - Vital Signs Analysis
     - Sleep Cycle Evaluation
     - Activity & Mobility Assessment
  -> Risk Aggregation Agent
  -> Threat Classification Agent
  -> Action Recommendation Agent
  -> Decision Orchestrator Agent
  -> Optional Appointment Booking Workflow

---

## Agents Overview

Context & Normalization Agent:
Interprets subject metadata such as species, age category, and dependency type to ensure all downstream agents analyze data within the correct biological context.

Vital Signs Analysis Agent:
Analyzes physiological parameters like heart rate and body temperature using age- and species-specific reference ranges.

Sleep Cycle Evaluation Agent:
Evaluates sleep duration and quality against expected biological sleep patterns.

Activity & Mobility Assessment Agent:
Assesses activity levels and movement behavior to detect lethargy or abnormal inactivity.

Risk Aggregation Agent:
Combines severity indicators from all specialist agents into a unified and explainable risk score.

Threat Classification Agent:
Converts the aggregated risk score into clear threat levels such as Normal, Monitor, Warning, or Critical.

Action Recommendation Agent:
Maps the classified threat level to appropriate, non-diagnostic recommendations.

Decision Orchestrator Agent:
Acts as the central coordinator that collects outputs from all agents, produces the final explainable response, manages user consent, and invokes automated workflows when appropriate.

---

## Automated Workflow

Appointment Booking Workflow:
- Implemented as a native IBM watsonx Orchestrate tool
- Invoked only when a Critical condition is detected
- Requires explicit user consent
- Simulates booking an appointment with the appropriate medical or veterinary consultant
- Does not perform diagnosis or autonomous actions

This demonstrates how agentic AI can safely move from risk assessment to coordinated real-world action.

---

## Demo Scenarios

The system has been tested using:
- Infant health data (critical condition with escalation)
- Dog health data (warning-level monitoring)
- Snake or exotic animal data (scalability across species)

These scenarios demonstrate that the agent architecture is extensible and scalable by design.

---

## Safety and Ethics

- The system is non-diagnostic
- All conclusions are derived strictly from delegated agent outputs
- No assumptions or hallucinations are introduced
- All real-world actions are gated by explicit user consent
- Designed to support caregivers, not replace professionals

---

## Technology Stack

- IBM watsonx Orchestrate
  - Multi-agent orchestration
  - Decision pipelines
  - Automated workflows
- HTML, CSS, JavaScript
  - Frontend demonstration interface
- GitHub Pages
  - Hosting for demo UI

---

## Notes

- This repository focuses on the demo interface.
- Core intelligence, agents, and workflows run entirely within IBM watsonx Orchestrate.
- The architecture is designed for real-world scalability without architectural changes.

---

## License

This project is created for hackathon and educational purposes.

---

## Acknowledgements

Built as part of an IBM agentic AI hackathon using IBM watsonx Orchestrate.
