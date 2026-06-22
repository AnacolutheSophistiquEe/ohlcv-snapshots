# 000660

**Generated** : 2026-06-22T21:44:14.469667+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 10/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · ₩2919000.00  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : %B 1.09 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2578058.50–₩2696741.50 (mid ₩2637400.00)
- Spot actuel : ₩2919000.00 (+10.7% au-dessus de la zone — repli à attendre)
- Stop : ₩2320912.00 (stop atr-based (-10.09%))
- Targets : T1 ₩2829775.77 · R/R 0.61 | T2 ₩3022151.53 · R/R 1.22 | T3 ₩3214527.30 · R/R 1.82
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2320912.00


## Edge, scénarios & sizing

- EV/risk : -0.006 | EV/share : ₩-1798.942 | p_fill : —
- Régime probabiliste (posterior HMM, swing) : bull 19.8 | bear 31.8 | side 48.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 640.0


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.28 · part idiosyncratique 0.32
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Indicateurs (résumé)

- **RSI** : 65.5  _(momentum haussier)_
- **ADX** : 37.5  _(tendance etablie)_
- **MACD** : hist 46568.592  _(bullish_recent)_
- **BB** : %B 1.09 · largeur 46.3%
- **ATR** : 196428.57 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.107  _(accumulation)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 35.1  _(marche directionnel)_
- **MA** : MA20 2296597.87 · MA50 1778275.41 · MA200 923462.85  _(prix > MA20)_
- **Dist MA** : MA20 +27.1% · MA50 +64.1% · MA200 +216.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16043 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
