# KSN
Software Defined Radio: FM-Radioempfänger

## Mitglieder:
Garcia Sharon

## Beschreibung:
Ein FM-Radioempfänger empfängt Signale, die mit der Frequenzmodulation (FM) moduliert sind. In FM-Radiosendern wird die Information durch die Änderung der Frequenz des Trägersignals übertragen. Der Empfänger muss dieses modulierte Signal demodulieren, um die ursprüngliche Information (z. B. Musik oder Sprache) wiederherzustellen.

### Aufbau des FM-Receivers:

Um diesen FM-Radioempfänger zu bauen, verwenden wir verschiedene Blöcke in GNU Radio, die jeweils eine spezifische Funktion erfüllen:

1. **File Source Block:**
   - Dieser Block wird verwendet, um die Datendatei "radio.dat" einzulesen, die die Radiosignale enthält.

2. **Signal Source Block:**
   - Dieser Block erzeugt ein Sinuswellensignal mit der Mittenfrequenz des Empfängers (91 MHz), das als Referenzsignal für die Modulation dient.

3. **Multiply Block:**
   - Dieser Block moduliert das empfangene Signal mit dem Referenzsignal, um das Signal für die Frequenzverschiebung vorzubereiten.

4. **Low Pass Filter Block:**
   - Dieser Block filtert hochfrequente Komponenten des Signals heraus und trennt die gewünschten Signale von den unerwünschten. Der Filter wird vor dem Demodulator platziert.

5. **WBFM Receive Block:**
   - Dieser Block demoduliert das FM-Signal und extrahiert das Audiosignal. Wir verwenden den "WBFM Receive" Block für die Breitband-FM-Demodulation.

6. **Audio Sink Block:**
   - Dieser Block gibt das demodulierte Audiosignal über die Soundkarte wieder, sodass es über Lautsprecher gehört werden kann.

7. **Frequency und Waterfall Sink Blocks:**
   - Diese Blöcke dienen dazu, das Eingangssignal zu visualisieren und dessen Frequenzspektrum darzustellen.

Bei der Bestimmung der Parameter wie Gain, Decimation usw. müssen wir die Eigenschaften des Signals, die Systemanforderungen und die Hardwarekonfiguration berücksichtigen:

- Der Gain-Parameter beim Low Pass Filter bestimmt die Verstärkung des Filters und sollte so eingestellt werden, dass das Signal angemessen verstärkt wird, ohne zu übersteuern oder zu schwach zu sein.
- Die Decimation beim Low Pass Filter reduziert die Abtastrate des Signals und beeinflusst die Rechenleistung. Eine geeignete Decimation wird basierend auf der Abtastrate des Eingangssignals gewählt.
- Die Audio-Decimation beim WBFM Receive Block bestimmt die Abtastrate des demodulierten Audiosignals und sollte so gewählt werden, dass das Audiosignal mit der gewünschten Qualität wiedergegeben wird.

Durch die Auswahl und Anpassung dieser Parameter können wir einen funktionierenden FM-Radioempfänger in GNU Radio aufbauen und das gewünschte Radiosignal demodulieren und wiedergeben.

### Was sollte herauskommen:

Nachdem Sie das Flussdiagramm erstellt und die Parameter konfiguriert haben, sollten Sie in der Lage sein, den FM-Receiver auszuführen. Das Ergebnis sollte ein hörbares Audioausgangssignal sein, das den Radiosender wiedergibt, den Sie ausgewählt haben.

## Screenshots:
![flow](/Bilder/flowgraph.png)
![radio](/Bilder/frequency_range_waterfall_sink.png)

