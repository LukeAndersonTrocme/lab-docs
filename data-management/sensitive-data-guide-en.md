# Sensitive Research Data: Student Onboarding Guide

Not all research labs work with sensitive data. A project studying insect populations or forest cover relies on data that carries little meaningful privacy risk. Our lab is different. Because we work with human genealogical data — and sometimes with health records and DNA — the individuals and families represented in our datasets have a real stake in how their information is handled. Many of these individuals are living; others have living descendants. The legal frameworks we operate under exist for good reason, and so does this guide. Understanding how to work responsibly with sensitive data is not just a regulatory obligation: it is a form of respect for the people behind the records.

> **Key rule:** The project data is confidential and must remain on the Digital Research Alliance (Compute Canada) clusters at all times. Aggregate summary statistics may be exported. When in doubt, ask the PI before acting.

---

## Before You Start: Onboarding Checklist

*Complete the following before accessing any project data.*

- [ ] Read UdeM's [data confidentiality level guide (PDF)](https://vie-privee.umontreal.ca/fileadmin2/vie-privee/documents/exemples-rp.pdf). Pay particular attention to Level 4 examples (health records, DNA) to understand where our data sits on the sensitivity spectrum.
- [ ] Complete the **TCPS 2: CORE-2022** online ethics training (~4 hrs) at [tcps2core.ca](https://tcps2core.ca/welcome). The certificate is worth keeping — it is a recognized credential that follows you beyond this lab and strengthens any future research ethics application.
- [ ] Read this guide in full.
- [ ] Confirm your **Digital Research Alliance** (Compute Canada) account is active and that the PI has provisioned your access to the project directories.
- [ ] Verify which files and directories you are authorized to access — confirm this with the PI.

---

## Guiding Principles

These are not bureaucratic rules. They are habits worth developing for any future work with human data.

**DNA and health records are among the most sensitive data a researcher can handle.** UdeM classifies them at Level 4 out of 5.  Treat them accordingly.

**The structure of the genealogy is itself sensitive.** Even without names, knowing who is related to whom — or which families carry certain genetic traits — can expose deeply private information about real people and their living relatives. A pedigree is not a neutral data structure.

**Before transferring anything off the cluster, pause.** Ask yourself: "Am I explicitly authorized to transfer this?" Not "I think it's probably fine". If you are not certain, ask the PI first. The cost of asking is zero. The cost of a breach is not.

**When in doubt, do nothing and ask.** This applies to data transfers, sharing outputs, using new tools, or anything else that involves data leaving its authorized environment. Caution is always the right default.

---

## 1. Legal & Regulatory Framework

### Quebec Law 25 (*Loi 25*)

Quebec's *Loi 25 — Loi modernisant des dispositions législatives en matière de protection des renseignements personnels*, fully in force since September 2023, significantly strengthens privacy obligations for all Quebec organizations, including universities. Key points relevant to research:

- **Privacy impact assessments (ÉFVP — *Évaluation des facteurs relatifs à la vie privée*)** are legally required for projects involving the collection, creation, or reuse of personal information. Because this project reuses existing data rather than collecting new data, an ÉFVP may not be required — but the PI must confirm this. Contact the UdeM privacy office for guidance: [vie-privee@umontreal.ca](mailto:vie-privee@umontreal.ca).
- Access to personal information must be restricted to authorized personnel only.
- Data breaches must be reported to the *Commission d'accès à l'information* (CAI) and to affected individuals.

### TCPS 2 — Tri-Council Policy Statement on Research Ethics

Canada's national framework for ethical research involving human participants. All universities receiving federal tri-council funding (NSERC, SSHRC, CIHR) are bound by it.

The **CORE-2022** online tutorial at [tcps2core.ca](https://tcps2core.ca/welcome) is free, self-paced (~4 hrs), and covers privacy, consent, data security, and research involving Indigenous communities. The certificate of completion is typically required for Research Ethics Board (*Comité d'éthique de la recherche* — CÉR) applications; retain your copy.

### UdeM Institutional Policies

The following UdeM policies govern how information must be handled. The [research data protection guide](https://vie-privee.umontreal.ca/proteger-les-donnees-de-recherche/) links to the full text of each.

---

## 2. About This Lab's Data

### Type of data

This lab works with genealogical records compiled by the Balsac genealogy. Records may include identifiers, dates of birth/death/marriage, family relationships, geographic information, and material drawn from historical censuses, civil registrations, and notarial records. Some records may be linked to or include health and DNA data.

Even when derived from historical sources, genealogical data can contain **personal information about living individuals or recent descendants** and must be treated as sensitive.

### What can be shared

| Data type | Permitted? |
|-----------|------------|
| Summary / aggregate statistics (counts, rates, distributions) | ✓ Yes — may be exported |
| Anonymized outputs where re-identification is not reasonably possible | ✓ With PI approval |
| The structure of genealogical relationships (pedigrees, family networks) | ✗ Sensitive — must remain on the cluster |
| Individual-level records, even in modified form | ✗ Must remain on the cluster |
| Raw data files | ✗ Must remain on the cluster |

If you are unsure whether a specific output is exportable, ask the PI.

---

## 3. Data Storage

### Primary: Digital Research Alliance (Compute Canada) Clusters

The project data lives on Alliance clusters. It must **not** be transferred to:

- Personal laptops or desktops
- Personal cloud services (Google Drive, Dropbox, iCloud, OneDrive, etc.)
- USB drives or external hard drives
- Email attachments

All analysis should be conducted directly on the cluster via SSH or through authorized remote interfaces. Do not stage data locally even temporarily.

### Secondary: The Lab Workstation ("TrashMac")

The lab has one dedicated desktop workstation at UdeM — an encrypted machine with an anti-theft device installed. In specific cases, some data may be stored or processed here. **This requires explicit PI approval in advance.** Do not copy data to the TrashMac without first confirming with the PI.

---

## 4. Workstation & Access

If you are working from a **personal laptop**, no sensitive data should ever be stored on it. All access to project data must go through the Alliance cluster via SSH, JupyterHub, or another authorized remote interface. Your laptop is a terminal — not a storage location.

Do not share your cluster login credentials with anyone.

---

## 5. AI Tools

Do not submit any sensitive project data to AI tools — including but not limited to Claude, ChatGPT, GitHub Copilot, or any other assistant that processes or transmits data externally.

This includes:

- Pasting data records into a chat interface
- Uploading data files to an AI service
- Using AI coding assistants that may send code context containing embedded data to external servers

Code and summary statistics without embedded data are generally fine. If you are unsure whether a specific tool or use case is permitted, ask the PI first.

---

## 6. Reporting a Concern

If you suspect a data breach, unauthorized access, or accidental disclosure — or if you are simply unsure whether a planned action is permitted:

1. **Stop the action immediately.**
2. Notify the PI as soon as possible.
3. The PI will escalate to UdeM's privacy office as required: [vie-privee@umontreal.ca](mailto:vie-privee@umontreal.ca)

Do not attempt to investigate or remediate a breach on your own.

---

## 7. Key Resources

| Resource | Link |
|----------|------|
| TCPS 2: CORE-2022 ethics training | [tcps2core.ca](https://tcps2core.ca/welcome) |
| UdeM data confidentiality level guide (PDF) | [vie-privee.umontreal.ca](https://vie-privee.umontreal.ca/fileadmin2/vie-privee/documents/exemples-rp.pdf) |
| UdeM research data protection guide | [vie-privee.umontreal.ca](https://vie-privee.umontreal.ca/proteger-les-donnees-de-recherche/) |
| Alliance Sensitive Data Toolkit — Part 1: Glossary | [Zenodo](https://zenodo.org/records/4088946) |
| Alliance Sensitive Data Toolkit — Part 2: Risk Matrix | [Zenodo](https://zenodo.org/records/4088954) |
| Alliance training resources (RDM) | [alliancecan.ca](https://www.alliancecan.ca/en/our-services/research-data-management/learning-resources/training-resources) |
| UdeM privacy office | [vie-privee@umontreal.ca](mailto:vie-privee@umontreal.ca) |

---

*Last updated: 2026-03-13. Maintained by the PI. Questions? Contact the PI or the UdeM privacy office.*
