# 207940

**Generated** : 2026-10-09T00:21:43.395059+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · ₩1219000.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 26/125 fenêtres (p_fill pondéré 20 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot ₩1219000.00 (+3.4% vs entrée) · entrée ₩1178571.60 · stop ₩1084285.87 · T1 ₩1198785.80 · R/R 0.21  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -1793 % hors [0,100] (R² max 0.53). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 1219000.0 · ATR Wilder 45260.84 (3.71 %)_
- **Swing** : plage **1160084.58 → 1130761.46** (-4.83 % a -7.24 % sous la cloture, 0.65 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 1148539.38-1162377.12 (B) ; 1125476.25-1145464.25 (A). stop INDICATIF 1078245.33 (-4.64 % sous le bas ; sous le support 1100875.75-1122401.25 (- 0,5 ATR)).
- **Deep** : plage **1130761.46 → 1051000.77** (-7.24 % a -13.78 % sous la cloture, 1.76 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1125476.25-1145464.25 (A) ; 1100875.75-1122401.25 (A) ; 1067050.0-1077812.75 (A). stop INDICATIF 1004443.58 (-4.43 % sous le bas ; sous le support 1027074.0-1027074.0 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.74 ATR sous le plus haut 20 s., RSI(2) 2.9. Limite **1196369.58** (seance suivante), stop catastrophe 1015326.22, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 1179290.12-1197740.5 (B, -1.74 %) ; 1148539.38-1162377.12 (B, -4.65 %) ; 1125476.25-1145464.25 (A, -6.03 %) ; 1100875.75-1122401.25 (A, -7.92 %) ; 1067050.0-1077812.75 (A, -11.58 %) ; 1027074.0-1027074.0 (C, -15.74 %)
- Resistances reelles au-dessus : 1253091.75-1270004.75 (A, 2.8 %) ; 1279229.88-1300000.0 (A, 4.94 %) ; 1304000.0-1320743.38 (A, 6.97 %) ; 1336000.0-1353031.62 (A, 9.6 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (9.95 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 9.95 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.254 % | p01 -2.573 % | pire -5.458 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0036** [0.0002 ; 0.0225] _(largeur 2.2 pt, n_eff 173.1)_
   - swing : **0.4489** [0.3971 ; 0.5016] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4223** [0.3711 ; 0.4748] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 23.0 observations effectives », dont la borne haute a 95 % vaut environ 13.0 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-3.66 %** | CVaR **-5.15 %** | vol 2.33 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.57 % contre 2.74 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.65 % vs -6.29 % si l'on extrapolait par √5 _(rapport 0.897 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3066** (β de hausse 0.222, asymétrie 1.3808) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : ₩-3843.639 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 12 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 56.2 | side 38.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.315% → cible +1.715% / stop −8.0%, p_fill 20%, n_eff≈23.0) : P(cible|rempli) **42%** · **EV/risk +0.007** (×p_fill ; si rempli +0.28% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→53% · +2.0%→32% · +3.0%→20% · +5.0%→4% · +8.0%→2%
- Range intraday médian 3.64% (p90 6.02%) · excursion haute méd. +1.04% / basse méd. −1.54%
- Profil de vol intra : ouverture 2.265% vs midi 0.627% vs clôture 0.744% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 15% · trend ↑1%/↓3% ; spike-down 50% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.141 ; mean-reverting — autocorr -0.106)_ ; drift intra méd. -0.235% ; recovery-V 24%
- **σ réalisé intraday** 1.956% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 54% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 1368762.5 (VA 1354937.5–1388512.5 ; dernier close 1354000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 38% · rebond 60% · **stop −2.94%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.47 (high win-rate)
- Gaps overnight (n=152) : méd. 0.07% · baisse 38% (gap-down >1% 16% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −2.0%) · haut méd +0.47% · range méd 1.25%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −2.4%) · haut méd +0.56% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.92% (p90 −2.53%) · haut méd +0.58% · range méd 1.8%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −3.29%) · haut méd +0.74% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1354000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 81% (111/152) · gap 24% · délai 0.4min · rebond 46% (51/111) (MFE +0.9%)
   - −1.0% : fill 30min 48% · séance 63% (89/152) · gap 16% · délai 1.4min · rebond 52% (43/89) (MFE +1.01%)
   - −1.5% : fill 30min 35% · séance 50% (71/152) · gap 8% · délai 3.5min · rebond 52% (33/71) (MFE +1.38%)
   - −2.0% : fill 30min 21% · séance 38% (57/152) · gap 5% · délai 7.6min · rebond 60% (31/57) (MFE +1.39%)
   - −3.0% : fill 30min 9% · séance 20% (34/152) · gap 2% · délai 53.3min · rebond 42% (17/34) (MFE +0.74%)
   - −4.0% : fill 30min 5% · séance 13% (19/152) · gap 2% · délai 67.5min · rebond 47% (9/19) (MFE +0.96%)
   - −5.0% : fill 30min 2% · séance 6% (10/152) · gap 2% · délai 110.1min · rebond 80% (8/10) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.86%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.1%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.87% (p90 −2.09%) → stop au-delà de −1.58% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=402 jambes) : jambe baissière méd −1.07% (p90 −2.66%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 100% (43/44) · rebond 63% (24/43)
      · −2.0% : fill 69% (32/44) · rebond 72% (17/32)
      · −3.0% : fill 26% (18/44) · rebond 44% (9/18)
      · −4.0% : fill 18% (10/44) · rebond 58% (5/10)
      · −5.0% : fill 10% (6/44) · rebond 100% (6/6)
   - **flat** (40 séances) :
      · −1.0% : fill 56% (25/40) · rebond 39% (7/25)
      · −2.0% : fill 32% (13/40) · rebond 36% (6/13)
      · −3.0% : fill 28% (10/40) · rebond 50% (6/10)
      · −4.0% : fill 12% (5/40) · rebond 60% (3/5)
      · −5.0% : fill 5% (2/40) · rebond 55% (1/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 40% (21/68) · rebond 43% (12/21)
      · −2.0% : fill 20% (12/68) · rebond 53% (8/12)
      · −3.0% : fill 11% (6/68) · rebond 25% (2/6)
      · −4.0% : fill 9% (4/68) · rebond 19% (1/4)
      · −5.0% : fill 3% (2/68) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 78% si les 15 1res min sont vertes (54 cas) · 28% si rouges (106 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **24min** → P(séance verte=clôture>ouverture) 80% si début vert vs 22% si rouge (base 46% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 220min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=60) : tient le vert **80%** · continue >prix actuel 52% ; creux résiduel méd -0.95% (q20 -1.91%) → **SL/trailing à −1.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.15% / q75 +2.6% → **scale +1.15% / runner +2.6%**, sortie à la clôture
  - **si ROUGE au coude** (n=100) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.49%** (au-delà de la MAE q10 -3.49%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.02% .. +2.69%] · haut q95 +3.0% · bas q05 -3.49%
   - 60min (n=160) : retour [-3.26% .. +2.21%] · haut q95 +3.43% · bas q05 -3.75%
   - 2h (n=160) : retour [-3.64% .. +3.17%] · haut q95 +3.98% · bas q05 -4.22%
   - 4h (n=160) : retour [-4.18% .. +3.04%] · haut q95 +4.11% · bas q05 -4.76%
   - 6h (n=160) : retour [-4.73% .. +3.16%] · haut q95 +4.53% · bas q05 -5.43%
   - session (n=160) : retour [-4.55% .. +3.12%] · haut q95 +4.53% · bas q05 -5.45%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 1.99%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.28 · part idiosyncratique 0.71
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.2  _(survente)_
- **ADX** : 27.0  _(tendance etablie)_
- **MACD** : hist -13642.466  _(bearish_recent)_
- **BB** : %B -0.22 · largeur 16.4%
- **ATR** : 40428.4 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.235  _(distribution)_
- **Vol ratio** : 1.89  _(volume au-dessus de la moyenne)_
- **Choppiness** : 37.0  _(marche directionnel)_
- **MA** : MA20 1381630.57 · MA50 1469652.23 · MA200 1543288.06  _(prix < MA20)_
- **Dist MA** : MA20 -11.8% · MA50 -17.1% · MA200 -21.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (563802 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
