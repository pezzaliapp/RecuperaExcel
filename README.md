# RecuperaExcel

Strumento gratuito per **recuperare, analizzare e convertire** file Excel e CSV.

Molti gestionali esportano file in formati vecchi o con l'estensione sbagliata
(per esempio un vecchio `.xls` salvato come `.xlsx`), e Excel si rifiuta di aprirli
mostrando errori come *"formato ed estensione non corrispondono"* o *"il formato del file non è valido"*.
RecuperaExcel riconosce il formato reale, lo ripara, ne analizza il contenuto e lo converte
da/verso CSV — tutto **nel browser**, senza inviare nulla online.

## 👉 Apri lo strumento

- **https://alessandropezzali.it/RecuperaExcel.html**
- oppure: **https://pezzaliapp.github.io/RecuperaExcel/**

## Funzioni

Lo strumento è organizzato in tre schede.

### 01 · Recupera
Trascina un file che Excel non riesce ad aprire: viene riconosciuto il formato reale
e restituito come `.xlsx` pulito, apribile da qualsiasi versione di Excel.

### 02 · Analizza
Trascina un file per scoprirne i dettagli, senza modificarlo:
- chi lo ha **creato** e chi lo ha **modificato per ultimo**;
- con quale **programma e versione** è stato generato (utile per identificare il gestionale);
- **date** di creazione e ultima modifica;
- **numero di fogli** ed elenco per nome, con stato **visibile / nascosto / molto nascosto**;
- per ogni foglio: righe × colonne, intestazioni con il **tipo di dato** rilevato per colonna,
  conteggio di **formule** (con esempi), celle unite, collegamenti e note.

### 03 · CSV ⇄ Excel
Conversione bidirezionale con **direzione automatica**: carica un Excel e ottieni il CSV,
carica un CSV e ottieni l'`.xlsx`. Il separatore in entrata viene rilevato da solo;
in uscita puoi scegliere separatore (predefinito `;`, stile Excel italiano) e BOM UTF-8.
Se l'Excel ha più fogli, viene generato un CSV per ciascuno.

## Formati riconosciuti

- Excel 97-2003 (`.xls` binario, anche se rinominato in `.xlsx`)
- Excel moderno (`.xlsx`, `.xlsm`, `.xlsb`)
- SYLK (il formato che genera l'errore "file non valido")
- Tabelle HTML o XML salvate con estensione Excel
- XML SpreadsheetML 2003
- CSV / testo delimitato (separatore rilevato automaticamente)
- DIF, dBASE (`.dbf`)

## Privacy

Tutta l'elaborazione avviene **nel browser dell'utente**: i file **non vengono mai caricati**
su nessun server. Lo strumento funziona anche offline una volta aperta la pagina.

## Come è fatto

Un unico file HTML autonomo, senza dipendenze esterne: la libreria di lettura
([SheetJS](https://sheetjs.com), licenza Apache-2.0) è incorporata direttamente nel file.
Nessuna installazione, nessun server, nessun account.

## Pubblicazione (GitHub Pages)

1. **Settings → Pages**: come *Source* seleziona il branch `main`, cartella `/ (root)`, salva.
2. Lo strumento sarà online su `https://pezzaliapp.github.io/RecuperaExcel/`.
3. (Opzionale) Per usare il dominio personalizzato, sempre in *Pages* imposta
   *Custom domain* = `alessandropezzali.it` e configura i record DNS come da
   [guida GitHub](https://docs.github.com/pages). Un dominio apex può servire un solo sito Pages.

## Licenza

MIT — vedi il file `LICENSE`. La libreria SheetJS è distribuita con licenza Apache-2.0.
