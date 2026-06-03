# RecuperaExcel

Strumento gratuito che **recupera i file Excel che non si aprono**.

Molti gestionali esportano file Excel in formati vecchi o con l'estensione sbagliata
(per esempio un vecchio `.xls` salvato con estensione `.xlsx`), e Excel si rifiuta di aprirli
mostrando errori come *"formato ed estensione non corrispondono"* o *"il formato del file non è valido"*.
RecuperaExcel riconosce il formato reale del file e lo riconverte in un `.xlsx` pulito,
apribile da qualsiasi versione di Excel.

## 👉 Apri lo strumento

- **https://alessandropezzali.it/RecuperaExcel.html**
- oppure: **https://pezzaliapp.github.io/RecuperaExcel/**

## Come si usa

1. Trascina nel riquadro il file che Excel non riesce ad aprire (puoi caricarne più di uno).
2. Lo strumento ti dice **che formato era davvero** e lo riconverte.
3. Premi **Scarica** e apri il nuovo file `.xlsx`: si aprirà senza errori.

## Formati riconosciuti

- Excel 97-2003 (`.xls` binario, anche se rinominato in `.xlsx`)
- SYLK (il formato che genera l'errore "file non valido")
- Tabelle HTML o XML salvate con estensione Excel
- XML SpreadsheetML 2003
- CSV / testo delimitato
- DIF, dBASE (`.dbf`)

## Privacy

Tutta la conversione avviene **nel browser dell'utente**: i file **non vengono mai caricati**
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

MIT — vedi sotto. La libreria SheetJS è distribuita con licenza Apache-2.0.
