# 000660

**Generated** : 2026-10-13T21:51:54.683025+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1443000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩1443000.00 (+2.8% vs entrée) · entrée ₩1404336.32 · stop ₩1325836.32 · T1 ₩1550150.00 · R/R 1.86  
> ↳ ¼-Kelly 0.046 · _first-passage empirique daily (historique réel, n≈210) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -265 % hors [0,100] (R² max 0.58). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 12.7 < 20 (tendance pas encore confirmée) alors que Choppiness 29.1 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-13 : 1443000.0 · ATR Wilder 90931.86 (6.3 %)_
- **Swing** : plage **1339773.13 → 1272769.54** (-7.15 % a -11.8 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 1200263.93 (-5.7 % sous le bas ; sous le support 1245729.86-1245729.86 (- 0,5 ATR)).
- **Deep** : plage **1272769.54 → 1121511.39** (-11.8 % a -22.28 % sous la cloture, 1.66 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1245729.86-1245729.86 (C). stop INDICATIF 996133.96 (-11.18 % sous le bas ; sous le support 1041599.89-1077586.1 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.41 ATR sous le plus haut 20 s., RSI(2) 0.6. Limite **1397534.07** (seance suivante), stop catastrophe 1033806.65, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 1245729.86-1245729.86 (C, -13.67 %) ; 1041599.89-1077586.1 (B, -25.32 %) ; 883660.61-989619.88 (B, -31.42 %) ; 772277.75-807689.81 (A, -44.03 %) ; 722389.03-731369.02 (B, -49.32 %) ; 591680.52-623609.38 (B, -56.78 %)
- Resistances reelles au-dessus : 1556662.48-1558000.0 (B, 7.88 %) ; 1671000.0-1689351.12 (A, 15.8 %) ; 1717627.62-1736000.0 (A, 19.03 %) ; 1791611.52-1791611.57 (C, 24.16 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.56 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.12 %)** : le gap seul le franchit 0.656 % des séances (8 fois sur 1219).
   - exécution **1.096 pt plus bas** dans le cas TYPIQUE (médiane), 2.375 au p90, **2.74 au pire**
   - perte réelle **9.358 %** en moyenne _(tirée par la queue)_, jusqu'à **10.86 %** — au lieu des 8.12 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0081 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.45 % | p01 -6.994 % | pire -10.86 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.497** [0.4231 ; 0.571] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4046** [0.3538 ; 0.457] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.3332** [0.2851 ; 0.3841] _(largeur 9.9 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-9.19 %** | CVaR **-11.46 %** | vol 5.76 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.81 % contre 6.63 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.53 % vs -10.81 % si l'on extrapolait par √5 _(rapport 0.881 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4149** (β de hausse 1.623, asymétrie 0.8718) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.335 | EV/share : ₩26315.469 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 22 % | T3 10 %
- Kelly (position) : f* 0.184 | ¼-Kelly 0.046 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈210) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 8.5 | bear 6.5 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.218% → cible +2.754% / stop −1.652%, p_fill 65%, n_eff≈73.0) : P(cible|rempli) **23%** · **EV/risk -0.186** (×p_fill ; si rempli -0.47% du capital)
  - **swing** (entrée dip −2.68% → cible +10.383% / stop −5.59%, p_fill 59%, n_eff≈67.9) : P(cible|rempli) **25%** · **EV/risk -0.118** (×p_fill ; si rempli -1.12% du capital)
  - **deep** (entrée dip −4.14% → cible +12.066% / stop −8.513%, p_fill 57%, n_eff≈61.7) : P(cible|rempli) **35%** · **EV/risk -0.087** (×p_fill ; si rempli -1.29% du capital)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.22 · part idiosyncratique 0.78
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.7  _(survente)_
- **ADX** : 12.7  _(pas de tendance nette)_
- **MACD** : hist -35869.629  _(pas de croisement recent)_
- **BB** : %B -0.27 · largeur 23.5%
- **ATR** : 78500.0 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.283  _(distribution)_
- **Vol ratio** : 1.7  _(volume au-dessus de la moyenne)_
- **Choppiness** : 29.1  _(marche directionnel)_
- **MA** : MA20 1759550.0 · MA50 1671976.46 · MA200 1444547.92  _(prix < MA20)_
- **Dist MA** : MA20 -18.0% · MA50 -13.7% · MA200 -0.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (602530 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
