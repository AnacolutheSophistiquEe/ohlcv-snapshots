# 207940

**Generated** : 2026-10-30T22:02:55.765062+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩1487000.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 19/125 fenêtres (p_fill pondéré 15 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot ₩1487000.00 (+3.7% vs entrée) · entrée ₩1433375.00 · stop ₩1318705.00 · T1 ₩1474160.71 · R/R 0.36  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-30 : 1487000.0 · ATR Wilder 68614.48 (4.61 %)_
- **Swing** : plage **1398314.51 → 1353801.39** (-5.96 % a -8.96 % sous la cloture, 0.65 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 1381000.0-1414533.12 (B). stop INDICATIF 1301692.76 (-3.85 % sous le bas ; sous le support 1336000.0-1353031.62 (- 0,5 ATR)).
- **Deep** : plage **1353801.39 → 1222518.08** (-8.96 % a -17.79 % sous la cloture, 1.91 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1336000.0-1353031.62 (B) ; 1300000.0-1320743.38 (B) ; 1257704.38-1279229.88 (B) ; 1219266.0-1253091.75 (B). stop INDICATIF 1144982.88 (-6.34 % sous le bas ; sous le support 1179290.12-1205428.12 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.03 ATR sous le plus haut 20 s., RSI(2) 89.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 1416070.62-1448000.0 (B, -2.62 %) ; 1381000.0-1414533.12 (B, -4.87 %) ; 1336000.0-1353031.62 (B, -9.01 %) ; 1300000.0-1320743.38 (B, -11.18 %) ; 1257704.38-1279229.88 (B, -13.97 %) ; 1219266.0-1253091.75 (B, -15.73 %)
- Resistances reelles au-dessus : 1537536.0-1569824.25 (A, 3.4 %) ; 1572899.25-1600574.88 (A, 5.78 %) ; 1609800.12-1637000.0 (A, 8.26 %) ; 1645000.0-1676000.0 (A, 10.63 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (13.54 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.54 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.297 % | p01 -2.573 % | pire -5.458 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0035** [0.0002 ; 0.0223] _(largeur 2.2 pt, n_eff 173.1)_
   - swing : **0.2014** [0.1617 ; 0.2461] _(largeur 8.4 pt, n_eff 345.6)_
   - deep : **0.1846** [0.1464 ; 0.228] _(largeur 8.2 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first, p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.8 observations effectives », dont la borne haute a 95 % vaut environ 17.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (13.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.53 %** | CVaR **-6.0 %** | vol 2.78 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.62 % contre 3.18 % aujourd'hui, rapport 0.51)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.77 % vs -6.32 % si l'on extrapolait par √5 _(rapport 0.914 ; < 1 = le √5 surestime)_
- **β de baisse : 0.269** (β de hausse 0.2068, asymétrie 1.3007) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.022 | EV/share : ₩-2559.364 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.1 | bear 16.6 | side 5.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.609% → cible +2.845% / stop −8.0%, p_fill 15%, n_eff≈16.8) : P(cible|rempli) **0%** · **EV/risk -0.006** (×p_fill ; si rempli -0.34% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.2 · part idiosyncratique 0.8
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 69.9  _(momentum haussier)_
- **ADX** : 22.0  _(pas de tendance nette)_
- **MACD** : hist 17742.231  _(pas de croisement recent)_
- **BB** : %B 0.89 · largeur 28.0%
- **ATR** : 81571.43 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.122  _(accumulation)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 46.0  _(transition)_
- **MA** : MA20 1341318.18 · MA50 1416912.23 · MA200 1515683.06  _(prix > MA20)_
- **Dist MA** : MA20 +10.9% · MA50 +4.9% · MA200 -1.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (502267 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
