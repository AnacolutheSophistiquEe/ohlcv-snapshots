# 005930

**Generated** : 2026-11-27T21:53:07.820752+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩179300.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (25 séance(s) de retard, drapeau lu sur first_passage_by_horizon); usable=false (intervalle le plus large 25.2 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩179300.00 (+2.1% vs entrée) · entrée ₩175685.68 · stop ₩171887.94 · T1 ₩183281.16 · R/R 2.0  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.16% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-27 : 179300.0 · ATR Wilder 12643.39 (7.05 %)_
- **Swing** : plage **163909.58 → 154176.79** (-8.58 % a -14.01 % sous la cloture, 0.77 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 139871.67 (-9.28 % sous le bas ; sous le support 146193.36-148545.01 (- 0,5 ATR)).
- **Deep** : plage **154176.79 → 124079.11** (-14.01 % a -30.8 % sous la cloture, 2.38 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 146193.36-148545.01 (B) ; 138942.48-141588.09 (A) ; 125910.51-130025.88 (B). stop INDICATIF 101427.76 (-18.26 % sous le bas ; sous le support 107749.46-109602.16 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.17 ATR sous le plus haut 20 s., RSI(2) 64.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 163928.63-165986.3 (A, -7.43 %) ; 146193.36-148545.01 (B, -17.15 %) ; 138942.48-141588.09 (A, -21.03 %) ; 125910.51-130025.88 (B, -27.48 %) ; 107749.46-109602.16 (C, -38.87 %) ; 100143.61-103361.47 (A, -42.35 %)
- Resistances reelles au-dessus : 185975.9-190874.46 (A, 3.72 %) ; 203500.0-204788.31 (A, 13.5 %) ; 210612.49-216000.0 (B, 17.46 %) ; 218506.19-223623.24 (A, 21.87 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.92 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.74 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1219).
   - exécution **0.202 pt plus bas** dans le cas TYPIQUE (médiane), 0.202 au p90, **0.202 au pire**
   - perte réelle **10.942 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 10.74 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0002 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.986 % | p01 -5.322 % | pire -10.942 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4384** [0.366 ; 0.5128] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.326** [0.2782 ; 0.3767] _(largeur 9.9 pt, n_eff 345.6)_
   - deep : **0.2852** [0.2395 ; 0.3344] _(largeur 9.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (25.2 pt), swing (26.9 pt), deep (27.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.26 %** | CVaR **-10.11 %** | vol 4.98 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.60 % contre 5.59 % aujourd'hui, rapport 0.46)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.5 % vs -8.16 % si l'on extrapolait par √5 _(rapport 0.919 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1883** (β de hausse 1.3326, asymétrie 0.8917) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.09 | EV/share : ₩-341.720 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.2 | bear 81.4 | side 13.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.012% → cible +4.323% / stop −2.162%, p_fill 53%, n_eff≈58.1) : P(cible|rempli) **9%** · **EV/risk -0.272** (×p_fill ; si rempli -1.12% du capital)
  - **swing** (entrée dip −4.432% → cible +6.964% / stop −6.601%, p_fill 43%, n_eff≈50.5) : P(cible|rempli) **35%** · **EV/risk -0.065** (×p_fill ; si rempli -1.00% du capital)
  - **deep** (entrée dip −6.858% → cible +21.628% / stop −10.814%, p_fill 42%, n_eff≈47.7) : P(cible|rempli) **11%** · **EV/risk -0.073** (×p_fill ; si rempli -1.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→47% · +3.0%→34% · +5.0%→18% · +8.0%→3%
- Range intraday médian 5.16% (p90 8.97%) · excursion haute méd. +1.89% / basse méd. −2.23%
- Profil de vol intra : ouverture 2.706% vs midi 1.151% vs clôture 1.316% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.097)_ ; drift intra méd. -0.205% ; recovery-V 27%
- **σ réalisé intraday** 2.986% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 64% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 212950.0 (VA 208450.0–215050.0 ; dernier close 215500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 21% · rebond 72% · **stop −4.9%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.31 (high win-rate)
- Gaps overnight (n=152) : méd. 1.23% · baisse 35% (gap-down >1% 24% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.51% (p90 −1.56%) · haut méd +0.59% · range méd 1.29%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.15%) · haut méd +0.77% · range méd 2.07%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.68%) · haut méd +0.98% · range méd 2.36%
- Excursion ouverture 60min (n=160) : bas méd −1.21% (p90 −3.39%) · haut méd +1.18% · range méd 2.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 215500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 43% · séance 55% (77/152) · gap 33% · délai 0.0min · rebond 48% (39/77) (MFE +0.95%)
   - −1.0% : fill 30min 39% · séance 50% (71/152) · gap 24% · délai 0.0min · rebond 52% (37/71) (MFE +1.2%)
   - −1.5% : fill 30min 32% · séance 44% (65/152) · gap 21% · délai 0.3min · rebond 59% (37/65) (MFE +1.11%)
   - −2.0% : fill 30min 27% · séance 39% (57/152) · gap 17% · délai 0.1min · rebond 53% (32/57) (MFE +1.46%)
   - −3.0% : fill 30min 17% · séance 30% (44/152) · gap 13% · délai 4.2min · rebond 54% (26/44) (MFE +1.25%)
   - −4.0% : fill 30min 14% · séance 27% (39/152) · gap 5% · délai 10.6min · rebond 47% (21/39) (MFE +0.93%)
   - −5.0% : fill 30min 11% · séance 21% (32/152) · gap 3% · délai 24.1min · rebond 72% (25/32) (MFE +1.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −1.78%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.98%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −2.15%) → stop au-delà de −1.53% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=773 jambes) : jambe baissière méd −1.19% (p90 −2.81%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 100% (47/47) · rebond 55% (24/47)
      · −2.0% : fill 81% (40/47) · rebond 44% (20/40)
      · −3.0% : fill 65% (32/47) · rebond 45% (16/32)
      · −4.0% : fill 60% (28/47) · rebond 43% (15/28)
      · −5.0% : fill 48% (23/47) · rebond 68% (17/23)
   - **flat** (9 séances) :
      · −1.0% : fill 48% (5/9) · rebond 27% (2/5)
      · −2.0% : fill 48% (5/9) · rebond 27% (2/5)
      · −3.0% : fill 44% (4/9) · rebond 64% (3/4)
      · −4.0% : fill 44% (4/9) · rebond 34% (2/4)
      · −5.0% : fill 44% (4/9) · rebond 70% (3/4)
   - **gap-up** (96 séances) :
      · −1.0% : fill 23% (19/96) · rebond 49% (11/19)
      · −2.0% : fill 14% (12/96) · rebond 90% (10/12)
      · −3.0% : fill 9% (8/96) · rebond 91% (7/8)
      · −4.0% : fill 7% (7/96) · rebond 72% (4/7)
      · −5.0% : fill 4% (5/96) · rebond 100% (5/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 64% si les 15 1res min sont vertes (79 cas) · 20% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:17** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 42% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 77min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **82%** · continue >prix actuel 58% ; creux résiduel méd -1.18% (q20 -2.31%) → **SL/trailing à −2.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.58% / q75 +2.99% → **scale +1.58% / runner +2.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **8%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.13%** (au-delà de la MAE q10 -5.13%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.52% .. +3.07%] · haut q95 +3.45% · bas q05 -3.33%
   - 60min (n=160) : retour [-2.99% .. +3.07%] · haut q95 +4.3% · bas q05 -3.65%
   - 2h (n=160) : retour [-3.97% .. +4.52%] · haut q95 +5.82% · bas q05 -5.0%
   - 4h (n=160) : retour [-5.32% .. +5.06%] · haut q95 +6.21% · bas q05 -6.7%
   - 6h (n=160) : retour [-5.49% .. +4.64%] · haut q95 +6.65% · bas q05 -7.05%
   - session (n=160) : retour [-5.1% .. +5.3%] · haut q95 +6.65% · bas q05 -7.05%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 3.02%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.8  _(momentum baissier)_
- **ADX** : 23.9  _(pas de tendance nette)_
- **MACD** : hist -936.25  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 32.2%
- **ATR** : 11310.71 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.171  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 46.0  _(transition)_
- **MA** : MA20 195775.0 · MA50 225066.96 · MA200 238562.18  _(prix < MA20)_
- **Dist MA** : MA20 -8.4% · MA50 -20.3% · MA200 -24.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (394200 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
