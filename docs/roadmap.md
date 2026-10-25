# Roadmap

Every stage is unchecked. **All hardware tests: NOT RUN.** These are questions to investigate, not instructions known to work.

- [ ] **1. Inventory and preserve.** Identify the Pi revision/RAM, microSD, OS, power supply, data cable, and test computer. Review and back up existing microSD contents before any changes. Record only non-identifying head-unit model and firmware details. Success: a complete inventory and a recoverable starting point.
- [ ] **2. Review the source and authentication path.** Understand which component sends video, its build requirements, licensing, and how authentication would work. Success: a reproducible candidate path that uses credentials we are entitled to use. If none is available, record the blocker and stay on the bench.
- [ ] **3. Observe USB device enumeration on a computer.** Plan a supported Pi 4 USB-C device-mode experiment after checking power and cabling. Success: the computer identifies the intended USB device, with a repeatable connect/disconnect result. This would prove USB transport only.
- [ ] **4. Send synthetic video to a test receiver.** Choose a suitable computer-based receiver and a small generated test pattern. Success: a stable, repeatable image with the software versions, resolution, and test duration recorded. No YouTube account is needed for this stage.
- [ ] **5. Check audio, input, and reliability.** Test a generated tone, input events, repeated connections, and clean shutdown. Success: documented results and known limitations, with a safe power arrangement and recovery procedure.
- [ ] **6. Evaluate the factory screen while safely parked.** Prerequisites: reliable bench results, identified head unit, appropriate power/cabling, and compatible legitimate authentication. Success: synthetic video works without changing driving restrictions or disrupting normal vehicle functions. Stop on unexpected behavior.
- [ ] **7. Explore YouTube playback.** Only after the earlier stages pass, investigate browser playback, network access, controls, audio/video sync, and performance while parked. Success: an observed result with limitations; no promise that it will work.

Use the [experiment template](../experiments/TEMPLATE.md) for each attempt. Mark a stage complete only when its evidence is recorded. A failed test or an authentication blocker is a useful result, not a reason to skip a prerequisite.
