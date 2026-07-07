# Consegna studenti - Lezione 13

## Obiettivo

Capire quale comportamento vale la pena proteggere prima di scrivere test.

## Comportamento di partenza

```txt
priority + sourceChannel -> urgencyLabel
```

Mapping:

| Priority | Source channel | Urgency label |
| --- | --- | --- |
| alta | telefono | intervento rapido |
| alta | chat | prioritario |
| alta | email | prioritario |
| normale | telefono | da gestire |
| normale | chat | da gestire |
| normale | email | standard |
| bassa | telefono | monitorare |
| bassa | chat | monitorare |
| bassa | email | monitorare |

## Attivita'

Scrivi una nota minima:

```txt
Comportamento:
Rischio:
Controllo:
Comando candidato:
```

## Esempio

```txt
Comportamento: alta + telefono -> intervento rapido
Rischio: la regola viene cambiata o duplicata nel client
Controllo: la response contiene urgencyLabel=intervento rapido
Comando candidato: pnpm test:unit
```

## Prompt AI facoltativo

```txt
Dato questo comportamento:
priority + sourceChannel -> urgencyLabel

Proponi 5 rischi testabili.
Per ciascuno indica:
- livello di test piu' piccolo utile;
- controllo falsificabile;
- comando candidato;
- motivo per cui non partiresti da un test browser.

Non proporre una suite completa.
```

## Pronto quando

Sei pronto per L14 quando puoi dire:

```txt
Questo test sarebbe utile perche' protegge questo rischio.
Questo controllo fallirebbe se il comportamento si rompe.
```
