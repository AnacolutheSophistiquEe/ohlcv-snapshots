# HOOD

**Generated** : 2026-06-23T00:22:08.479144+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $105.71  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $105.71 (+3.9% vs entrée) · entrée $101.75 · stop $98.50 · T1 $108.26 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.116 · ¼-Kelly 0.006 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $100.45–$103.05 (mid $101.75)
- Spot actuel : $105.71 (+3.9% au-dessus de la zone — repli à attendre)
- Stop : $98.50 (stop atr-based (-10.3%))
- Targets : T1 $108.26 · R/R 2.0 | T2 $114.76 · R/R 4.0 | T3 $121.27 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $98.50


## Edge, scénarios & sizing

- EV/risk : 0.116 | EV/share : $0.378 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 41.8 | bear 27.2 | side 31.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 634.0 (= 6 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 165 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.7% → cible +2.86% / stop −2.095%, p_fill 60%, 99 remplis) : P(cible|rempli) **22%** · **EV/risk -0.101** (×p_fill ; si rempli -0.35% du capital)
  - **swing** (entrée dip −3.742% → cible +6.394% / stop −3.197%, p_fill 50%, 80 remplis) : P(cible|rempli) **30%** · **EV/risk -0.005** (×p_fill ; si rempli -0.04% du capital)
  - **deep** (entrée dip −5.79% → cible +9.043% / stop −4.521%, p_fill 46%, 72 remplis) : P(cible|rempli) **24%** · **EV/risk -0.174** (×p_fill ; si rempli -1.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→69% · +2.0%→50% · +3.0%→36% · +5.0%→14% · +8.0%→4%
- Range intraday médian 4.77% (p90 8.67%) · excursion haute méd. +1.98% / basse méd. −2.24%
- Profil de vol intra : ouverture 3.229% vs midi 1.046% vs clôture 0.987% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.63 · part idiosyncratique 1.3
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.2  _(momentum haussier)_
- **ADX** : 27.4  _(tendance etablie)_
- **MACD** : hist 2.098  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 44.4%
- **ATR** : 7.26 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.186  _(accumulation)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 42.0  _(transition)_
- **MA** : MA20 89.51 · MA50 83.51 · MA200 102.82  _(prix > MA20)_
- **Dist MA** : MA20 +18.1% · MA50 +26.6% · MA200 +2.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (27622 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
