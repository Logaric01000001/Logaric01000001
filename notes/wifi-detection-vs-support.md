# Wi-Fi detection is not hardware support

Recognizing a USB ID is only the start of making an adapter useful. In Antena, several different questions have to be answered:

1. Is the USB device visible?
2. Is there a recipe for its chipset?
3. Is the expected driver available and loaded?
4. Has a wireless interface appeared?
5. Can NetworkManager actually scan with it?

A match at step one does not prove step five. A driver advertised by the kernel does not prove that a particular adapter has been tested with this app.

The AIC8800D80 recipe also distinguishes storage, transition and operational USB identities. That is why a single “supported” label would hide useful information.

The public README records which observations came from hardware and which paths were exercised with simulations. The installation path was not rerun on the already functioning development adapter. More hardware observations are still needed; automated tests cannot supply them.

## Read the implementation

- [Detection](https://github.com/Logaric01000001/antena-arch/blob/main/antena/core/detect.py)
- [Diagnostics](https://github.com/Logaric01000001/antena-arch/blob/main/antena/core/diagnose.py)
- [Tests](https://github.com/Logaric01000001/antena-arch/tree/main/tests)
- [Limitations](https://github.com/Logaric01000001/antena-arch#limitaciones-conocidas-011)

If you report a hardware observation, include the chipset or USB ID, driver, kernel and steps performed. Remove SSIDs, MAC addresses, serial numbers and other personal details. A failed test is useful evidence too.
