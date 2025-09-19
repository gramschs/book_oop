---
jupytext:
  cell_metadata_filter: -all
  formats: ipynb,md:myst
  main_language: python
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.5
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# Installation

Python wird in der Regel mit dem Betriebsystem ausgeliefert. Für diese Vorlesung
benötigen wir jedoch Python-Erweiterungen, die standardmäßig nicht installiert
werden. Daher benutzen wir in dieser Vorlesung **Anaconda**, eine sehr bekannte
Python-Distribution.

Eine Python-Distribution ist eine Sammlung von Python-Softwarekomponenten. Sie
umfasst den Python-Interpreter selbst, aber auch zusätzliche Bibliotheken und
Frameworks, Entwicklungs- und Debugging-Tools sowie Anwendungen, die für die
Entwicklung mit Python nützlich sein können.

## Warum Anaconda?

Anaconda ist eine Python-Distribution, die von der Firma Anaconda, Inc.
entwickelt wird. Sie ist eine kostenlose Open-Source-Plattform, die es
Python-Entwickler:innen ermöglicht, Python, R und andere Programmiersprachen
sowie zahlreiche Bibliotheken und Tools auf einfache Weise zu installieren, zu
verwalten und zu verwenden.

Die Distribution enthält eine Reihe von nützlichen Paketen und Bibliotheken für
wissenschaftliche Berechnungen, Datenanalyse, maschinelles Lernen und andere
Anwendungen. Sie ist sowohl für Einsteiger als auch für fortgeschrittene
Entwickler geeignet und bietet eine benutzerfreundliche Benutzeroberfläche, um
Python und seine Bibliotheken zu verwalten und zu verwenden.

## Installation Anaconda und Start JupyterLab für Jupyter Notebooks

Hier ist eine Schritt-für-Schritt-Anleitung zum Installieren von Python mit der
Distribution Anaconda für Windows und MacOS:

1. Öffnen Sie die offizielle Anaconda-Website unter
   <https://www.anaconda.com/products/individual> und laden Sie die neueste
   Version von Anaconda für Ihr Betriebssystem herunter.
2. Führen Sie die Installationsdatei aus und folgen Sie den Anweisungen auf dem
   Bildschirm. Wählen Sie ggf. ein freies Installationsverzeichnis und stellen
   Sie sicher, dass die Option "Add Anaconda to my PATH environment variable"
   aktiviert ist.
3. Öffnen Sie nach der Installation das Anaconda-Navigator-Programm, das im
   Startmenü oder Launchpad verfügbar sein sollte.
4. Um ein neues Jupyter Notebook für die Python-Programmierung zu erstellen,
   klicken Sie auf "Home" im Anaconda-Navigator und wählen "JupyterLab"
   aus. Alternativ können Sie JupyterLab auch mit dem Befehl "jupyter-lab" aus einem Terminal oder einer Konsole starten (Linux oder MacOS).
5. Wählen Sie "Python 3 (ipykernel)" aus, um ein neues Notebook zu erstellen.
6. Sie können jetzt Python-Code in dem Notebook schreiben und ausführen. Wenn
   Sie zusätzliche Pakete benötigen, können Sie diese über den
   "Environments"-Tab im Anaconda-Navigator installieren.

```{figure} pics/fig_chap00_sec03_jupyterlab.png
:name: fig_chap00_sec03_jupyterlab

Startansicht der Software JupyterLab: ein neues Jupyter Notebook wird mit Klick auf den Button Python 3 (ipykernel) erstellt.
```

## Was ist JupyterLab und welche Alternativen gibt es?

[JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)
ist eine webbasierte Entwicklungsumgebung, um Jupyter Notebooks zu öffnen, zu
editieren, den Python-Code auszuführen und alles wieder zu speichern. Neben
JupyterLab gibt es weitere Möglichkeiten, um Jupyter Notebooks zu bearbeiten.

Die beiden Entwicklungsumgebungen

* [PyCharm](https://www.jetbrains.com/help/pycharm/jupyter-notebook-support.html)
* [Microsoft Visual Studio
  Code](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)

ermöglichen ebenfalls die direkte Bearbeitung von Jupyter Notebooks. Auch
zahlreiche Cloudanbieter bieten direkt das Bearbeiten und Ausführen von Jupyter
Notebooks an, z.B.

* [Google Colab](https://colab.research.google.com/notebook)
* [Microsoft
  Azure](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Deepnote](https://deepnote.com)
* [replit](https://replit.com/template/jupyter-notebook)

Wie bei allen Clouddiensten sollte man sich jedoch eingehend mit den
Datenschutzbestimmungen des Anbieters vertraut machen, bevor man den Dienst in
Anspruch nimmt. Aufgrund des Datenschutzes empfehle ich stets, Python/Anaconda
lokal zu installieren.
