# SAF

**Generated** : 2026-06-23T00:07:16.445968+00:00  
**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €331.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €331.40 (+7.3% vs entrée) · entrée €308.81 · stop €305.42 · T1 €315.57 · R/R 1.99  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.155 · ¼-Kelly 0.011 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 73.9 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €307.45–€310.16 (mid €308.81)
- Spot actuel : €331.40 (+7.3% au-dessus de la zone — repli à attendre)
- Stop : €305.42 (stop atr-based (-4.14%))
- Targets : T1 €315.57 · R/R 1.99 | T2 €322.34 · R/R 3.99 | T3 €329.11 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €305.42


## Edge, scénarios & sizing

- EV/risk : 0.155 | EV/share : €0.526 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 21 % | T3 9 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 21.0 | bear 36.8 | side 42.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 331.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 132 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.101% → cible +0.98% / stop −1.0%, p_fill 11%, 15 remplis) : P(cible|rempli) **27%** · **EV/risk -0.021** (×p_fill ; si rempli -0.18% du capital)
  - **swing** : indisponible (trop peu de remplissages (4))
  - **deep** : indisponible (trop peu de remplissages (3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→65% · +1.0%→54% · +2.0%→29% · +3.0%→11% · +5.0%→4% · +8.0%→2%
- Range intraday médian 2.58% (p90 4.79%) · excursion haute méd. +1.02% / basse méd. −1.03%
- Profil de vol intra : ouverture 1.544% vs midi 0.547% vs clôture 0.697% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.74 · part idiosyncratique 9.23
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 73.9  _(surachat)_
- **ADX** : 21.3  _(pas de tendance nette)_
- **MACD** : hist 3.324  _(pas de croisement recent)_
- **BB** : %B 0.94 · largeur 18.5%
- **ATR** : 9.14 (69.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.18  _(distribution)_
- **Vol ratio** : 0.24  _(volume atone)_
- **Choppiness** : 34.4  _(marche directionnel)_
- **MA** : MA20 306.6 · MA50 291.88 · MA200 298.5  _(prix > MA20)_
- **Dist MA** : MA20 +8.1% · MA50 +13.5% · MA200 +11.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (27323 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
