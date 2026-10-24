# omg-to-typst Plugin

obsidian://show-plugin?id=omd-to-typst
https://github.com/tisgoud/Obsidian-Omd2Typst

- Installiert in Obsidian erstmal ohne Typst zu installieren
- Exportiert ein .typ Dokument, kein PDF
- Typst installieren auf Mac mit homebrew

```
brew install typst
```

![[Bildschirmfoto 2026-10-24 um 01.21.17.png]]

- Erster export sieht schon mal gar nicht schlecht aus, Deckblatt, Inhaltsverzeichnis, Notiz
- Aus Github Templates und Examples runtergeladen

![[Bildschirmfoto 2026-10-24 um 01.27.16.png]]
- Man muss templates in den Plugin Einstellungen extra hinzufügen
- Erster Test mit Beispieltemplates schon mal absolut überragend, man kann bei Klick auf die 3 Punkte sagen, mit welchem Template das exportieren soll, man sieht in Obsidian grob die Stuktur ohne zu viele LaTeX ähnliche Strukturen

![[Bildschirmfoto 2026-10-24 um 01.34.44.png]]
![[Bildschirmfoto 2026-10-24 um 01.35.45.png]]
![[Bildschirmfoto 2026-10-24 um 01.36.19.png]]

# TypstPDFExport

- hier kann man Einstellungen zu Seitenrändern und Schriftarten machen
- braucht aber pandoc, muss man installieren

```
brew install pandoc
```

- gibt jetzt export TO pdf und export AS Pdf, das eine ist vom omd2typst plugin, das andere typstPDFexport
- export failed mehrfach, vielleicht liegts an dem Dokument hier?
- in den settings default.typ als standard template ausgewählt, export failed immernoch 
- man braucht noch das hier laut github Doku, optional aber vielleicht ist das der Grund?

```
brew install imagemagick
```

- Laut Doku gibts nicht nur das default.typ template sondern noch mehr, modern.typ z.b., allerdings sind die nirgends in meinem vault
- geht immer noch nicht
![[Bildschirmfoto 2026-10-24 um 02.24.41.png]]
- Also das Template ist da nicht gespeichert, nervt direkt, dann halt nicht
- Pandoc deinstalliert mit brew und Plugin entfernt

# Tinymist
- Plugin um Typst Dateien in Obsidian selbst zu bearbeiten und zu ändern, könnte zum omd2typst Plugin passen, weil dort kann man templates zwar verwenden, aber nicht direkt sehen wie sie aussehen
- in Obsidian installieren und dann über brew auch 

```
brew install tinymist
```

- Tinymist und das andere Plugin gemeinsam funktioniert schon mal nicht
- die .typ dateien werden auch nicht mehr angezeigt, wenn man das erste Plugin deaktiviert, also erstmal nicht direkt testbar
- laut Doku kann nur ein Plugin .typ anzeigen, also musste das alte wieder deinstalliert werden (disable allein hat nicht gereicht), jetzt werden .typ dateien wieder angezeigt vom neuen plugin

![[Bildschirmfoto 2026-10-24 um 03.07.47.png]]
- Das Plugin macht schon mal ne kleine Entwicklungsumgebung aus Obsidian, aber es rendert das typ file nicht. Kann auch sein dass es dran liegt dass das Beispiele fürs andere plugin waren
- https://typst.app/universe hier templates runterladen
- Es gab eins von der OTH direkt, das hab ich runtergeladen und in obsidian gezogen
- die doku vom PLugin meint zwar, dass man jedes .typ öffnen kann und direkt live bearbeiten kann, aber nein, hier funktioniert nur main, alles andere nicht
- die Schreibweise ist auch nicht so intuitiv Markdown wie im vorherigen Plugin, also nicht allzu zufriedenstellend

![[Bildschirmfoto 2026-10-24 um 03.20.30.png]]
![[Bildschirmfoto 2026-10-24 um 03.22.52.png]]

- aber es baut das Dokument schon mal cool zusammen aus verschiedenen Inhalten, Quellen funktionieren, glossar geht, lediglich die Formatierung ist gewöhnungsbedürftig 
