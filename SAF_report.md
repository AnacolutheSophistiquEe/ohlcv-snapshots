# SAF

**Generated** : 2026-06-24T00:07:10.580623+00:00  
**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €332.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €332.20 (+7.4% vs entrée) · entrée €309.17 · stop €305.85 · T1 €315.80 · R/R 2.0  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.137 · ¼-Kelly 0.011 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 143 % hors [0,100] (R² max 0.19). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 78.9 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €307.84–€310.49 (mid €309.17)
- Spot actuel : €332.20 (+7.4% au-dessus de la zone — repli à attendre)
- Stop : €305.85 (stop swing_plan-based (-7.93%))
- Targets : T1 €315.80 · R/R 2.0 | T2 €322.44 · R/R 4.0 | T3 €329.08 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €305.85


## Edge, scénarios & sizing

- EV/risk : 0.137 | EV/share : €0.453 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 21 % | T3 9 %
- Kelly (position) : f* 0.042 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 13.6 | bear 29.2 | side 57.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 332.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→59% · +2.0%→36% · +3.0%→15% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.87% (p90 5.22%) · excursion haute méd. +1.2% / basse méd. −1.17%
- Profil de vol intra : ouverture 1.714% vs midi 0.678% vs clôture 0.805% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (133 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 37% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; neutre — autocorr -0.011)_ ; drift intra méd. 0.454% ; recovery-V 19%
- **σ réalisé intraday** 2.059% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 52% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 330.015 (VA 328.935–330.465 ; dernier close 331.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 21% · rebond 65% · **stop −1.62%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.8 (high win-rate)
- Gaps overnight (n=132) : méd. -0.06% · baisse 50% (gap-down >1% 14% · >2% 2%)
- Excursion ouverture 5min (n=133) : bas méd −0.36% (p90 −1.52%) · haut méd +0.27% · range méd 0.97%
- Excursion ouverture 15min (n=133) : bas méd −0.38% (p90 −1.91%) · haut méd +0.48% · range méd 1.22%
- Excursion ouverture 30min (n=133) : bas méd −0.46% (p90 −1.95%) · haut méd +0.57% · range méd 1.33%
- Excursion ouverture 60min (n=133) : bas méd −0.67% (p90 −2.04%) · haut méd +0.69% · range méd 1.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 331.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 67% (94/132) · gap 28% · délai 0.2min · rebond 36% (34/94) (MFE +0.68%)
   - −1.0% : fill 30min 40% · séance 50% (67/132) · gap 14% · délai 0.3min · rebond 39% (23/67) (MFE +0.53%)
   - −1.5% : fill 30min 30% · séance 44% (58/132) · gap 6% · délai 5.1min · rebond 37% (19/58) (MFE +0.89%)
   - −2.0% : fill 30min 16% · séance 34% (42/132) · gap 2% · délai 32.5min · rebond 51% (19/42) (MFE +1.07%)
   - −3.0% : fill 30min 6% · séance 21% (25/132) · gap 1% · délai 102.5min · rebond 65% (16/25) (MFE +1.3%)
   - −4.0% : fill 30min 3% · séance 10% (12/132) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/132) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.2% (p90 −0.97%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=164 jambes) : jambe baissière méd −1.08% (p90 −2.73%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 74% (36/47) · rebond 38% (13/36)
      · −2.0% : fill 56% (26/47) · rebond 56% (13/26)
      · −3.0% : fill 33% (15/47) · rebond 67% (9/15)
      · −4.0% : fill 17% (8/47) · rebond 59% (4/8)
      · −5.0% : fill 3% (2/47) · rebond 0% (0/2)
   - **flat** (35 séances) :
      · −1.0% : fill 48% (15/35) · rebond 55% (7/15)
      · −2.0% : fill 25% (7/35) · rebond 50% (3/7)
      · −3.0% : fill 12% (4/35) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/35) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (50 séances) :
      · −1.0% : fill 25% (16/50) · rebond 26% (3/16)
      · −2.0% : fill 16% (9/50) · rebond 34% (3/9)
      · −3.0% : fill 12% (6/50) · rebond 55% (4/6)
      · −4.0% : fill 8% (3/50) · rebond 30% (1/3)
      · −5.0% : fill 2% (1/50) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=133) : 48% en base · 67% si les 15 1res min sont vertes (59 cas) · 28% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=133) : retour [-1.88% .. +2.23%] · haut q95 +2.79% · bas q05 -2.42%
   - 60min (n=133) : retour [-1.84% .. +2.56%] · haut q95 +3.32% · bas q05 -2.8%
   - session (n=133) : retour [-3.14% .. +3.78%] · haut q95 +4.54% · bas q05 -4.48%


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.74 · part idiosyncratique 0.26
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 78.9  _(surachat)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist 3.023  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 19.4%
- **ATR** : 9.29 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.131  _(distribution)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 35.0  _(marche directionnel)_
- **MA** : MA20 308.45 · MA50 292.39 · MA200 298.78  _(prix > MA20)_
- **Dist MA** : MA20 +7.7% · MA50 +13.6% · MA200 +11.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (42262 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
