# smartctl.8
smartctl.8

# SmartDrive Inspector

SmartDrive Inspector to natywna aplikacja GTK dla systemu Linux, która
przedstawia stan i dane diagnostyczne raportowane przez `smartctl` w czytelnym
interfejsie graficznym. Obsługuje dyski ATA/SATA, NVMe oraz SCSI/SAS.

English documentation: DOWN 

## Funkcje

- Wykrywanie fizycznych dysków i prezentowanie ich stanu SMART.
- Atrybuty ATA, dane kondycji NVMe, temperatura, czas pracy i najważniejsze
  parametry dysku.
- Wyróżnianie typowych sygnałów ostrzegawczych, np. sektorów przeniesionych
  lub oczekujących na remapowanie.
- Uruchamianie krótkich, rozszerzonych i transportowych autotestów, jeśli dysk
  je obsługuje.
- Historia autotestów oraz pełny raport JSON z `smartctl`.
- Polski interfejs oraz polskie metadane widoczne w menu aplikacji.

## Instalacja

Pobierz plik `SmartDrive-Inspector_1.0.0_all.deb` z tego repozytorium i
zainstaluj go w systemie opartym na Debianie lub Ubuntu:

```bash
sudo apt install ./SmartDrive-Inspector_1.0.0_all.deb
```

Pakiet instaluje polecenie `smartdrive-inspector` oraz pozycję **SmartDrive
Inspector** w menu aplikacji.

## Wymagania

Pakiet deklaruje i instaluje, jeśli są dostępne w repozytoriach systemu,
następujące zależności:

- Python 3.10 lub nowszy
- GTK 3 oraz PyGObject
- `smartmontools`
- PolicyKit (`pkexec`)

## Korzystanie z aplikacji

Otwórz **SmartDrive Inspector** z menu aplikacji, wybierz dysk i poczekaj na
wczytanie raportu. Odczyt danych SMART oraz uruchamianie i przerywanie
autotestów mogą wymagać uwierzytelnienia administratora — aplikacja wyświetli
standardowe okno systemowe.

Wyniki SMART są przydatne diagnostycznie, ale nie zastępują regularnych kopii
zapasowych. Gdy dysk zgłasza ostrzeżenie krytyczne, jak najszybciej wykonaj
kopię ważnych danych.

## Licencja

Zapoznaj się z warunkami licencji dołączonych komponentów oraz ich projektów
źródłowych.


# SmartDrive Inspector

SmartDrive Inspector is a native GTK application for Linux that presents the
health and diagnostic data reported by `smartctl` in a clear graphical
interface. It supports ATA/SATA, NVMe, and SCSI/SAS drives.

Polish documentation: UPP

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
