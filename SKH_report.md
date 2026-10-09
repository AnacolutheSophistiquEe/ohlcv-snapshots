# 000660

**Generated** : 2026-10-09T21:55:17.266268+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1681000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot ₩1681000.00 (+0.5% vs entrée) · entrée ₩1672065.19 · stop ₩1602993.76 · T1 ₩1749289.39 · R/R 1.12  
> ↳ ¼-Kelly 0.058 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 1681000.0 · ATR Wilder 84702.03 (5.04 %)_
- **Swing** : plage **1584845.29 → 1523025.8** (-5.72 % a -9.4 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 1556662.48-1558000.0 (B). stop INDICATIF 1438323.77 (-5.56 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **1523025.8 → 1381537.54** (-9.4 % a -17.81 % sous la cloture, 1.67 ATR) — touchee 41 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 1296835.51 (-6.13 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (3.0 ATR sous le plus haut 20 s., RSI(2) 5.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 1556662.48-1558000.0 (B, -7.32 %) ; 1245729.86-1245729.86 (C, -25.89 %) ; 1041599.96-1077586.1 (B, -35.9 %) ; 926644.12-989619.88 (B, -41.13 %) ; 883660.61-902986.35 (B, -46.28 %) ; 772277.81-807689.75 (A, -51.95 %)
- Resistances reelles au-dessus : 1717627.62-1736000.0 (A, 2.18 %) ; 1791611.52-1791611.57 (C, 6.58 %) ; 1854597.89-1890000.0 (A, 10.33 %) ; 1994234.05-2005565.09 (B, 18.63 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.48 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (4.64 %)** : le gap seul le franchit 2.297 % des séances (28 fois sur 1219).
   - exécution **2.017 pt plus bas** dans le cas TYPIQUE (médiane), 4.841 au p90, **6.22 au pire**
   - perte réelle **7.035 %** en moyenne _(tirée par la queue)_, jusqu'à **10.86 %** — au lieu des 4.64 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.055 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.443 % | p01 -6.994 % | pire -10.86 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4714** [0.398 ; 0.5457] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4275** [0.3761 ; 0.4801] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.3833** [0.3332 ; 0.4354] _(largeur 10.2 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 98.3 observations effectives », dont la borne haute a 95 % vaut environ 3.1 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.73 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.88 % contre 6.56 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.74 % si l'on extrapolait par √5 _(rapport 0.875 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4162** (β de hausse 1.6231, asymétrie 0.8725) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.339 | EV/share : ₩23377.456 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 40 % | T3 27 %
- Kelly (position) : f* 0.232 | ¼-Kelly 0.058 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.0 | bear 6.7 | side 8.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.325% → cible +2.061% / stop −1.5%, p_fill 84%, n_eff≈90.8) : P(cible|rempli) **30%** · **EV/risk -0.200** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −0.531% → cible +4.618% / stop −4.131%, p_fill 84%, n_eff≈98.3) : P(cible|rempli) **43%** · **EV/risk -0.161** (×p_fill ; si rempli -0.79% du capital)
  - **deep** (entrée dip −0.691% → cible +15.001% / stop −7.501%, p_fill 89%, n_eff≈99.5) : P(cible|rempli) **36%** · **EV/risk +0.133** (×p_fill ; si rempli +1.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→54% · +3.0%→38% · +5.0%→21% · +8.0%→8%
- Range intraday médian 5.51% (p90 10.55%) · excursion haute méd. +2.19% / basse méd. −2.54%
- Profil de vol intra : ouverture 2.923% vs midi 1.197% vs clôture 1.401% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 57% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.174% ; recovery-V 21%
- **σ réalisé intraday** 2.966% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 58% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1845912.5 (VA 1837812.5–1847937.5 ; dernier close 1843000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 70% · **stop −7.14%** sous le fill (sous le bruit) · cible +2.04% · R/R 0.29 (high win-rate)
- Gaps overnight (n=152) : méd. 0.6% · baisse 45% (gap-down >1% 29% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.8%) · haut méd +0.76% · range méd 1.36%
- Excursion ouverture 15min (n=160) : bas méd −0.84% (p90 −2.29%) · haut méd +0.95% · range méd 1.86%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −3.02%) · haut méd +1.28% · range méd 2.47%
- Excursion ouverture 60min (n=160) : bas méd −1.23% (p90 −3.82%) · haut méd +1.38% · range méd 2.98%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1841000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 63% (93/152) · gap 37% · délai 0.0min · rebond 60% (53/93) (MFE +1.37%)
   - −1.0% : fill 30min 45% · séance 59% (86/152) · gap 29% · délai 0.0min · rebond 61% (55/86) (MFE +1.52%)
   - −1.5% : fill 30min 36% · séance 53% (78/152) · gap 24% · délai 0.1min · rebond 69% (53/78) (MFE +1.6%)
   - −2.0% : fill 30min 30% · séance 42% (69/152) · gap 22% · délai 0.0min · rebond 61% (45/69) (MFE +1.77%)
   - −3.0% : fill 30min 26% · séance 38% (59/152) · gap 18% · délai 0.8min · rebond 69% (40/59) (MFE +1.74%)
   - −4.0% : fill 30min 21% · séance 31% (50/152) · gap 12% · délai 1.0min · rebond 64% (35/50) (MFE +2.2%)
   - −5.0% : fill 30min 13% · séance 24% (38/152) · gap 7% · délai 12.9min · rebond 70% (25/38) (MFE +2.04%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.29% (p90 −2.29%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −2.55%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.65%) → stop au-delà de −2.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=831 jambes) : jambe baissière méd −1.2% (p90 −3.25%) · ~10.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 97% (59/60) · rebond 57% (33/59)
      · −2.0% : fill 73% (50/60) · rebond 49% (28/50)
      · −3.0% : fill 70% (45/60) · rebond 62% (28/45)
      · −4.0% : fill 62% (41/60) · rebond 59% (27/41)
      · −5.0% : fill 46% (31/60) · rebond 62% (18/31)
   - **flat** (10 séances) :
      · −1.0% : fill 27% (6/10) · rebond 100% (6/6)
      · −2.0% : fill 14% (3/10) · rebond 100% (3/3)
      · −3.0% : fill 10% (2/10) · rebond 100% (2/2)
      · −4.0% : fill 0% (0/10) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/10) · rebond 0% (0/0)
   - **gap-up** (82 séances) :
      · −1.0% : fill 33% (21/82) · rebond 66% (16/21)
      · −2.0% : fill 23% (16/82) · rebond 87% (14/16)
      · −3.0% : fill 17% (12/82) · rebond 86% (10/12)
      · −4.0% : fill 11% (9/82) · rebond 83% (8/9)
      · −5.0% : fill 10% (7/82) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 58% si les 15 1res min sont vertes (84 cas) · 28% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 70% si début vert vs 11% si rouge (base 45% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 223min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=89) : tient le vert **70%** · continue >prix actuel 54% ; creux résiduel méd -1.24% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.89% → **scale +1.55% / runner +2.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **11%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.13%** (au-delà de la MAE q10 -6.13%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.02% .. +2.58%] · haut q95 +3.28% · bas q05 -3.89%
   - 60min (n=160) : retour [-3.3% .. +4.21%] · haut q95 +4.7% · bas q05 -5.02%
   - 2h (n=160) : retour [-4.39% .. +4.41%] · haut q95 +5.98% · bas q05 -6.58%
   - 4h (n=160) : retour [-6.22% .. +5.15%] · haut q95 +6.66% · bas q05 -7.39%
   - 6h (n=160) : retour [-6.31% .. +5.01%] · haut q95 +7.83% · bas q05 -8.0%
   - session (n=160) : retour [-6.86% .. +5.54%] · haut q95 +8.01% · bas q05 -8.13%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 000660 = **volatil sans tendance propre (choppy)** (vol intra méd 3.1%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.21 · part idiosyncratique 0.79
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.2  _(neutre)_
- **ADX** : 9.6  _(pas de tendance nette)_
- **MACD** : hist -13087.126  _(bearish_recent)_
- **BB** : %B 0.06 · largeur 13.7%
- **ATR** : 69071.43 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.201  _(distribution)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 50.7  _(transition)_
- **MA** : MA20 1789600.0 · MA50 1678321.87 · MA200 1434975.29  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 +0.2% · MA200 +17.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (597636 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
