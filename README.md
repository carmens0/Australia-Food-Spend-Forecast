# Australia-Food-Spend-Forecast
![Marble Bar in Sydney](./image.png)

## 📌 Descrizione del Progetto
Questo progetto analizza l'andamento delle spese per cene e pranzi fuori in Australia, basandosi su una serie storica mensile (\`auscafe\`) contenuta nel pacchetto **fpp2** in R. L'obiettivo è individuare trend, stagionalità e fattori che influenzano queste spese, attraverso tecniche di analisi descrittiva, decomposizione e modelli previsionali.

## 📊 Dataset
Il dataset utilizzato contiene:
- **408 osservazioni**
- **Periodo di riferimento:** Aprile 1982 - Settembre 2017
- **Unità di misura:** Bilioni di dollari australiani

Le analisi si concentrano sugli anni **1983-2016**, escludendo dati incompleti di 1982 e 2017.

## 🔍 Metodologia
L'analisi si sviluppa attraverso diverse fasi:
### 1️⃣ **Pulizia e verifica dati**
- Assenza di valori mancanti verificata con \`statsNA()\`
- Analisi grafica per identificare valori anomali

### 2️⃣ **Analisi descrittiva**
- Identificazione delle componenti principali: **trend, stagionalità, ciclicità**
- Utilizzo di **autoplot(), ggseasonplot()** per visualizzare variazioni stagionali

### 3️⃣ **Modelli di previsione**
Sono stati confrontati quattro modelli benchmark:
- **Average Method**
- **Naive Method**
- **Seasonal Naive Method**
- **Drift Method**

**Metriche di valutazione**: RMSE, MAE, MAPE, SMAPE

### 4️⃣ **Decomposizione delle serie storiche**
Sono state applicate diverse tecniche di decomposizione:
- **Modello moltiplicativo classico**
- **X11 Decomposition**
- **X13 SEATS Decomposition**
- **STL Decomposition**

### 5️⃣ **Modelli di regressione**
Sono stati costruiti diversi modelli per analizzare il legame tra le spese per cene e pranzi fuori e variabili esterne (produzione di gas, vendite di vino, partenze di residenti e turisti, tasso di disoccupazione). I modelli sono stati selezionati sulla base di criteri di performance (AIC, BIC, Adjusted R²).

## 📉 Risultati Principali
- **Trend crescente**: le spese per cene e pranzi fuori sono aumentate nel tempo.
- **Stagionalità evidente**: decrementi a febbraio e giugno, incrementi a luglio e dicembre.
- **Miglior modello previsionale**: il metodo **Seasonal Naive** offre le previsioni più accurate.
- **Modelli di regressione**: identificati fattori economici che influenzano le spese, tra cui il numero di turisti e il tasso di occupazione.

## 🛠️ Tecnologie e Strumenti
- **Linguaggi**: R
- **Librerie principali**: fpp2, ggplot2, forecast, dplyr
- **Software**: RStudio

## 📂 Struttura del Progetto
```
├── australian_food_forecast.html    # Codice in HTML per l'analisi
├── australian_food_forecast.pdf     # Report finale in pdf
├── README.md                  # Documentazione del progetto
```

## 🚀 Avvio del Progetto
1. Clonare la repository:
   ```sh
   git clone https://github.com/carmens0/Australia-Food-Spend-Forecast.git
   ```
2. Aprire lo script in **RStudio** e installare le dipendenze necessarie:
   ```r
   install.packages(c("fpp2", "ggplot2", "forecast", "dplyr"))
   ```
3. Eseguire il codice per generare le analisi:
   ```r
   source("australian_food_forecast.html")
   ```

## 📝 Autore

| Name                | Description                                                                                       |
|---------------------|---------------------------------------------------------------------------------------------------|
| **Carmela Pia Senatore** | Developer - [carmens0](https://github.com/carmens0) <br> Email - [carmensenatore58@gmail.com](mailto:carmensenatore58@gmail.com) <br> LinkedIn - [Carmela Pia Senatore](https://linkedin.com/in/carmela-pia-senatore-ba1797207) |

---
🔍 Per maggiori dettagli, contattare l'autore.
