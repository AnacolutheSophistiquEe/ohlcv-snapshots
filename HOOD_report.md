# HOOD

**Generated** : 2026-06-22T00:20:21.321524+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $108.15  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : %B 1.02 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $100.53–$105.16 (mid $102.85)
- Spot actuel : $108.15 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : $90.51 (stop atr-based (-10.22%))
- Targets : T1 $109.34 · R/R 0.53 | T2 $115.82 · R/R 1.05 | T3 $122.31 · R/R 1.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $90.51


## Edge, scénarios & sizing

- EV/risk : -0.01 | EV/share : $-0.122 | p_fill : —
- Régime probabiliste (posterior HMM, swing) : bull 42.0 | bear 27.1 | side 30.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 541.0 (= 5 part(s) × prix) · cible 640.0


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Indicateurs (résumé)

- **RSI** : 62.9  _(momentum haussier)_
- **ADX** : 25.8  _(tendance etablie)_
- **MACD** : hist 2.17  _(pas de croisement recent)_
- **BB** : %B 1.02 · largeur 43.7%
- **ATR** : 7.37 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.234  _(accumulation)_
- **Vol ratio** : 1.14  _(volume normal)_
- **Choppiness** : 44.6  _(transition)_
- **MA** : MA20 88.02 · MA50 82.8 · MA200 102.79  _(prix > MA20)_
- **Dist MA** : MA20 +22.9% · MA50 +30.6% · MA200 +5.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19194 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
