# 005930

**Generated** : 2026-11-17T01:15:23.508400+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩193100.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (17 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩193100.00 (+1.1% vs entrée) · entrée ₩190928.06 · stop ₩184955.35 · T1 ₩202873.48 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-17 : 193100.0 · ATR Wilder 12935.93 (6.7 %)_
- **Swing** : plage **177406.85 → 167662.33** (-8.13 % a -13.17 % sous la cloture, 0.75 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 176274.72-179200.0 (B). stop INDICATIF 157460.68 (-6.08 % sous le bas ; sous le support 163928.64-165986.31 (- 0,5 ATR)).
- **Deep** : plage **167662.33 → 136812.99** (-13.17 % a -29.15 % sous la cloture, 2.38 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 163928.64-165986.31 (A) ; 146193.37-148545.0 (B) ; 138942.5-141588.09 (A). stop INDICATIF 119442.54 (-12.7 % sous le bas ; sous le support 125910.51-130025.86 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.32 ATR sous le plus haut 20 s., RSI(2) 10.0. Limite **186632.03** (seance suivante), stop catastrophe 134888.31, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 176274.72-179200.0 (B, -7.2 %) ; 163928.64-165986.31 (A, -14.04 %) ; 146193.37-148545.0 (B, -23.07 %) ; 138942.5-141588.09 (A, -26.68 %) ; 125910.51-130025.86 (B, -32.66 %) ; 107749.45-109602.16 (C, -43.24 %)
- Resistances reelles au-dessus : 203500.0-204788.3 (A, 5.39 %) ; 218506.17-223623.24 (A, 13.16 %) ; 225340.65-228000.0 (B, 16.7 %) ; 235910.23-242299.46 (A, 22.17 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.68 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.67 %)** : le gap seul le franchit 0.164 % des séances (2 fois sur 1219).
   - exécution **1.136 pt plus bas** dans le cas TYPIQUE (médiane), 1.245 au p90, **1.272 au pire**
   - perte réelle **10.806 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 9.67 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0019 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.827 % | p01 -5.098 % | pire -10.942 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3108** [0.2454 ; 0.3824] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.2766** [0.2314 ; 0.3255] _(largeur 9.4 pt, n_eff 345.6)_
   - deep : **0.2575** [0.2136 ; 0.3055] _(largeur 9.2 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.82 %** | CVaR **-9.95 %** | vol 4.91 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.03 % contre 5.56 % aujourd'hui, rapport 0.54)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.29 % vs -7.92 % si l'on extrapolait par √5 _(rapport 0.92 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1782** (β de hausse 1.3397, asymétrie 0.8795) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 5.6 | side 9.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.127% → cible +6.257% / stop −3.128%, p_fill 67%, n_eff≈73.1) : P(cible|rempli) **6%** · **EV/risk -0.270** (×p_fill ; si rempli -1.26% du capital)
  - **swing** (entrée dip −2.475% → cible +7.727% / stop −7.377%, p_fill 62%, n_eff≈72.4) : P(cible|rempli) **30%** · **EV/risk -0.154** (×p_fill ; si rempli -1.83% du capital)
  - **deep** (entrée dip −3.829% → cible +18.286% / stop −11.221%, p_fill 61%, n_eff≈67.1) : P(cible|rempli) **14%** · **EV/risk -0.114** (×p_fill ; si rempli -2.10% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.25 · part idiosyncratique 0.75
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 24.4  _(survente)_
- **ADX** : 22.8  _(pas de tendance nette)_
- **MACD** : hist -298.819  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 27.7%
- **ATR** : 13892.86 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.049  _(neutre)_
- **Vol ratio** : 0.21  _(volume atone)_
- **Choppiness** : 38.8  _(transition)_
- **MA** : MA20 212145.0 · MA50 236991.98 · MA200 237385.73  _(prix < MA20)_
- **Dist MA** : MA20 -9.0% · MA50 -18.5% · MA200 -18.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (405026 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
