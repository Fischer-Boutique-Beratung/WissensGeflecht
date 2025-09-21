# **WissensGeflecht: AI-Powered Knowledge System & Markdown Editor**

**Ein intelligentes System zur Erstellung, Verwaltung und Visualisierung von vernetzten Wissensdatenbanken auf Markdown-Basis.**

WissensGeflecht ist nicht nur ein Blog-Generator, sondern ein komplettes Werkzeugset, das den gesamten Prozess von der ersten Idee bis zur finalen Publikation abdeckt. Es kombiniert die kreative Kraft einer modernen KI mit einem leistungsstarken grafischen Editor und einem dynamischen Webserver, um aus losen Gedanken strukturierte und intelligent vernetzte Wissens-Webseiten zu erstellen.

## **Hauptfunktionen**

* **KI-gestützte Inhaltsgenerierung:** Erstellen Sie auf Knopfdruck ganze Themenwelten. Das System generiert nicht nur Texte, sondern liefert sie in einer vordefinierten, logischen JSON-Struktur (Einleitung, Hauptteil, Fazit etc.).  
* **Vollständiger GUI-Editor:** Bearbeiten Sie Ihre Inhalte in einer komfortablen grafischen Oberfläche. Fügen Sie Überschriften, Listen, Bilder und Zitate über ein intuitives Menüsystem ein, ohne sich um die Markdown-Syntax kümmern zu müssen.  
* **Änderungsverfolgung (Versioning):** Jede an einer Datei gespeicherte Änderung wird versioniert. Sie können jederzeit auf frühere Versionen zurückgreifen und den Verlauf Ihrer Arbeit nachvollziehen.  
* **Visualisierung von Abhängigkeiten:** Analysieren Sie die Link-Struktur Ihres Blogs mit einem interaktiven Graphen. Erkennen Sie Zusammenhänge, finden Sie isolierte Seiten und navigieren Sie durch Ihr Wissen per Mausklick.  
* **Pfadanalyse:** Finden und visualisieren Sie alle möglichen Verbindungen zwischen zwei beliebigen Artikeln in Ihrem Blog.  
* **Dynamischer Webserver:** Starten Sie mit einem einzigen Befehl einen lokalen Webserver, der Ihren Blog als professionelle Webseite darstellt und alle Markdown-Features, inklusive BibTeX-Quellenverzeichnis, live rendert.  
* **PDF-Export:** Exportieren Sie jeden Artikel mit einem Klick in eine hochwertig formatierte PDF-Datei, die das Design Ihres Blogs beibehält.  
* **BibTeX-Quellenverwaltung:** Verwalten Sie Ihre wissenschaftlichen Quellen in einer zentralen .bib-Datei und fügen Sie Zitate bequem über einen Dialog in Ihre Texte ein.  
* **Flexible Konfiguration:** Jeder Blog ist vollständig modular. Passen Sie das Aussehen (CSS), das Grundgerüst (HTML-Template) und die Dateinamen für Ihre Quellen über eine einfache config.json-Datei pro Projekt an.

## **Die drei Kernkomponenten**

1. **Der KI-Generator (stichworte\_fixed.py):** Das Fundament. Dieses Skript nimmt ein Thema entgegen und beauftragt die Google Gemini API, eine strukturierte Wissensbasis mit allen notwendigen Dateien (.md, config.json, style.css etc.) zu erstellen.  
2. **Der Editor (edit\_blog\_gui.py):** Das Herzstück. Eine vollständige Desktop-Anwendung zur Erstellung, Bearbeitung und Analyse Ihrer Inhalte.  
3. **Der Webserver (start\_webserver.py):** Das Schaufenster. Ein leichtgewichtiger Python-Server, der Ihren Blog für die Vorschau im Browser live rendert.

## **Technologie-Stack**

* **Backend & GUI:** Python 3  
* **Grafische Oberfläche:** Tkinter  
* **KI-Anbindung:** Google Gemini API (google-generativeai)  
* **Webserver:** Python Standard Library (http.server) & Flask (für erweiterte Versionen)  
* **Markdown-Verarbeitung:** markdown  
* **PDF-Export:** xhtml2pdf

## **Installation & Setup**

1. **Repository klonen:**  
   git clone https://github.com/ihr-name/wissensgeflecht.git  
   cd wissensgeflecht

2. **Virtuelle Umgebung erstellen (empfohlen):**  
   python \-m venv venv  
   \# Windows  
   .\\venv\\Scripts\\activate  
   \# macOS / Linux  
   source venv/bin/activate

3. Abhängigkeiten installieren:  
   Alle notwendigen Pakete sind in der requirements.txt definiert.  
   pip install \-r requirements.txt

4. API-Schlüssel konfigurieren:  
   Sie benötigen einen API-Schlüssel für die Google Gemini API. Tragen Sie diesen entweder direkt in die stichworte\_fixed.py-Datei ein oder (sicherer) legen Sie ihn als Umgebungsvariable GOOGLE\_API\_KEY an.

## **Typischer Arbeitsablauf**

1. **Inhalte generieren:**  
   python stichworte\_fixed.py

   Folgen Sie den Anweisungen, um einen neuen Blog zu einem Thema Ihrer Wahl zu erstellen.  
2. **Bearbeiten & Verfeinern:**  
   python edit\_blog\_gui.py

   Nutzen Sie die grafische Oberfläche, um die generierten Texte zu bearbeiten, neue Seiten zu erstellen, das Design anzupassen oder die Link-Struktur zu analysieren.  
3. **Vorschau & Publizieren:**  
   python start\_webserver.py \[name-ihres-blog-ordners\]

   Starten Sie den Server und betrachten Sie Ihren Blog live im Browser unter http://127.0.0.1:8000.

## **Mitwirken**

Fehlerreports, Feature-Wünsche und Pull Requests sind herzlich willkommen\!

## **Lizenz**

siehe: [Lizenz-Model](LICENSE.md)
