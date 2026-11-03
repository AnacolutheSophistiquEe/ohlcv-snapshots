# 000660

**Generated** : 2026-11-03T21:54:13.442947+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1397000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)  
> ↳ spot ₩1397000.00 (+1.2% vs entrée) · entrée ₩1380745.64 · stop ₩1273817.06 · T1 ₩1547307.14 · R/R 1.56  
> ↳ ¼-Kelly 0.036 · _first-passage empirique daily (historique réel, n≈210) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-03 : 1397000.0 · ATR Wilder 101872.39 (7.29 %)_
- **Swing** : plage **1280558.91 → 1197003.14** (-8.34 % a -14.32 % sous la cloture, 0.82 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 1245729.86-1245729.86 (C). stop INDICATIF 1095130.75 (-8.51 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **1197003.14 → 1008361.49** (-14.32 % a -27.82 % sous la cloture, 1.85 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1041599.96-1077586.1 (B). stop INDICATIF 832724.41 (-17.42 % sous le bas ; sous le support 883660.61-989619.88 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.32 ATR sous le plus haut 20 s., RSI(2) 29.9 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 1245729.86-1245729.86 (C, -10.83 %) ; 1041599.96-1077586.1 (B, -22.86 %) ; 883660.61-989619.88 (B, -29.16 %) ; 786246.67-807689.75 (A, -42.18 %) ; 722389.03-772277.81 (A, -44.72 %) ; 622165.99-644101.27 (C, -53.89 %)
- Resistances reelles au-dessus : 1556662.48-1587000.0 (A, 11.43 %) ; 1671000.0-1717627.62 (A, 19.61 %) ; 1731624.54-1736000.0 (B, 23.95 %) ; 1791611.52-1791611.57 (C, 28.25 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.89 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.82 %)** : le gap seul le franchit 0.41 % des séances (5 fois sur 1219).
   - exécution **1.125 pt plus bas** dans le cas TYPIQUE (médiane), 1.831 au p90, **2.04 au pire**
   - perte réelle **9.915 %** en moyenne _(tirée par la queue)_, jusqu'à **10.86 %** — au lieu des 8.82 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0045 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.535 % | p01 -7.068 % | pire -10.86 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4479** [0.3752 ; 0.5223] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3275** [0.2796 ; 0.3783] _(largeur 9.9 pt, n_eff 345.6)_
   - deep : **0.3099** [0.2629 ; 0.3601] _(largeur 9.7 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-9.56 %** | CVaR **-11.58 %** | vol 5.83 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.86 % contre 6.71 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.83 % vs -11.06 % si l'on extrapolait par √5 _(rapport 0.889 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4223** (β de hausse 1.6216, asymétrie 0.8771) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.183 | EV/share : ₩19567.440 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 13 % | T3 4 %
- Kelly (position) : f* 0.144 | ¼-Kelly 0.036 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈210) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 71.4 | bear 21.9 | side 6.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.524% → cible +3.847% / stop −2.308%, p_fill 80%, n_eff≈85.9) : P(cible|rempli) **17%** · **EV/risk -0.290** (×p_fill ; si rempli -0.84% du capital)
  - **swing** (entrée dip −1.166% → cible +12.063% / stop −7.744%, p_fill 78%, n_eff≈90.6) : P(cible|rempli) **22%** · **EV/risk -0.164** (×p_fill ; si rempli -1.62% du capital)
  - **deep** (entrée dip −1.698% → cible +12.678% / stop −11.68%, p_fill 82%, n_eff≈90.1) : P(cible|rempli) **34%** · **EV/risk -0.180** (×p_fill ; si rempli -2.57% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→55% · +3.0%→38% · +5.0%→23% · +8.0%→8%
- Range intraday médian 6.05% (p90 10.45%) · excursion haute méd. +2.31% / basse méd. −2.61%
- Profil de vol intra : ouverture 3.003% vs midi 1.225% vs clôture 1.446% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 62% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.404% ; recovery-V 17%
- **σ réalisé intraday** 3.303% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 65% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1222800.0 (VA 1186400.0–1253600.0 ; dernier close 1281000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 60% · **stop −7.48%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.23 (high win-rate)
- Gaps overnight (n=152) : méd. -0.07% · baisse 51% (gap-down >1% 36% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.48% (p90 −1.95%) · haut méd +0.82% · range méd 1.36%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.42%) · haut méd +1.01% · range méd 2.04%
- Excursion ouverture 30min (n=160) : bas méd −0.97% (p90 −3.27%) · haut méd +1.34% · range méd 2.54%
- Excursion ouverture 60min (n=160) : bas méd −1.28% (p90 −3.8%) · haut méd +1.49% · range méd 3.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1277000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 69% (97/152) · gap 44% · délai 0.0min · rebond 48% (51/97) (MFE +0.92%)
   - −1.0% : fill 30min 51% · séance 66% (93/152) · gap 36% · délai 0.0min · rebond 59% (58/93) (MFE +1.3%)
   - −1.5% : fill 30min 42% · séance 60% (85/152) · gap 31% · délai 0.0min · rebond 64% (55/85) (MFE +1.63%)
   - −2.0% : fill 30min 38% · séance 50% (75/152) · gap 26% · délai 0.0min · rebond 56% (46/75) (MFE +1.52%)
   - −3.0% : fill 30min 31% · séance 43% (64/152) · gap 20% · délai 1.9min · rebond 61% (41/64) (MFE +1.3%)
   - −4.0% : fill 30min 26% · séance 37% (55/152) · gap 15% · délai 3.0min · rebond 61% (37/55) (MFE +1.84%)
   - −5.0% : fill 30min 17% · séance 28% (42/152) · gap 7% · délai 6.8min · rebond 60% (26/42) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −2.29%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.35% (p90 −2.6%) → stop au-delà de −2.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.56%) → stop au-delà de −2.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=848 jambes) : jambe baissière méd −1.25% (p90 −3.37%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 55% (35/64)
      · −2.0% : fill 81% (55/65) · rebond 50% (29/55)
      · −3.0% : fill 76% (50/65) · rebond 55% (29/50)
      · −4.0% : fill 70% (46/65) · rebond 58% (29/46)
      · −5.0% : fill 51% (35/65) · rebond 54% (19/35)
   - **flat** (10 séances) :
      · −1.0% : fill 42% (6/10) · rebond 100% (6/6)
      · −2.0% : fill 11% (3/10) · rebond 100% (3/3)
      · −3.0% : fill 8% (2/10) · rebond 100% (2/2)
      · −4.0% : fill 0% (0/10) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/10) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 38% (23/77) · rebond 63% (17/23)
      · −2.0% : fill 25% (17/77) · rebond 74% (14/17)
      · −3.0% : fill 16% (12/77) · rebond 86% (10/12)
      · −4.0% : fill 10% (9/77) · rebond 83% (8/9)
      · −5.0% : fill 9% (7/77) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 56% si les 15 1res min sont vertes (87 cas) · 21% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 65% si début vert vs 9% si rouge (base 40% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 223min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=88) : tient le vert **65%** · continue >prix actuel 49% ; creux résiduel méd -1.45% (q20 -3.7%) → **SL/trailing à −3.7%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.94% → **scale +1.46% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **9%** (continue à baisser 68%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.01%** (au-delà de la MAE q10 -5.01%), cible rebond +1.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.65%] · haut q95 +3.82% · bas q05 -4.01%
   - 60min (n=160) : retour [-3.6% .. +3.81%] · haut q95 +4.68% · bas q05 -5.02%
   - 2h (n=160) : retour [-4.69% .. +4.46%] · haut q95 +5.68% · bas q05 -6.5%
   - 4h (n=160) : retour [-5.25% .. +4.7%] · haut q95 +6.4% · bas q05 -7.14%
   - 6h (n=160) : retour [-6.42% .. +5.56%] · haut q95 +7.17% · bas q05 -7.45%
   - session (n=160) : retour [-6.55% .. +6.05%] · haut q95 +7.17% · bas q05 -7.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — 000660 = **volatil sans tendance propre (choppy)** (vol intra méd 3.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.34 · part idiosyncratique 0.67
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.8  _(neutre)_
- **ADX** : 23.1  _(pas de tendance nette)_
- **MACD** : hist 22951.187  _(pas de croisement recent)_
- **BB** : %B 0.47 · largeur 47.8%
- **ATR** : 106928.57 (64.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.232  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 48.5  _(transition)_
- **MA** : MA20 1419400.0 · MA50 1616955.83 · MA200 1499380.47  _(prix < MA20)_
- **Dist MA** : MA20 -1.6% · MA50 -13.6% · MA200 -6.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (451988 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
