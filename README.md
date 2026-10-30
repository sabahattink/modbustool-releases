# ModbusTool

Modbus commissioning tool for Windows, for building-automation engineers: read, write, scan and diagnose Modbus TCP
and RTU devices on site, and test your BMS against a simulated device before the hardware arrives.

**Product page, pricing and Pro licenses:** https://sabahattinkalkan.com/modbustool/

This repository publishes the releases (downloads and release notes). The source code is not public.

## Download

Get the latest ZIP from [Releases](https://github.com/sabahattink/modbustool-releases/releases/latest) or from the
[product page](https://sabahattinkalkan.com/modbustool/#download). Each release lists the SHA-256 of the ZIP; check it
before running:

```powershell
Get-FileHash .\ModbusTool-2.1.0-win-x64.zip -Algorithm SHA256
```

- Windows 10 or 11, 64-bit. Self-contained: no installer, no .NET to install.
- Unzip and run `ModbusTool.exe`. `ModbusSimulator.exe` is a demo Modbus TCP server with three devices, to try
  everything without hardware (`ModbusSimulator.exe --port 1502`, then connect to `127.0.0.1:1502`).
- The executables are not code-signed yet, so Windows SmartScreen may ask you to confirm the first start
  (More info → Run anyway).

## Free and Pro

| | Free | Pro |
|---|:---:|:---:|
| Modbus TCP, RTU (serial) and RTU over TCP | ✓ | ✓ |
| Read and write FC01–06, 15, 16; eight data types, four byte orders | ✓ | ✓ |
| Write lock, read-back verification and one-click undo | ✓ | ✓ |
| Slave ID and register scanning, FC43 device identity | ✓ | ✓ |
| Communication quality per slave and raw TX / RX frames | ✓ | ✓ |
| Polling with trend, bit grid, labels, profiles and CSV export | ✓ | ✓ |
| Twelve languages, dark and light theme | ✓ | ✓ |
| Point list with engineering units, CSV import with Modicon addresses | | ✓ |
| Long-term CSV recording | | ✓ |
| Passive RS-485 bus monitor | | ✓ |
| Slave (server) mode over TCP and RTU | | ✓ |
| Commissioning report (HTML, prints to PDF) | | ✓ |

Pro is 49 USD per seat, one-time, with 12 months of updates. The license key is verified offline; no account, no
telemetry. Buy it on the [product page](https://sabahattinkalkan.com/modbustool/#pricing).

## Safety

ModbusTool is a commissioning and diagnostic tool, not a control system. Writes are locked by default and verified by
reading back. Do not write to, command or simulate life-safety systems (fire detection, suppression, voice evacuation)
without the system owner's authorisation and the applicable procedures.

## License and support

ModbusTool is proprietary software, © 2026 Sabahattin Kalkan. Use is governed by the
[End User License Agreement](https://sabahattinkalkan.com/modbustool/terms/) included in every ZIP (`EULA.md`).
Third-party components are listed in `THIRD-PARTY-NOTICES.txt`.

Questions and bug reports: hello@sabahattinkalkan.com
