# 298040

**Generated** : 2026-11-13T01:17:03.942953+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · ₩1856000.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (15 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩1856000.00 (+1.3% vs entrée) · entrée ₩1832011.67 · stop ₩1685450.74 · T1 ₩1917297.39 · R/R 0.58  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-13 : 1856000.0 · ATR Wilder 158819.88 (8.56 %)_
- **Swing** : plage **1680790.62 → 1545596.06** (-9.44 % a -16.72 % sous la cloture, 0.85 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 1363404.74 (-11.79 % sous le bas ; sous le support 1442814.68-1491605.62 (- 0,5 ATR)).
- **Deep** : plage **1545596.06 → 1304213.33** (-16.72 % a -29.73 % sous la cloture, 1.52 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1442814.68-1491605.62 (A) ; 1350211.69-1364151.97 (A) ; 1264578.88-1309386.78 (A). stop INDICATIF 1091570.07 (-16.3 % sous le bas ; sous le support 1170980.01-1187907.55 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.79 ATR sous le plus haut 20 s., RSI(2) 85.9 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 1723610.98-1793312.2 (B, -3.38 %) ; 1442814.68-1491605.62 (A, -19.63 %) ; 1350211.69-1364151.97 (A, -26.5 %) ; 1264578.88-1309386.78 (A, -29.45 %) ; 1170980.01-1187907.55 (A, -36.0 %) ; 1068419.78-1138120.94 (A, -38.68 %)
- Resistances reelles au-dessus : 1991000.0-2042245.05 (A, 7.27 %) ; 2071121.22-2140000.0 (A, 11.59 %) ; 2189000.0-2220000.0 (B, 17.94 %) ; 2400000.0-2472400.84 (A, 29.31 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.86 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.03 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1219).
   - exécution **4.72 pt plus bas** dans le cas TYPIQUE (médiane), 4.72 au p90, **4.72 au pire**
   - perte réelle **16.75 %** en moyenne _(tirée par la queue)_, jusqu'à **16.75 %** — au lieu des 12.03 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0039 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.629 % | p01 -5.158 % | pire -16.75 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0842** [0.0496 ; 0.1325] _(largeur 8.3 pt, n_eff 173.1)_
   - swing : **0.3041** [0.2574 ; 0.3541] _(largeur 9.7 pt, n_eff 345.6)_
   - deep : **0.3007** [0.2542 ; 0.3506] _(largeur 9.6 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.69 %** | CVaR **-10.87 %** | vol 5.26 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.61 % contre 6.12 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.51 % vs -12.72 % si l'on extrapolait par √5 _(rapport 0.983 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1589** (β de hausse 1.0167, asymétrie 1.1399) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.057 | EV/share : ₩-8358.829 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 18 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 57.8 | bear 5.9 | side 36.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.293% → cible +4.655% / stop −8.0%, p_fill 81%, n_eff≈86.7) : P(cible|rempli) **13%** · **EV/risk -0.078** (×p_fill ; si rempli -0.76% du capital)
  - **swing** (entrée dip −2.839% → cible +16.321% / stop −9.459%, p_fill 74%, n_eff≈86.0) : P(cible|rempli) **11%** · **EV/risk -0.124** (×p_fill ; si rempli -1.59% du capital)
  - **deep** (entrée dip −4.395% → cible +18.208% / stop −14.419%, p_fill 72%, n_eff≈81.4) : P(cible|rempli) **17%** · **EV/risk -0.229** (×p_fill ; si rempli -4.57% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.14 · part idiosyncratique 0.86
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 50.1  _(neutre)_
- **ADX** : 29.7  _(tendance etablie)_
- **MACD** : hist 26902.712  _(bullish_recent)_
- **BB** : %B 0.48 · largeur 28.3%
- **ATR** : 170571.43 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.199  _(accumulation)_
- **Vol ratio** : 0.15  _(volume atone)_
- **Choppiness** : 49.2  _(transition)_
- **MA** : MA20 1864100.0 · MA50 2356240.0 · MA200 2844015.0  _(prix < MA20)_
- **Dist MA** : MA20 -0.4% · MA50 -21.2% · MA200 -34.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (410867 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
