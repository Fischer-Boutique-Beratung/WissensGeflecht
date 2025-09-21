# **Anleitung: Google API-Schlüssel für den KI-Generator**

Dieses Dokument erklärt, wie Sie einen kostenlosen API-Schlüssel von Google erhalten und wo Sie ihn eintragen müssen, um die KI-gestützte Inhaltsgenerierung zu nutzen.

### **Wofür wird der Schlüssel benötigt?**

Der API-Schlüssel ist Ihre persönliche Zugangsberechtigung zur **Google Gemini API**, einem leistungsstarken KI-Modell von Google.

* **Ausschließlich für den Generator:** Nur das Skript stichworte\_fixed.py benötigt diesen Schlüssel, um Inhalte (Texte, Stichwörter etc.) zu erstellen.  
* **Keine Notwendigkeit für Editor & Webserver:** Der grafische Editor (edit\_blog\_gui.py) und der Webserver (start\_webserver.py) funktionieren vollständig **ohne** diesen API-Schlüssel. Sie können also neue Blogs anlegen sowie bestehende Blogs bearbeiten und ansehen, ohne eine Verbindung zu Google herstellen zu müssen.

### **Schritt-für-Schritt-Anleitung zum API-Schlüssel**

Das Erstellen eines Schlüssels ist kostenlos und dauert nur wenige Minuten.

1. Google AI Studio besuchen:  
   Öffnen Sie die Webseite des [Google AI Studio](https://aistudio.google.com/apikey) in Ihrem Webbrowser. Sie werden aufgefordert, sich mit Ihrem Google-Konto anzumelden.  
2. **API-Schlüssel erstellen:**  
   * Klicken Sie nach der Anmeldung auf der linken Seite auf den Menüpunkt **"Get API key"**.  
   * Auf der folgenden Seite klicken Sie auf den Button **"Create API key in new project"**.  
3. **Schlüssel kopieren:**  
   * Es wird sofort ein neuer API-Schlüssel für Sie generiert und in einem Pop-up-Fenster angezeigt. Dies ist eine lange Zeichenkette, die mit AIza... beginnt.  
   * **Kopieren Sie diesen Schlüssel** in Ihre Zwischenablage. Behandeln Sie ihn wie ein Passwort und geben Sie ihn nicht öffentlich weiter.  
4. **Schlüssel im Skript eintragen:**  
   * Öffnen Sie die Datei stichworte\_fixed.py in einem Texteditor.  
   * Suchen Sie die folgende Zeile (ungefähr bei Zeile 40):  
     genai.configure(api\_key="YOUR\_API\_KEY")

   * Ersetzen Sie den Platzhalter YOUR\_API\_KEY durch den Schlüssel, den Sie eben kopiert haben.  
     \# Beispiel:  
     genai.configure(api\_key="XYZ-aSyBvJiuzMyzbn6fH-SxnPhAe8tLEu7m12345")  
