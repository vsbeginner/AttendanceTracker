<div align="center">

# Attendance Tracker — Python CLI Application
### Automated Classroom Record Telemetry, Input Validation & File I/O Persistence

[![Python](https://img.shields.io/badge/Python-3.8%20%7C%203.9%20%7C%203.10%20%7C%203.11-3776AB.svg?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![CLI](https://img.shields.io/badge/Interface-Interactive%20Terminal-4D4D4D.svg?style=for-the-badge&logo=gnubash&logoColor=white)](https://en.wikipedia.org/wiki/Command-line_interface)
[![File I/O](https://img.shields.io/badge/Storage-Persistent%20Disk%20Export-blue.svg?style=for-the-badge)](https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

<p align="center">
  <b>A lightweight, zero-dependency Python command-line utility for institutional attendance tracking and reporting.</b><br>
  Built with sanitizing input validation loops, in-memory roster aggregation, formatted terminal matrices, and persistent text log exports.
</p>

---

</div>

## Executive Summary

Manual attendance recording in academic and corporate settings is prone to clerical errors, misplaced paper logs, and tedious manual reconciliation.

**Attendance Tracker** is a streamlined terminal-based productivity utility that automates student roll-call workflows. The script enforces defensive validation on candidate name strings (rejecting whitespace-only and malformed entries), compiles session attendance records in-memory, dynamically renders tabular verification summaries, and serializes final attendance manifests directly to structured disk files (`attendance_log.txt`) for archival integrity.

---

## Architectural Workflow & State Validation

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                              TERMINAL ATTENDANCE SESSION                               │
└────────────────────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
                       ┌─────────────────────────┐
                       │  Input Collection Loop  │
                       │  (Student Name Prompt)  │
                       └─────────────────────────┘
                                    │
                                    ▼
                       ┌─────────────────────────┐
                       │ Input Sanitizer Guard   │ ◄── Rejects Empty / Whitespace Entries
                       └─────────────────────────┘
                                    │
                                    ▼
                       ┌─────────────────────────┐
                       │ In-Memory Roster Map    │ ──► Tracks Present/Absent Status
                       └─────────────────────────┘
                                    │
                                    ▼
                       ┌─────────────────────────┐
                       │ Session Summary HUD     │ ──► Formatted Terminal Matrix
                       └─────────────────────────┘
                                    │
                                    ▼
                       ┌─────────────────────────┐
                       │ File Persistence Engine │ ──► Appends to `attendance_log.txt`
                       └─────────────────────────┘
```

---

## Core Technical Features

| Feature Module | Technical Implementation | Operational Benefit |
|:---|:---|:---|
| **Defensive Validation** | String normalization and non-empty checks rejecting empty/whitespace inputs. | Prevents silent roster corruption from accidental return key presses. |
| **In-Memory Tracking** | Structured Python dictionaries maintaining student identifier keys and attendance flags. | Fast, constant-time $O(1)$ lookups and status mutations during live sessions. |
| **Tabular Summary Matrix** | Dynamic string formatting with column alignment and border separators. | Provides immediate visual verification for educators before session termination. |
| **Persistent File Log** | Safe file context managers (`with open(...) as f:`) writing records to disk. | Guarantees file handle finalization and persistent audit logs. |
| **Zero External Deps** | Pure Python standard library implementation with zero third-party requirements. | Runs out-of-the-box on any standard Python 3.x installation. |

---

## Quickstart & Local Execution

```bash
# Clone the repository
git clone https://github.com/vsbeginner/AttendanceTracker.git
cd AttendanceTracker

# Execute using Python 3
python tracker.py
```

### Example Terminal Session:
```text
====================================================
           ATTENDANCE TRACKER CLI
====================================================
Enter student name (or type 'done' to finalize): Rahul Sharma
[STATUS: Present] Recorded: Rahul Sharma

Enter student name (or type 'done' to finalize): Priya Singh
[STATUS: Present] Recorded: Priya Singh

Enter student name (or type 'done' to finalize): done

====================================================
             FINAL ATTENDANCE SUMMARY
====================================================
Total Students Present : 2
Report Export Target   : attendance_log.txt
Status                 : Successfully Serialized to Disk
====================================================
```

---

## Candidate Profile & Institutional Details

- **Candidate Name**: Vinayak Sharma
- **Enrollment / Roll No**: 2501940012
- **GitHub Profile**: [@vsbeginner](https://github.com/vsbeginner)
- **LinkedIn Profile**: [Vinayak Sharma](https://www.linkedin.com/in/vinayak-sharma-24a8aa384/)
- **Email Contact**: vsbeginner14@gmail.com
- **Degree Program**: Master of Computer Applications (MCA)
- **Institution**: Department of Computer Science & Engineering, K.R. Mangalam University

---

<div align="center">
  <sub>Developed for academic excellence and technical portfolio showcase. Licensed under the <a href="LICENSE">MIT License</a>.</sub>
</div>
