# 🏫 Scuole Primarie - Analizzatore Distanze e Raggiungibilità

> **Sistema di analisi per la raggiungibilità delle scuole primarie di Padova e provincia entro l'orario di entrata alle 7:50**

[![GitHub release](https://img.shields.io/github/release/yourusername/scuoleprimarie.svg)](https://github.com/yourusername/scuoleprimarie/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)

## 🎯 **Scopo del Progetto**

Questo sistema analizza **automaticamente** quali scuole primarie della provincia di Padova sono raggiungibili entro le **7:50 del mattino**, considerando:

- 📍 **Partenza fissa**: via Giovanni d'Alemagna 12, 35134 Padova
- ⏰ **Vincolo sveglia**: Non prima delle **6:15** del mattino
- 🚗 **Trasporto auto**: Tempi stimati con traffico ora di punta
- 🚌 **Mezzi pubblici**: Orari realistici + tempo cammino alle fermate
- 📊 **Coordinate GPS precise**: Tramite OpenStreetMap Nominatim API

## ✨ **Funzionalità Principali**

### 🔍 **Analisi Automatica**
- Caricamento file Excel con elenco scuole
- Geocoding automatico tramite API OpenStreetMap
- Calcolo distanze precise con formula di Haversine
- Stima tempi di percorrenza auto e mezzi pubblici

### 🚨 **Vincoli Critici**
- **Orario arrivo**: Entro le 7:50 (con 10 min di margine)
- **Orario sveglia**: Non prima delle 6:15 del mattino
- **Tempo preparazione**: 30 min mezzi pubblici, 15 min auto
- **Distanza massima ragionevole**: 2 ore di viaggio

### 📊 **Output Dettagliato**
- Elenco scuole ordinate per raggiungibilità
- Orari di partenza specifici per auto e mezzi pubblici
- Analisi dettagliata tempi e distanze
- Alert per situazioni critiche o problematiche

## 🚀 **Demo Live**

[**👉 Prova il sistema qui**](https://sterius74.github.io/scuoleprimarie)

## 📋 **Requisiti**

### Dati di Input
- File Excel (.xlsx/.xls) con struttura:
- - Codici MIUR che iniziano con "PDEE" (scuole primarie Padova)

### Tecnologie
- React 18+
- Lucide React (icone)
- SheetJS/xlsx (lettura Excel)
- OpenStreetMap Nominatim API (geocoding)

## 🛠️ **Installazione**

### Opzione 1: Uso diretto
1. Apri `index.html` in un browser moderno
2. Carica il file Excel delle scuole
3. Avvia l'analisi

### Opzione 2: Sviluppo locale
```bash
# Clona il repository
git clone https://github.com/sterius74/scuoleprimarie.git
cd scuoleprimarie

# Installa dipendenze
npm install

# Avvia server di sviluppo
npm start
