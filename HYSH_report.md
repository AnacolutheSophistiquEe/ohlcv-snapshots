# 298040

**Generated** : 2026-11-09T01:17:14.211257+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 1/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · ₩1558000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩1558000.00 (+11.5% vs entrée) · entrée ₩1397071.43 · stop ₩1348792.86 · T1 ₩1477535.71 · R/R 1.67  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-09 : 1558000.0 · ATR Wilder 168761.42 (10.83 %)_
- **Swing** : plage **1373463.96 → 1233853.18** (-11.84 % a -20.81 % sous la cloture, 0.83 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 1350211.69-1364151.97 (A) ; 1264578.88-1309386.78 (A). stop INDICATIF 1086599.3 (-11.93 % sous le bas ; sous le support 1170980.01-1187907.55 (- 0,5 ATR)).
- **Deep** : plage **1233853.18 → 973858.55** (-20.81 % a -37.49 % sous la cloture, 1.54 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1170980.01-1187907.55 (A) ; 1068419.78-1138120.94 (A) ; 941961.85-1005688.68 (A). stop INDICATIF 721165.98 (-25.95 % sous le bas ; sous le support 805546.69-864294.8 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 3.85 ATR sous le plus haut 20 s., RSI(2) 8.2. Limite **1473619.29** (seance suivante), stop catastrophe 798573.59, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 1442814.68-1491605.62 (C, -4.26 %) ; 1350211.69-1364151.97 (A, -12.44 %) ; 1264578.88-1309386.78 (A, -15.96 %) ; 1170980.01-1187907.55 (A, -23.75 %) ; 1068419.78-1138120.94 (A, -26.95 %) ; 941961.85-1005688.68 (A, -35.45 %)
- Resistances reelles au-dessus : 1723610.98-1793312.2 (A, 10.63 %) ; 1834000.0-1913000.0 (A, 17.72 %) ; 1991000.0-2071121.22 (A, 27.79 %) ; 2091035.73-2140000.0 (A, 34.21 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.86 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (30.18 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 30.18 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.629 % | p01 -5.158 % | pire -16.75 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4356** [0.3633 ; 0.51] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.2147** [0.1739 ; 0.2603] _(largeur 8.6 pt, n_eff 345.6)_
   - deep : **0.2306** [0.1886 ; 0.2771] _(largeur 8.9 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.69 %** | CVaR **-10.87 %** | vol 5.23 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.73 % contre 6.03 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.51 % vs -12.72 % si l'on extrapolait par √5 _(rapport 0.983 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1564** (β de hausse 0.997, asymétrie 1.1598) vs KS11 — 556 séances de repli, historique complet


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 52.6 | bear 37.2 | side 10.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→62% · +2.0%→50% · +3.0%→32% · +5.0%→18% · +8.0%→5%
- Range intraday médian 5.91% (p90 9.91%) · excursion haute méd. +2.0% / basse méd. −3.47%
- Profil de vol intra : ouverture 4.013% vs midi 1.037% vs clôture 1.07% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 22% · trend ↑0%/↓3% ; spike-down 78% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.147 ; neutre — autocorr -0.004)_ ; drift intra méd. -1.036% ; recovery-V 30%
- **σ réalisé intraday** 3.347% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 56% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 1815075.0 (VA 1805675.0–1845625.0 ; dernier close 1873000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 69% · **stop −4.94%** sous le fill (sous le bruit) · cible +2.26% · R/R 0.46 (high win-rate)
- Gaps overnight (n=152) : méd. 0.17% · baisse 41% (gap-down >1% 26% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.46% (p90 −3.14%) · haut méd +0.42% · range méd 2.26%
- Excursion ouverture 15min (n=160) : bas méd −1.94% (p90 −4.02%) · haut méd +0.65% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −2.08% (p90 −4.21%) · haut méd +0.77% · range méd 3.46%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −5.29%) · haut méd +1.0% · range méd 3.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1877000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 76% (106/152) · gap 34% · délai 0.0min · rebond 50% (57/106) (MFE +0.97%)
   - −1.0% : fill 30min 61% · séance 69% (99/152) · gap 26% · délai 0.0min · rebond 48% (50/99) (MFE +0.91%)
   - −1.5% : fill 30min 53% · séance 62% (89/152) · gap 24% · délai 1.3min · rebond 47% (47/89) (MFE +0.96%)
   - −2.0% : fill 30min 48% · séance 59% (83/152) · gap 20% · délai 3.5min · rebond 46% (41/83) (MFE +0.95%)
   - −3.0% : fill 30min 37% · séance 46% (68/152) · gap 14% · délai 1.4min · rebond 57% (41/68) (MFE +1.17%)
   - −4.0% : fill 30min 27% · séance 41% (60/152) · gap 10% · délai 6.1min · rebond 70% (44/60) (MFE +1.73%)
   - −5.0% : fill 30min 19% · séance 33% (47/152) · gap 6% · délai 22.8min · rebond 69% (34/47) (MFE +2.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.94% (p90 −3.47%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.14% (p90 −2.58%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −3.94%) → stop au-delà de −2.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=844 jambes) : jambe baissière méd −1.36% (p90 −3.29%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 96% (50/51) · rebond 36% (22/50)
      · −2.0% : fill 94% (46/51) · rebond 40% (20/46)
      · −3.0% : fill 86% (44/51) · rebond 55% (26/44)
      · −4.0% : fill 78% (40/51) · rebond 74% (29/40)
      · −5.0% : fill 65% (32/51) · rebond 77% (25/32)
   - **flat** (20 séances) :
      · −1.0% : fill 92% (18/20) · rebond 67% (11/18)
      · −2.0% : fill 61% (14/20) · rebond 38% (6/14)
      · −3.0% : fill 20% (7/20) · rebond 56% (4/7)
      · −4.0% : fill 20% (7/20) · rebond 52% (5/7)
      · −5.0% : fill 16% (4/20) · rebond 40% (2/4)
   - **gap-up** (81 séances) :
      · −1.0% : fill 40% (31/81) · rebond 59% (17/31)
      · −2.0% : fill 31% (23/81) · rebond 68% (15/23)
      · −3.0% : fill 23% (17/81) · rebond 61% (11/17)
      · −4.0% : fill 18% (13/81) · rebond 60% (10/13)
      · −5.0% : fill 12% (11/81) · rebond 48% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 55% si les 15 1res min sont vertes (51 cas) · 32% si rouges (109 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:42** → P(séance verte=clôture>ouverture) 82% si début vert vs 14% si rouge (base 38% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=58) : tient le vert **82%** · continue >prix actuel 52% ; creux résiduel méd -1.27% (q20 -2.31%) → **SL/trailing à −2.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.69% → **scale +1.55% / runner +2.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=102) : edge inversé — récupère vert seulement **14%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.36%** (au-delà de la MAE q10 -4.36%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.07% .. +3.41%] · haut q95 +5.62% · bas q05 -5.13%
   - 60min (n=160) : retour [-5.16% .. +2.93%] · haut q95 +5.86% · bas q05 -5.54%
   - 2h (n=160) : retour [-6.47% .. +3.73%] · haut q95 +5.87% · bas q05 -6.72%
   - 4h (n=160) : retour [-7.71% .. +4.89%] · haut q95 +6.08% · bas q05 -8.56%
   - 6h (n=160) : retour [-8.35% .. +4.92%] · haut q95 +6.23% · bas q05 -9.22%
   - session (n=160) : retour [-8.22% .. +5.23%] · haut q95 +6.23% · bas q05 -9.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.79%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.13 · part idiosyncratique 0.87
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.9  _(momentum baissier)_
- **ADX** : 34.7  _(tendance etablie)_
- **MACD** : hist -6644.655  _(bearish_recent)_
- **BB** : %B -0.07 · largeur 31.7%
- **ATR** : 160928.57 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.103  _(accumulation)_
- **Vol ratio** : 0.17  _(volume atone)_
- **Choppiness** : 47.0  _(transition)_
- **MA** : MA20 1904650.0 · MA50 2451620.0 · MA200 2853205.0  _(prix < MA20)_
- **Dist MA** : MA20 -18.2% · MA50 -36.5% · MA200 -45.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (407401 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
