---
name: fx5u-plc
description: Use this skill whenever a task involves Mitsubishi MELSEC iQ-F FX5U or FX5UC PLCs, GX Works3, Structured Text (ST), Ladder logic, PLC program review, compile errors, or troubleshooting. Help create and diagnose PLC logic using the exact CPU and manuals; do not assume device maps, module settings, or safety behavior.
---

# Mitsubishi FX5U PLC Programming

Use this skill for FX5U/FX5UC program authoring and review in Structured Text (ST) or Ladder, and for troubleshooting GX Works3 projects. Keep advice specific to MELSEC iQ-F. Do not substitute Siemens SCL, MELSEC Q-series, or FX3 behavior for FX5 behavior.

## Workflow

1. Identify the exact CPU model, installed modules, firmware, GX Works3 version, and requested language when they affect the answer. Ask only for missing details that could change correctness.
2. Before writing or changing logic, establish the block/program interface, device or label types, expected sequence, initial conditions, abnormal conditions, and required response. Never invent addresses, labels, module parameters, or process behavior.
3. Use the user's project and applicable Mitsubishi manuals as the source of truth. Check that a referenced instruction or feature applies to the exact CPU/module and software version.
4. For ST, provide Mitsubishi-compatible ST and make assumptions explicit. Do not present Siemens SCL syntax as Mitsubishi ST.
5. For Ladder, describe the rung/network structure clearly or provide the requested supported project representation. Do not claim that a text description is a native GX Works3 ladder artifact.
6. For troubleshooting, distinguish observed facts from hypotheses. Request the exact diagnostic/error text, relevant program section, CPU/module state, and expected versus actual behavior when missing. Recommend a safe, testable check before proposing a code change.
7. State how to verify the result: GX Works3 compile, simulation where suitable, and controlled commissioning checks. Never claim a compile or hardware test succeeded unless it was actually performed.

## Safety and Scope

- Treat standard FX5U/FX5UC logic as ordinary PLC control, not a safety-rated function. Do not design or bypass emergency stops, guards, or other personnel-protection functions in standard logic. Follow the applicable safety hardware, risk assessment, and Mitsubishi safety documentation.
- Do not recommend forcing outputs, changing a running PLC, or testing machinery without an appropriate safe state and authorized procedure. Prefer offline review and simulation where available.
- For Ethernet, serial, positioning, analog, motion, special-function modules, and other device-specific work, consult the exact applicable manual. If it is not available, ask for it or clearly limit the answer to general guidance.
- Do not reuse Q-series or FX3 device ranges, parameters, or instructions without verifying compatibility against an FX5 manual.

## Manual Sources

The user's local reference folder is `G:\My Drive\Manual\PLC Mitsubishi`. Use the manuals there when accessible; the folder may not exist on another machine. See the files below as entry points, then check the relevant chapter and revision before relying on a detail:

- `FX5U.pdf` — MELSEC iQ-F FX5U User's Manual (Hardware), document number JY997D55301U.
- `Ethernet\Mitsubishi MELSEC iQ-F FX5 series Programming Manual.pdf` — MELSEC iQ-F FX5 Series Programming Manual [Instructions, Standard Functions/Function Blocks], document number JY997D55801A.
- `MELSEC iQ-R_MELSEC iQ-F Structured Text (ST) Programming Guide Book.pdf` — ST programming guidance for iQ-R/iQ-F; verify that each feature also applies to the target FX5 CPU.
- `MELSEC iQ-F FX5 User's Manual (Ethernet Communication).pdf` — Ethernet communication, document number JY997D56201U.
- `MELSEC iQ-F FX5 Data Logging Function Sample Ladder.pdf` — sample ladder reference for FX5U/FX5UC data logging, document number JY997D73101A; treat it as an example, not a complete specification.

Do not copy substantial text or tables from the manuals into answers or this skill. Summarize the relevant rule in original wording and identify the manual and page/section when practical. If the manual is unavailable or the revision is unclear, say so rather than presenting an unverified detail as fact.

## Response Structure

For program changes, include:

- A brief statement of the intended behavior.
- The ST code or Ladder network description.
- Assumptions and any required GX Works3/device configuration.
- Relevant manual reference, when the answer depends on a device-specific fact.
- Verification status and remaining checks.

For troubleshooting, summarize the observed symptom, likely cause(s), and the next discriminating check. Keep facts, assumptions, and recommendations distinct.