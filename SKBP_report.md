# 326030

**Generated** : 2026-11-27T01:21:40.042200+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩96900.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 8/125 fenêtres (p_fill pondéré 5 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot ₩96900.00 (+5.1% vs entrée) · entrée ₩92194.44 · stop ₩89573.59 · T1 ₩97436.14 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 155 % hors [0,100] (R² max 0.03). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : %B 1.08 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-27 : 96900.0 · ATR Wilder 4641.17 (4.79 %)_
- **Swing** : plage **90767.66 → 87858.16** (-6.33 % a -9.33 % sous la cloture, 0.63 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 88500.0-90500.0 (B) ; 86100.0-88400.0 (B). stop INDICATIF 80979.42 (-7.83 % sous le bas ; sous le support 83300.0-85400.0 (- 0,5 ATR)).
- **Deep** : plage **87858.16 → 78737.52** (-9.33 % a -18.74 % sous la cloture, 1.97 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 86100.0-88400.0 (B) ; 83300.0-85400.0 (B) ; 80600.0-82800.0 (B) ; 78000.0-80000.0 (A). stop INDICATIF 73179.42 (-7.06 % sous le bas ; sous le support 75500.0-77100.0 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.02 ATR sous le plus haut 20 s., RSI(2) 95.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 93700.0-95500.0 (B, -1.44 %) ; 91000.0-93300.0 (B, -3.72 %) ; 88500.0-90500.0 (B, -6.6 %) ; 86100.0-88400.0 (B, -8.77 %) ; 83300.0-85400.0 (B, -11.87 %) ; 80600.0-82800.0 (B, -14.55 %)
- Resistances reelles au-dessus : 98900.0-101050.0 (A, 2.06 %) ; 101500.0-103700.0 (A, 4.75 %) ; 104100.0-106200.0 (A, 7.43 %) ; 106800.0-108800.0 (A, 10.22 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.15 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (16.3 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 16.3 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.605 % | p01 -3.095 % | pire -5.539 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.23** [0.1721 ; 0.2968] _(largeur 12.5 pt, n_eff 173.1)_
   - swing : **0.275** [0.2299 ; 0.3238] _(largeur 9.4 pt, n_eff 345.6)_
   - deep : **0.273** [0.2281 ; 0.3217] _(largeur 9.4 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.07 %** | CVaR **-6.13 %** | vol 2.94 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 1.81 % contre 3.32 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.29 % vs -8.8 % si l'on extrapolait par √5 _(rapport 0.942 ; < 1 = le √5 surestime)_
- **β de baisse : 0.4677** (β de hausse 0.4061, asymétrie 1.1518) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 59.2 | bear 7.9 | side 32.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 591.0 (= 9 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→42% · +3.0%→27% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.08% (p90 7.08%) · excursion haute méd. +1.51% / basse méd. −2.09%
- Profil de vol intra : ouverture 2.677% vs midi 0.822% vs clôture 0.886% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓0% ; spike-down 60% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.111)_ ; drift intra méd. 0.077% ; recovery-V 24%
- **σ réalisé intraday** 2.491% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 60% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 76828.75 (VA 75598.75–77341.25 ; dernier close 76500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 30% · rebond 59% · **stop −2.56%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.5 (high win-rate)
- Gaps overnight (n=152) : méd. -0.1% · baisse 50% (gap-down >1% 21% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −2.18%) · haut méd +0.47% · range méd 1.52%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.59%) · haut méd +0.57% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −2.64%) · haut méd +0.78% · range méd 2.35%
- Excursion ouverture 60min (n=160) : bas méd −1.21% (p90 −2.88%) · haut méd +0.9% · range méd 2.77%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 76900.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 81% (118/152) · gap 34% · délai 0.0min · rebond 46% (50/118) (MFE +0.85%)
   - −1.0% : fill 30min 52% · séance 73% (107/152) · gap 21% · délai 0.5min · rebond 49% (49/107) (MFE +0.9%)
   - −1.5% : fill 30min 40% · séance 61% (88/152) · gap 8% · délai 5.2min · rebond 59% (50/88) (MFE +1.25%)
   - −2.0% : fill 30min 31% · séance 47% (70/152) · gap 4% · délai 5.3min · rebond 54% (39/70) (MFE +1.2%)
   - −3.0% : fill 30min 15% · séance 30% (46/152) · gap 3% · délai 24.9min · rebond 59% (25/46) (MFE +1.28%)
   - −4.0% : fill 30min 7% · séance 14% (29/152) · gap 2% · délai 49.8min · rebond 70% (19/29) (MFE +1.28%)
   - −5.0% : fill 30min 3% · séance 8% (17/152) · gap 1% · délai 74.1min · rebond 83% (11/17) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.45%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −1.55%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.6% (p90 −1.38%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=593 jambes) : jambe baissière méd −1.0% (p90 −2.27%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 94% (52/55) · rebond 58% (28/52)
      · −2.0% : fill 72% (41/55) · rebond 65% (25/41)
      · −3.0% : fill 54% (30/55) · rebond 63% (18/30)
      · −4.0% : fill 25% (19/55) · rebond 64% (12/19)
      · −5.0% : fill 13% (11/55) · rebond 84% (7/11)
   - **flat** (40 séances) :
      · −1.0% : fill 75% (30/40) · rebond 38% (10/30)
      · −2.0% : fill 45% (18/40) · rebond 36% (9/18)
      · −3.0% : fill 23% (11/40) · rebond 38% (3/11)
      · −4.0% : fill 16% (9/40) · rebond 81% (6/9)
      · −5.0% : fill 9% (6/40) · rebond 80% (4/6)
   - **gap-up** (57 séances) :
      · −1.0% : fill 46% (25/57) · rebond 42% (11/25)
      · −2.0% : fill 19% (11/57) · rebond 39% (5/11)
      · −3.0% : fill 7% (5/57) · rebond 87% (4/5)
      · −4.0% : fill 1% (1/57) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/57) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 59% si les 15 1res min sont vertes (60 cas) · 24% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **33min** → P(séance verte=clôture>ouverture) 76% si début vert vs 19% si rouge (base 38% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 192min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=57) : tient le vert **76%** · continue >prix actuel 58% ; creux résiduel méd -1.06% (q20 -2.78%) → **SL/trailing à −2.78%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.93% / q75 +2.93% → **scale +1.93% / runner +2.93%**, sortie à la clôture
  - **si ROUGE au coude** (n=103) : edge inversé — récupère vert seulement **19%** (continue à baisser 54%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.66%** (au-delà de la MAE q10 -2.66%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.47% .. +2.44%] · haut q95 +3.55% · bas q05 -3.16%
   - 60min (n=160) : retour [-2.72% .. +3.69%] · haut q95 +4.38% · bas q05 -3.43%
   - 2h (n=160) : retour [-3.05% .. +3.6%] · haut q95 +4.6% · bas q05 -3.62%
   - 4h (n=160) : retour [-3.04% .. +5.01%] · haut q95 +6.24% · bas q05 -4.28%
   - 6h (n=160) : retour [-3.56% .. +4.33%] · haut q95 +6.97% · bas q05 -4.59%
   - session (n=160) : retour [-3.57% .. +4.79%] · haut q95 +6.97% · bas q05 -4.63%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **volatil sans tendance propre (choppy)** (vol intra méd 2.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.27 · part idiosyncratique 0.73
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 67.1  _(momentum haussier)_
- **ADX** : 32.2  _(tendance etablie)_
- **MACD** : hist 506.655  _(bullish_recent)_
- **BB** : %B 1.08 · largeur 20.4%
- **ATR** : 4771.43 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.087  _(accumulation)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 51.9  _(transition)_
- **MA** : MA20 86630.0 · MA50 79862.0 · MA200 90038.5  _(prix > MA20)_
- **Dist MA** : MA20 +11.9% · MA50 +21.3% · MA200 +7.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (398085 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
