# Research notes

Reviewed: 2026-10-25. These are external reports and working interpretations. **We have not reproduced them. All project hardware tests: NOT RUN.** Upstream projects can change; record the exact upstream commit before a future build.

## The direction matters

We need a Linux/Pi source to send video to the existing factory receiver. Receiver projects such as [OpenAuto](https://github.com/f1xpl/openauto) and [FastCarPlay](https://github.com/niellun/FastCarPlay) put the receiving role on another device. They are not a direct solution for sending a Pi desktop to the factory screen. A receiver may still be useful as a bench tool if its compatibility and prerequisites are reviewed.

## Candidate sources and evidence

| Source | What it suggests | Limitation for this project |
| --- | --- | --- |
| [AACS README](https://github.com/tomasz-grobelny/AACS) | A Linux source-side path for video to an Android Auto head unit | Its documented development setup is Odroid N2 and Ubuntu 19.10. Treat it as research, not a ready Pi 4 tutorial. |
| [AACS issue 36](https://github.com/tomasz-grobelny/AACS/issues/36) | A contributor reports Pi Zero 2 W video at 480p, with input unresolved | Different hardware, external report, and authentication concerns. It does not prove Pi 4/Tiguan compatibility. |
| [AACS issue 28](https://github.com/tomasz-grobelny/AACS/issues/28) | The maintainer identifies expired authentication keys as a likely connection problem | A build or USB connection can succeed while authentication fails. We will not use extracted or private credentials. |
| [AARE README](https://github.com/prototux/AARE) | A prototype of the phone/source side of Android Auto | The author reports no real-car test and authentication refusal by Google's Desktop Head Unit with its generated certificate. It is not a verified Linux/Pi solution. |
| [Raspberry Pi: USB gadget mode](https://www.raspberrypi.com/news/usb-gadget-mode-in-raspberry-pi-os-ssh-over-usb/) | Official documentation identifies the Pi 4 board's USB-C port for USB device mode | The article demonstrates USB networking. It does not establish Android Auto, CarPlay, or video support on the Tiguan. |

Some upstream discussions propose credential extraction or sharing. Those suggestions are not part of this project's plan. Authentication remains an open feasibility question; a test receiver accepting a certificate would not prove the factory unit accepts it.

## Open questions

- Which exact factory head unit and firmware are involved?
- What OS and kernel are already on the Pi, and what should be preserved?
- Is there a maintainable source implementation with a legitimate authentication path accepted by that unit?
- Can we validate USB enumeration and synthetic video independently on a computer?
- Can the Pi encode video, handle audio/input, and remain stable with suitable power?
- Only after those questions: can YouTube run acceptably in this setup while parked?

The research points toward Android Auto as an area to investigate. No CarPlay source implementation or working vehicle integration has been established here. A clear negative result is an acceptable end to the investigation.
