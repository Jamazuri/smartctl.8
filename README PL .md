# SmartDrive Inspector

SmartDrive Inspector is a native GTK application for Linux that presents the
health and diagnostic data reported by `smartctl` in a clear graphical
interface. It supports ATA/SATA, NVMe, and SCSI/SAS drives.

Polish documentation: [README.pl.md](README.pl.md)

## Features

- Detects physical drives and displays their SMART health information.
- Shows ATA attributes, NVMe health data, temperature, power-on time, and
  other key metrics.
- Highlights common warning signals, such as reallocated or pending sectors.
- Runs short, extended, and conveyance self-tests when the drive supports
  them.
- Displays self-test history and the complete JSON report from `smartctl`.
- Includes a Polish interface and Polish desktop-menu metadata.

## Installation

Download `SmartDrive-Inspector_1.0.0_all.deb` from this repository and install
it on a Debian- or Ubuntu-based system:

```bash
sudo apt install ./SmartDrive-Inspector_1.0.0_all.deb
```

The package installs the `smartdrive-inspector` command and an application-menu
entry named **SmartDrive Inspector**.

## Requirements

The package declares and installs the following dependencies when available
from your distribution repositories:

- Python 3.10 or newer
- GTK 3 and PyGObject
- `smartmontools`
- PolicyKit (`pkexec`)

## Using the application

Open **SmartDrive Inspector** from the application menu, choose a drive, and
wait for its report to load. Reading SMART data and starting or stopping a
self-test can require administrator authentication; the application requests
it through the normal system dialog.

SMART results are useful diagnostics, but they do not replace regular backups.
If a drive reports a critical warning, back up important data as soon as
possible.

## License

See the license terms of the included components and their respective upstream
projects.
