# 207940

**Generated** : 2026-11-10T01:19:31.324539+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩1481000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-1 sess · macro taux)  
> ↳ spot ₩1481000.00 (+14.0% vs entrée) · entrée ₩1298950.00 · stop ₩1206632.19 · T1 ₩1483585.61 · R/R 2.0  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈210) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 1481000.0 · ATR Wilder 71717.83 (4.84 %)_
- **Swing** : plage **1388214.54 → 1341980.07** (-6.27 % a -9.39 % sous la cloture, 0.64 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 1386857.38-1417608.12 (B) ; 1349956.5-1381000.0 (A). stop INDICATIF 1275659.21 (-4.94 % sous le bas ; sous le support 1311518.12-1336000.0 (- 0,5 ATR)).
- **Deep** : plage **1341980.07 → 1212504.17** (-9.39 % a -18.13 % sous la cloture, 1.81 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1311518.12-1336000.0 (B) ; 1270004.75-1304000.0 (B) ; 1228000.0-1258000.0 (B) ; 1183902.62-1219266.0 (A). stop INDICATIF 1109605.33 (-8.49 % sous le bas ; sous le support 1145464.25-1180827.62 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.35 ATR sous le plus haut 20 s., RSI(2) 18.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 1386857.38-1417608.12 (B, -4.28 %) ; 1349956.5-1381000.0 (A, -6.75 %) ; 1311518.12-1336000.0 (B, -9.79 %) ; 1270004.75-1304000.0 (B, -11.95 %) ; 1228000.0-1258000.0 (B, -15.06 %) ; 1183902.62-1219266.0 (A, -17.67 %)
- Resistances reelles au-dessus : 1509860.25-1545223.62 (A, 1.95 %) ; 1548298.75-1582124.5 (A, 4.54 %) ; 1586000.0-1619000.0 (A, 7.09 %) ; 1623000.0-1657000.0 (A, 9.59 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (18.53 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 18.53 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.313 % | p01 -2.671 % | pire -5.458 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1808** [0.129 ; 0.2432] _(largeur 11.4 pt, n_eff 173.1)_
   - swing : **0.1444** [0.1104 ; 0.1844] _(largeur 7.4 pt, n_eff 345.6)_
   - deep : **0.1689** [0.1322 ; 0.2111] _(largeur 7.9 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.53 %** | CVaR **-6.0 %** | vol 2.79 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.57 % contre 3.21 % aujourd'hui, rapport 0.49)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.69 % vs -6.32 % si l'on extrapolait par √5 _(rapport 0.901 ; < 1 = le √5 surestime)_
- **β de baisse : 0.2342** (β de hausse 0.193, asymétrie 1.2131) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.049 | EV/share : ₩-4532.125 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 5 % | T2 1 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈210) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 64.3 | bear 30.6 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→52% · +2.0%→33% · +3.0%→21% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.74% (p90 6.11%) · excursion haute méd. +1.03% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.386% vs midi 0.652% vs clôture 0.805% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 20% · trend ↑1%/↓2% ; spike-down 56% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.164 ; mean-reverting — autocorr -0.063)_ ; drift intra méd. 0.083% ; recovery-V 35%
- **σ réalisé intraday** 2.379% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 54% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 1394525.0 (VA 1380575.0–1411575.0 ; dernier close 1358000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 49% · rebond 67% · **stop −2.57%** sous le fill (sous le bruit) · cible +1.87% · R/R 0.73 (high win-rate)
- Gaps overnight (n=152) : méd. 0.0% · baisse 49% (gap-down >1% 17% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.86% (p90 −2.14%) · haut méd +0.49% · range méd 1.46%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.69%) · haut méd +0.56% · range méd 1.94%
- Excursion ouverture 30min (n=160) : bas méd −1.26% (p90 −3.02%) · haut méd +0.59% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.36% (p90 −3.27%) · haut méd +0.85% · range méd 2.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1361000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 85% (119/152) · gap 28% · délai 0.2min · rebond 48% (57/119) (MFE +0.94%)
   - −1.0% : fill 30min 56% · séance 69% (97/152) · gap 17% · délai 0.2min · rebond 57% (50/97) (MFE +1.04%)
   - −1.5% : fill 30min 46% · séance 58% (80/152) · gap 6% · délai 1.1min · rebond 64% (42/80) (MFE +1.51%)
   - −2.0% : fill 30min 33% · séance 49% (66/152) · gap 4% · délai 1.7min · rebond 67% (39/66) (MFE +1.87%)
   - −3.0% : fill 30min 11% · séance 25% (38/152) · gap 2% · délai 100.9min · rebond 49% (19/38) (MFE +0.96%)
   - −4.0% : fill 30min 6% · séance 14% (21/152) · gap 2% · délai 66.4min · rebond 49% (10/21) (MFE +0.99%)
   - −5.0% : fill 30min 2% · séance 5% (10/152) · gap 2% · délai 110.1min · rebond 80% (8/10) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −2.08%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.26% (p90 −1.96%) → stop au-delà de −1.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.28% (p90 −2.04%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=437 jambes) : jambe baissière méd −1.06% (p90 −2.52%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 100% (51/51) · rebond 70% (31/51)
      · −2.0% : fill 81% (40/51) · rebond 75% (24/40)
      · −3.0% : fill 33% (21/51) · rebond 48% (10/21)
      · −4.0% : fill 20% (12/51) · rebond 56% (6/12)
      · −5.0% : fill 6% (6/51) · rebond 100% (6/6)
   - **flat** (38 séances) :
      · −1.0% : fill 60% (25/38) · rebond 35% (7/25)
      · −2.0% : fill 38% (14/38) · rebond 49% (7/14)
      · −3.0% : fill 34% (11/38) · rebond 61% (7/11)
      · −4.0% : fill 12% (5/38) · rebond 60% (3/5)
      · −5.0% : fill 5% (2/38) · rebond 55% (1/2)
   - **gap-up** (63 séances) :
      · −1.0% : fill 38% (21/63) · rebond 43% (12/21)
      · −2.0% : fill 19% (12/63) · rebond 53% (8/12)
      · −3.0% : fill 10% (6/63) · rebond 25% (2/6)
      · −4.0% : fill 9% (4/63) · rebond 19% (1/4)
      · −5.0% : fill 3% (2/63) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 82% si les 15 1res min sont vertes (54 cas) · 27% si rouges (106 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **24min** → P(séance verte=clôture>ouverture) 80% si début vert vs 23% si rouge (base 45% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 220min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **80%** · continue >prix actuel 56% ; creux résiduel méd -1.04% (q20 -1.93%) → **SL/trailing à −1.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.36% / q75 +2.68% → **scale +1.36% / runner +2.68%**, sortie à la clôture
  - **si ROUGE au coude** (n=99) : edge inversé — récupère vert seulement **23%** (continue à baisser 62%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.25%** (au-delà de la MAE q10 -3.25%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.87% .. +3.56%] · haut q95 +4.01% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.23% .. +3.26%] · haut q95 +4.89% · bas q05 -3.58%
   - 2h (n=160) : retour [-3.33% .. +3.85%] · haut q95 +5.25% · bas q05 -4.14%
   - 4h (n=160) : retour [-3.97% .. +5.05%] · haut q95 +5.77% · bas q05 -4.69%
   - 6h (n=160) : retour [-4.44% .. +6.15%] · haut q95 +7.4% · bas q05 -5.32%
   - session (n=160) : retour [-4.24% .. +6.03%] · haut q95 +7.4% · bas q05 -5.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.13%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.16 · part idiosyncratique 0.84
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.5  _(momentum haussier)_
- **ADX** : 21.2  _(pas de tendance nette)_
- **MACD** : hist 13409.755  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 25.8%
- **ATR** : 77000.0 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.124  _(accumulation)_
- **Vol ratio** : 0.1  _(volume atone)_
- **Choppiness** : 58.9  _(transition)_
- **MA** : MA20 1411800.0 · MA50 1405692.23 · MA200 1502938.06  _(prix > MA20)_
- **Dist MA** : MA20 +4.9% · MA50 +5.4% · MA200 -1.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (221425 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
