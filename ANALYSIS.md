# 🔍 UX Audit: Send Communication Workflow Analysis

This document provides a detailed analysis of the "Send Communication" setup process. The audit focuses on identifying logic errors and UI inconsistencies that could lead to user confusion and operational errors in the final product.

---

## 🚩 Finding 1: Incorrect Trigger Card Generation
**Issue:** When the option *"Schedule right now & on refreshing the campaign"* is selected, the system generates an incorrect number of trigger cards.

- **Expected Behavior:** A single combined trigger condition should result in one trigger card in the workflow.
- **Actual Behavior:** The system generates two separate cards: one for `Refresh settings` and one for `Trigger and segment`.
- **Impact:** This creates redundancy in the workflow and confuses the user regarding the actual starting point of the automation.
- **Evidence:** `screenshots/trigger-count-error.png`

---

## 🚩 Finding 2: UI Labeling Inconsistency
**Issue:** The naming of the configuration step is inconsistent across different design versions of the same modal.

- **Observed Discrepancy:** In some instances, the step is labeled as **"Configure action & trigger conditions"**, while in others, it is labeled as **"Choose trigger"**.
- **Impact:** Inconsistent terminology increases cognitive load for the user and suggests a lack of design synchronization.
- **Evidence:** `screenshots/label-inconsistency.png`

---

## 🚩 Finding 3: Modal vs. Workflow Representation Mismatch
**Issue:** There is a terminology mismatch between the setup modal and the final generated workflow card.

- **Observed Discrepancy:** The modal lists the trigger as **"Trigger #1: Choose date and time"**, but the corresponding card in the workflow is named **"Trigger and segment"**.
- **Impact:** This creates a "gap" in the user's mental model, making them question if the configuration they set in the modal was correctly applied.
- **Evidence:** `screenshots/modal-workflow-mismatch.png`

---

## 🚩 Finding 4: Downstream Workflow Divergence
**Issue:** Selecting a "Refresh" option triggers a mandatory downstream action that is absent in the standard "Schedule now" flow.

- **Observed Discrepancy:** Choosing the "Refresh" option forces the addition of a **"Send an internal notification"** block.
- **Impact:** This creates a divergent user experience. If this notification is critical, it should be an optional setting rather than a hard-coded requirement that alters the structural flow of the campaign.
- **Evidence:** `screenshots/downstream-divergence.png`
