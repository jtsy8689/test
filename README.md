# 	 Geländedarstellung und 3D-Datenvisualisierung WiSe 26/27
## EP01 | Geländedarstellung I

### Digitales Höhenmodelll des nevado de toluca
<img width="3508" height="2480" alt="image" src="https://github.com/user-attachments/assets/3c3065c2-a6b5-435f-8e23-aee98a5d86f5" />

### 3D-Reliefanalyse eines Stratovulkans

Diese Arbeit befasst sich mit der digitalen Geländedarstellung des mexikanischen Stratovulkans Nevado de Toluca. Ziel war es, die prägnanten Höhenunterschiede zwischen der Geländebasis auf rund 1.865 Metern und den hochgelegenen Gipfelregionen bei 4.665 Metern plastisch herauszuarbeiten.

### Methodische Umsetzung:

Das digitale Höhenraster wurde mit einem durchgehenden Hypsometrie-Farbverlauf symbolisiert, der von satten Grüntönen in den Niederungen bis zu hellen Ockertönen in den Hochlagen reicht. Durch die Überlagerung mit einer eigenständig berechneten Standard-Schummerung treten Hangneigungen, Felsgratstrukturen und die tiefen Kraterränder der Vulkanlandschaft anschaulich hervor.

## EP02 | Geländedarstellung II

### Relief Tschechien

<img src="ReliefTschechien_SM.png" width="800" alt="Reliefkarte Tschechien SM" />

### Plastische Reliefvisualisierung der tschechischen Topografie

Die Karte zeigt eine freigestellte Reliefdarstellung der Republik Tschechien im Imhof-Stil. Im Fokus steht die deutliche Ausprägung der geografischen Kesselstruktur – umrahmt von den Mittelgebirgszügen wie dem Böhmerwald, dem Erzgebirge und den Sudeten im Gegensatz zum flacheren Binnenland.

### Methodische Umsetzung:

Auf Basis von Höhendaten und Ländergrenzen aus dem ESRI Living Atlas wurde das Projekt in ArcGIS Pro in einer flächentreuen Lambert-Projektion angelegt. Über Spatial-Analyst-Tools wurden die Neigung und mehrstufige Schummerungen berechnet. Durch die feine Kombination aus DEM-Hypsometrie im Mist-Farbband, transparentem Neigungs-Layer und multispektraler Schummerung sowie einer dunklen Hintergrundmaskierung entsteht ein starker Dreidimensionalitätseffekt im finalen Layout.

## EP05 | Illuminated Choropleth Maps (Illuminierte 2D-Flächenkarte)

### Plastische 2.5D-Visualisierung sozialer Indikatoren

<img width="1171" height="922" alt="image" src="https://github.com/user-attachments/assets/dc18919d-ad49-4b6b-8c49-2ac80682e350" />
### Beleuchtete Flächenkarte zur Arbeitslosigkeit in Berlin (MSS 2025)
Diese Arbeit zeigt eine illuminierte Choroplethenkarte (Illuminated Choropleth Map) der Berliner Planungsräume auf Basis des Datensatzes Berlin LOR MSS 2025. Dargestellt ist der Status-Indikator S1 (Arbeitslosenquote in Prozent), der die räumliche Verteilung der Erwerbslosigkeit im Stadtgebiet abbildet: Während helle Cremetöne Gebiete mit sehr geringer Arbeitslosigkeit (ab 0,6 %) markieren, heben kräftige Orangetöne bis hin zu dunklem Rot Brennpunkte mit Werten von bis zu 16,9 % hervor.  

### Methodische Umsetzung: 

Auf Basis der administrativen LOR-Polygondaten wurde das Attribut S1 in fünf Klassen unterteilt und mit einem abgestuften Farbverlauf symbolisiert. Aus den klassifizierten Werten wurde ein Höhenraster abgeleitet, über eine prozentuale Streckung kontrastiert und in eine Schummerung (Hillshade) überführt. Durch die Überlagerung dieser Schummerung im Multiplizieren-Modus (Multiply) mit angepasster Transparenz verschmelzen Topographie-Effekt und thematische Färbung zu einer plastischen 2.5D-Anmutung.

## EP06 | Spike Maps

### Dreidimensionale Nadelkarte zur Arbeitslosigkeit in Berlin (MSS 2025)

<img width="1171" height="922" alt="image" src="https://github.com/user-attachments/assets/7ccf71e0-8d07-4c38-b27c-a0d5fbf43812" />
### Räumliche Verteilung und Intensität sozioökonomischer Kennzahlen
Diese Karte visualisiert die räumliche Verteilung und Intensität des Status-Indikators S1 (Arbeitslosenquote in Prozent) im Berliner Stadtgebiet mithilfe einer Spike Map. Anstelle reiner Flächeneinfärbungen werden die Werte der einzelnen Planungsräume durch vertikale, spitz zulaufende Nadeln dargestellt: Flache, gelbe Spitzen stehen für niedrige Quoten (ab 0,6 %), während hohe, rötlich leuchtende Spikes lokale Konzentrationen und Spitzenwerte (bis 16,9 %) im Stadtbild unmittelbar sichtbar machen.

### Methodische Umsetzung:

Die zugrunde liegenden Polygonflächen der Berliner Planungsräume wurden zunächst in repräsentative Mittelpunkte (Feature to Point) überführt. Für die Symbolisierung wurde in ArcGIS Pro ein benutzerdefinierter Style (SpikeMaps.stylx / Gradient Spike) geladen und über einen regulären Polygon-Effekt (3 Kanten, 3 Pkt Radius) zu dreikantigen Pyramiden konfiguriert. Mithilfe angepasster Arcade-Skripte für die vertikale Skalierung und den Y-Versatz wurde die Höhe der Spikes exakt an den Datenbereich von S1 (0,593 bis 16,871) gekoppelt, während ein dunkler Kartenhintergrund den Kontrast der Farbverläufe maximiert.
