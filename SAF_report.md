# SAF

**Generated** : 2026-06-22T00:06:10.119520+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €329.40  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 19.8 < 20 (tendance pas encore confirmée) alors que Choppiness 35.4 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 73.5 > 70 (surachat) ; %B 0.97 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €304.15–€311.66 (mid €307.91)
- Spot actuel : €329.40 (+7.0% au-dessus de la zone — repli à attendre)
- Stop : €289.14 (stop atr-based (-4.27%))
- Targets : T1 €315.91 · R/R 0.43 | T2 €323.92 · R/R 0.85 | T3 €331.92 · R/R 1.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €289.14


## Edge, scénarios & sizing

- EV/risk : -0.096 | EV/share : €-1.804 | p_fill : —
- Régime probabiliste (posterior HMM, swing) : bull 36.6 | bear 40.1 | side 23.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 329.0 (= 1 part(s) × prix) · cible 640.0


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.74 · part idiosyncratique 11.57
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Indicateurs (résumé)

- **RSI** : 73.5  _(surachat)_
- **ADX** : 19.8  _(pas de tendance nette)_
- **MACD** : hist 3.484  _(pas de croisement recent)_
- **BB** : %B 0.97 · largeur 17.1%
- **ATR** : 9.39 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.156  _(distribution)_
- **Vol ratio** : 1.78  _(volume au-dessus de la moyenne)_
- **Choppiness** : 35.4  _(marche directionnel)_
- **MA** : MA20 304.94 · MA50 291.45 · MA200 298.22  _(prix > MA20)_
- **Dist MA** : MA20 +8.0% · MA50 +13.0% · MA200 +10.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (20362 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
