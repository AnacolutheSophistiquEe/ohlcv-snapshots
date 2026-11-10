# 298040

**Generated** : 2026-11-10T21:55:47.899258+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 7.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · ₩1748000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-1 sess · macro taux)  
> ↳ spot ₩1748000.00 (+10.7% vs entrée) · entrée ₩1578357.14 · stop ₩1495994.51 · T1 ₩1743082.40 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 1748000.0 · ATR Wilder 172252.96 (9.85 %)_
- **Swing** : plage **1558285.49 → 1415612.26** (-10.85 % a -19.02 % sous la cloture, 0.83 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 1178452.4 (-16.75 % sous le bas ; sous le support 1264578.88-1350211.69 (- 0,5 ATR)).
- **Deep** : plage **1415612.26 → 1149696.3** (-19.02 % a -34.23 % sous la cloture, 1.54 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1264578.88-1350211.69 (A) ; 1170980.01-1187907.55 (A). stop INDICATIF 982293.3 (-14.56 % sous le bas ; sous le support 1068419.78-1138120.94 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.66 ATR sous le plus haut 20 s., RSI(2) 66.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 1264578.88-1350211.69 (A, -22.76 %) ; 1170980.01-1187907.55 (A, -32.04 %) ; 1068419.78-1138120.94 (A, -34.89 %) ; 941961.85-1005688.68 (A, -42.47 %) ; 805546.69-864294.8 (A, -50.56 %) ; 612374.78-662161.32 (B, -62.12 %)
- Resistances reelles au-dessus : 1834000.0-1913000.0 (A, 4.92 %) ; 1991000.0-2071121.22 (A, 13.9 %) ; 2091035.73-2140000.0 (A, 19.62 %) ; 2189000.0-2220000.0 (B, 25.23 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.86 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (29.08 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 29.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.629 % | p01 -5.158 % | pire -16.75 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2447** [0.1852 ; 0.3126] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.225** [0.1834 ; 0.2712] _(largeur 8.8 pt, n_eff 345.6)_
   - deep : **0.2351** [0.1927 ; 0.2819] _(largeur 8.9 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.69 %** | CVaR **-10.87 %** | vol 5.29 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.66 % contre 6.14 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.51 % vs -12.72 % si l'on extrapolait par √5 _(rapport 0.983 ; < 1 = le √5 surestime)_
- **β de baisse : 1.157** (β de hausse 0.997, asymétrie 1.1605) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 50.7 | bear 7.6 | side 41.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=4))
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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.1 · part idiosyncratique 0.9
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.4  _(momentum baissier)_
- **ADX** : 33.8  _(tendance etablie)_
- **MACD** : hist -171.534  _(bearish_recent)_
- **BB** : %B 0.26 · largeur 30.6%
- **ATR** : 169642.86 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.094  _(accumulation)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 49.0  _(transition)_
- **MA** : MA20 1884000.0 · MA50 2430460.0 · MA200 2851275.0  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -28.1% · MA200 -38.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (404869 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
