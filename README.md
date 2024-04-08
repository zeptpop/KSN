# KSN
Software Defined Radio: FM-Radioempfänger

## Mitglieder:

Bhuiyan Rifaz

Culap Paul

Garcia Sharon

## Beschreibung:
Ein FM-Radioempfänger empfängt Signale, die mit der Frequenzmodulation (FM) moduliert sind. In FM-Radiosendern wird die Information durch die Änderung der Frequenz des Trägersignals übertragen. Der Empfänger muss dieses modulierte Signal demodulieren, um die ursprüngliche Information (z. B. Musik oder Sprache) wiederherzustellen.
## Anleitung:

### Was ist GNU Radio?

GNU Radio ist eine kostenlose und Open-Source-Software-Entwicklungstoolbox, die es ermöglicht, Software-Defined Radio (SDR) Systeme zu erstellen. Mit GNU Radio können Benutzer Signale digital verarbeiten und Funkanwendungen entwickeln.

### Aufbau des FM-Receivers:
**Schritt 1: Installation von GNU Radio**

Zuerst müssen Sie GNU Radio auf Ihrem Computer installieren. Anweisungen zur Installation finden Sie auf der offiziellen Website von GNU Radio.

**Schritt 2: Öffnen Sie GNU Radio Companion (GRC)**

GRC ist eine grafische Benutzeroberfläche, die mit GNU Radio geliefert wird und es ermöglicht, Fließdiagramme für die Signalverarbeitung zu erstellen.

**Schritt 3: Erstellen Sie das Empfänger-Flussdiagramm**

* Ziehen Sie einen File Source-Block in das Hauptfenster von GRC. Dieser Block liest die Audiodatei vom Lehrer.
* Ziehen Sie einen Low Pass Filter-Block in das Fenster. Konfigurieren Sie den Tiefpassfilter mit einer Grenzfrequenz von etwa 40 kHz.
* Ziehen Sie einen WBFM Receive-Block in das Fenster. Dieser Block demoduliert das FM-Signal.
* Ziehen Sie einen Audio Sink-Block in das Fenster, um das demodulierte Audio abzuspielen.
* Ziehen Sie einen Frequency Sink-Block und einen Waterfall Sink-Block in das Fenster, um die Spektralanzeige und das Wasserfalldiagramm zu visualisieren.

Verbinden Sie die Blöcke entsprechend, um das Flussdiagramm zu vervollständigen.

**Schritt 4: Konfigurieren Sie die Parameter**

Stellen Sie sicher, dass die Parameter der Blöcke korrekt konfiguriert sind. Konfigurieren Sie den Tiefpassfilter mit einer Grenzfrequenz von ca. 40 kHz.

### Was sollte herauskommen:

Nachdem Sie das Flussdiagramm erstellt und die Parameter konfiguriert haben, sollten Sie in der Lage sein, den FM-Receiver auszuführen. Das Ergebnis sollte ein hörbares Audioausgangssignal sein, das den Radiosender wiedergibt, den Sie ausgewählt haben.

## Screenshots:
![Flowgraph](/Bilder/flowgraph.png)

![listen radio](/Bilder/frequency_range_waterfall_sink.png)

