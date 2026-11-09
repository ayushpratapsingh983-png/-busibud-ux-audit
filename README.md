# -busibud-ux-audit

# Busibud Send Communication Workflow Analysis

This repository contains a detailed UX/UI audit of the "Send Communication" feature as part of the Full Stack Developer recruitment process at Busibud.

## 🎯 Objective
The goal of this analysis was to identify logic gaps, UI inconsistencies, and workflow errors within the "Send Communication" modal and its resulting automated workflows.

## 🔍 Key Findings
I identified four primary issues affecting the user experience:
1. **Trigger Logic Error:** Incorrect number of trigger cards generated for specific Q1 options.
2. **UI Inconsistency:** Inconsistent labeling of the configuration steps across different design files.
3. **Modal-to-Workflow Mismatch:** Discrepancy between the trigger name in the setup modal and the final workflow card.
4. **Downstream Divergence:** Mandatory internal notifications added to some flows but not others, creating an inconsistent user journey.

## 📂 Repository Structure
- `ANALYSIS.md` - Detailed breakdown of each finding, the logic behind the error, and suggested fixes.
- `/screenshots` - Visual evidence of the identified bugs.
