# Onboarding Guide: Hardware Hacking Safety and Legal Compliance

This guide defines the minimum safety and legal baseline for all M0DUL0 members before hands-on participation in any research, modification, or workshop activity.

## Why This Matters

Hardware hacking involves real physical hazards: fumes, high voltage, flammable materials, and toxic chemicals. Doing it carelessly gets people hurt. Beyond the physical risks, hardware security research sits at the intersection of several Malaysian laws, and unawareness of those laws is not a defence. Both categories — physical safety and legal compliance — are non-negotiable.

---

## Part 1: Physical Workspace Safety

### A) Ventilation

- Always work in a well-ventilated area. Soldering produces fumes from flux and solder alloys that are harmful with prolonged exposure.
- Use a fume extractor when soldering. A desk fan blowing fumes away from your face is the minimum. A proper extractor with a carbon filter is better.
- When using chemical solvents (isopropyl alcohol, acetone, flux remover), ensure active airflow. Do not work with open solvent containers in an enclosed room.
- Hot air rework produces concentrated fumes. Ventilation requirements are higher, not lower, than standard soldering.

### B) Workspace Setup

- Keep your workstation clean and uncluttered before you begin. Loose metal debris, component offcuts, and wire strands on a bench are short-circuit and fire hazards.
- Use an anti-static (ESD) mat and wrist strap when handling PCBs, ICs, and other electrostatic-sensitive components. ESD damage is invisible and irreversible.
- Keep food and drink away from your workspace. Solder, flux, and chemical residues are toxic by ingestion.
- Store tools with sharp edges (scalpels, probes, cutters) safely when not in use.
- Keep a fire extinguisher or fire blanket accessible when working with LiPo batteries or open flames.

### C) Personal Hygiene

- Wash your hands thoroughly before and after every session. Lead-based solder and flux residues are toxic by skin contact and ingestion.
- Do not touch your face, mouth, or eyes while working.
- If working with chemical solvents or cleaning agents, wear nitrile gloves. Change gloves if they become contaminated.
- Wear safety glasses when using hot air stations, soldering iron at high temperature, or any cutting tool.

### D) Electrical Safety

- Never work on live circuits unless you have a specific, justified reason to do so. Power down and discharge capacitors before probing.
- Use a current-limiting bench power supply when powering unknown or untested circuits. Set current limits before connecting to protect both yourself and the device.
- Check voltage and polarity before connecting any supply to a target. Reversing polarity or applying excess voltage destroys devices and can cause fires.
- Do not probe mains voltage (240V AC) circuits unless you are trained and qualified to do so. Mains voltage is lethal.
- Never bypass fuses or protection circuitry on your test equipment.

### E) Chemical and Material Safety

- Flux is an irritant. Avoid prolonged skin contact and do not inhale fumes directly.
- Solder containing lead (Sn63Pb37 or similar alloys) is toxic. Treat it accordingly: ventilate, wash hands, do not eat or drink nearby.
- Isopropyl alcohol (IPA) and acetone are flammable. Keep them away from open flames, hot air stations, and soldering irons.
- Dispose of chemical-soaked materials (cotton swabs, wipes) in a sealed container, not loose in general waste.

### F) Battery Safety

- LiPo (lithium polymer) batteries are a fire and explosion risk if punctured, overcharged, short-circuited, or physically damaged.
- Store LiPo batteries in a fireproof LiPo storage bag when not in use.
- Never charge a swollen, damaged, or leaking battery.
- Discharge LiPo batteries to storage voltage before long-term storage.
- Dispose of batteries at a designated e-waste or battery recycling point. Do not dispose of them in general waste.

---

## Part 2: Malaysian Legal Compliance

Each member is individually responsible for understanding and complying with Malaysian law. The following acts are directly relevant to hardware hacking practice. This is a compliance awareness summary, not legal advice. Seek a qualified advocate and solicitor for legal interpretation.

### Computer Crimes Act 1997 [Act 563]

The most directly applicable law to hardware security research. Key provisions:

- **Section 3**: Unauthorised access to computer material is an offence, regardless of intent. This extends to firmware, embedded systems, and any computing device, not just conventional computers or servers.
- **Section 4**: Unauthorised access with intent to commit a further offence carries heavier penalties.
- **Section 5**: Unauthorised modification of computer material is an offence. This includes writing to flash memory, altering firmware, or injecting code on a device you do not own or have documented permission to test.
- **Section 6**: Wrongful communication of any means of access (passwords, keys, credentials) obtained without authorisation is an offence.

**Practical implication**: Own the device, or have documented, explicit permission from the owner before you touch it. This is not a formality. It is the legal threshold.

### Communications and Multimedia Act 1998 [Act 588]

Governs radio spectrum and network communications. Relevant to RF and SDR work:

- Transmitting on any radio frequency without the appropriate licence or class assignment from MCMC is an offence under the Act.
- Receiving-only SDR use (passive spectrum monitoring) is generally not restricted, but verify against current MCMC spectrum assignments for any frequency you work with.
- Deliberately interfering with radio communications, including Wi-Fi, Bluetooth, or other licensed spectrum, is an offence.

**Practical implication**: Receive and analyse freely. Transmit only with a licence or under a valid MCMC class assignment. Do not jam or disrupt any spectrum.

### Copyright Act 1987 [Act 332]

Relevant to firmware extraction and reverse engineering:

- Firmware is protected as a literary work under Malaysian copyright law. Extracting, copying, or redistributing firmware without authorisation from the rights holder may constitute infringement.
- Decompilation for the purposes of interoperability is a recognised exception, but its boundaries are narrow and fact-specific.
- Applying circumvention tools to bypass TPM, secure boot, or other technological protection measures on a device you do not own may engage both this Act and Act 563.

**Practical implication**: Reverse engineer your own devices or devices you have explicit written permission to analyse. Do not redistribute extracted firmware without legal basis.

### Personal Data Protection Act 2010 [Act 709] and Personal Data Protection (Amendment) Act 2024

Relevant when research surfaces personal data stored on a device:

- Personal data encountered incidentally during research (contacts, credentials, usage logs, location history) is subject to PDPA obligations even if its discovery was unintentional.
- Do not collect, retain, process, or share personal data found on a research device beyond what is strictly necessary to document the finding.
- Do not publish research that includes identifiable personal data without consent or lawful basis.

**Practical implication**: Redact personal data from all writeups, PoCs, and shared artefacts. If a device contains personal data belonging to others, handle it with care and minimise retention.

### Penal Code [Act 574]

General criminal law that intersects with hardware research in several ways:

- **Section 425–440 (Mischief)**: Intentionally destroying or rendering useless any device belonging to another person is an offence, regardless of technical intent.
- **Section 379 (Theft)**: Acquiring a device or component without the owner's consent, even temporarily, for the purpose of extracting data or conducting research is theft.
- **Section 420 (Cheating)**: Misrepresenting yourself to obtain access to a device or system (social engineering for unauthorised research purposes) may engage this provision.

**Practical implication**: Only work on what you own or are authorised to touch. Do not acquire, borrow, or access equipment under false pretences.

### Strategic Trade Act 2010 [Act 708]

Governs the export, transhipment, and transit of strategic goods and dual-use technology:

- Certain hardware security tools fall under dual-use technology classifications: spectrum analysers, signal generators, certain RF equipment, and some testing instruments may be listed as controlled items under the Strategic Trade (Strategic Items) Order 2010.
- Exporting, transhipping, or transferring such tools or technical knowledge internationally without a MITI permit where one is required is an offence.
- Sharing technical knowledge, training materials, or research with foreign nationals or organisations involving controlled technology (including by email or cloud storage) may constitute an intangible technology transfer (ITT) under this Act.

**Practical implication**: If you are importing, exporting, or sharing hardware security tools or research internationally, check the Strategic Items list at miti.gov.my before proceeding.

### Occupational Safety and Health Act 1994 [Act 514]

Governs safe practice in any workspace, including home labs and community workshops:

- Under Section 24, every person at a workplace has a duty to take reasonable care of their own safety and health and that of others who may be affected by their work.
- This duty applies whether the workspace is a formal lab, a community workshop, or a home setup.
- When M0DUL0 runs live workshops, organisers have additional duties as occupiers of the premises under Section 18 to ensure the space is safe for all participants.

**Practical implication**: Follow the physical safety steps in Part 1 of this guide. They are not optional good practice. For anyone running a workshop, those duties are backed by law.

### Electricity Supply Act 1990 [Act 447]

Governs the supply and use of electricity in Malaysia:

- Unauthorised interference with electrical supply infrastructure or licensed electrical installations is an offence.
- Modifications to mains wiring, building electrical systems, or any infrastructure connected to the national grid without a licensed wireman or electrical engineer are prohibited.

**Practical implication**: Bench-level work on low-voltage embedded systems is standard practice. Mains voltage work is not. Do not modify or work on mains-connected infrastructure without a licensed professional.

### Environmental Quality Act 1974 [Act 127]

Governs the disposal of hazardous waste, including e-waste and chemical materials:

- Improper disposal of electronic components, PCBs, batteries, and chemical solvents is regulated. Disposal into general waste or drains may constitute an offence.
- Dispose of e-waste at designated recycling points. Most municipal councils in Malaysia maintain scheduled e-waste collection programmes.
- Dispose of chemical materials (solvents, flux, cleaning agents) according to their safety data sheets.

**Practical implication**: Do not bin PCBs, batteries, or chemical-soaked materials in general household waste.

---

## Part 3: Responsible Disclosure

If your research uncovers a vulnerability in a vendor product:

1. Do not publish before notifying the vendor.
2. Contact the vendor or maintainer privately with a clear description of the finding and the affected product.
3. Give them a reasonable window to respond and patch before releasing technical details publicly.
4. If the vendor does not respond within a reasonable timeframe, escalate through established channels (national CERT, MYCERT, or community moderation) before publishing.
5. When publishing, share enough for the community to understand and learn from the finding without providing a ready-made attack against unpatched, deployed devices.

Refer to OWASP's [Vulnerability Disclosure Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Vulnerability_Disclosure_Cheat_Sheet.html) for the full playbook.

---

## Operational Guidance

- Use a consistent community handle across Discord and GitHub. You do not need to use your real name.
- Do not share extracted firmware, credentials, or device data in community channels without completing the redaction steps in [CONTRIBUTING.md](../CONTRIBUTING.md).
- Report suspicious or unsafe behaviour to a Volunteer or Core Founding Team member directly.

Completion of this guide is part of M0DUL0 onboarding readiness.

## Moderation Note

All activity remains subject to [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md) and [DISCLAIMER.md](../DISCLAIMER.md).
