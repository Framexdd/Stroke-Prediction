# ---

**Stroke Prediction Project **


## **📋 Descrizione**

Questo progetto di Machine Learning ha l'obiettivo di analizzare e modellare dati clinici per prevedere la probabilità che un paziente subisca un ictus (stroke). Attraverso l'analisi di fattori demografici e sanitari, è stato sviluppato un sistema predittivo in grado di identificare i soggetti a rischio.  
Il progetto copre l'intero ciclo di vita del Machine Learning: dall'analisi esplorativa dei dati (EDA) al pre-processing, passando per il bilanciamento delle classi fino all'addestramento e valutazione di diversi algoritmi.

## **🗂️ Dataset**

Il dataset utilizzato contiene informazioni su oltre 5.000 pazienti.  
Fonte: Kaggle \- Stroke Prediction Dataset

### **Variabili principali:**

* **Variabili Numeriche:**  
  * age: Età del paziente.  
  * avg\_glucose\_level: Livello medio di glucosio nel sangue.  
  * bmi: Indice di massa corporea (i valori mancanti sono stati imputati con la mediana).  
* **Variabili Categoriche:**  
  * gender, ever\_married, work\_type, Residence\_type, smoking\_status.  
  * hypertension, heart\_disease (indicatori binari di patologie pregresse).  
* **Target:**  
  * stroke: 1 se il paziente ha avuto un ictus, 0 altrimenti.

**Nota:** La colonna id è stata rimossa in quanto non rilevante ai fini predittivi.

## **🛠️ Tecnologie e Librerie**

Il progetto è sviluppato in **Python** utilizzando le seguenti librerie principali:

* **Data Manipulation:** pandas, numpy  
* **Visualization:** matplotlib, seaborn  
* **Machine Learning:** scikit-learn, xgboost  
* **Imbalanced Learning:** imbalanced-learn (per SMOTE)

Per installare le dipendenze necessarie:

Bash

pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn

## **⚙️ Metodologia**

Il flusso di lavoro ha seguito questi step:

1. **Data Analysis (EDA):** Analisi delle distribuzioni delle variabili e identificazione dei valori mancanti (BMI).  
2. **Data Preparation:**  
   * Imputazione dei valori nulli di BMI con la mediana.  
   * Rimozione feature inutili (id).  
3. **Feature Engineering:** Applicazione del **One-Hot Encoding** per le variabili categoriche.  
4. **Dataset Balancing:** Utilizzo della tecnica **SMOTE** (Synthetic Minority Over-sampling Technique) per gestire il forte sbilanciamento della classe target (pazienti con ictus).  
5. **Modeling:** Addestramento e confronto di diversi algoritmi:  
   * Decision Tree  
   * Random Forest  
   * Logistic Regression  
   * K-Nearest Neighbors (KNN)  
   * XGBoost Classifier

## **📊 Risultati**

I modelli sono stati valutati utilizzando metriche come Accuracy, Precision, Recall e F1-Score. Il modello **XGBoost** ha mostrato le performance migliori e più robuste dopo la validazione.

| Modello | Accuracy (Test) | F1-Score |
| :---- | :---- | :---- |
| **XGBoost** | **\~95.3%** | **0.953** |
| Random Forest | \~92.0% | 0.920 |
| Decision Tree | \~89.2% | 0.906 |
| Logistic Regression | \~84.6% | 0.881 |

## **🚀 Miglioramenti Futuri**

* **Hyperparameter Tuning:** Ottimizzazione avanzata dei parametri (es. GridSearchCV) per migliorare ulteriormente le performance.  
* **Analisi delle correlazioni:** Approfondire le dipendenze tra variabili per ridurre eventuali ridondanze.

---

*Progetto realizzato a scopo educativo e di analisi.*  
---

Per una spiegazione video che potrebbe essere utile per arricchire la presentazione del tuo progetto o per approfondire XGBoost, puoi consultare:  
XGBoost in Python from Start to Finish  
Questo video è rilevante perché XGBoost è il modello risultato più performante nel tuo progetto e il tutorial mostra come implementarlo e ottimizzarlo passo dopo passo.
