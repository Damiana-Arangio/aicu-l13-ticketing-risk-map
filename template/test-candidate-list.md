# Test candidate note - L13

Non compilare una suite. Scegli il primo test utile.

| Priorita' | Comportamento | Rischio | Livello | Controllo |
| --- | --- | --- | --- | --- |
| 1 | alta + telefono -> intervento rapido | Il caso speciale telefono viene trattato come chat o email | unit | Il calcolo restituisce `intervento rapido` |

## Primo test da scrivere in L14

```txt
Comportamento: alta + telefono -> intervento rapido
Rischio: il caso speciale telefono viene trattato come chat o email
Livello: unit
Controllo: il calcolo restituisce "intervento rapido"
Comando candidato: pnpm test:unit
```

## Test da non scrivere ora

```txt
Non scrivo: test browser per verificare che urgencyLabel sia visibile nella lista ticket
Perche': prima conviene proteggere la regola di mapping con un test più piccolo e diretto. Il browser aggiungerebbe form, rete e rendering, ma il rischio principale ora è che il calcolo di urgencyLabel sia sbagliato.
```
