# 326030

**Generated** : 2026-11-27T21:59:31.629141+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 9/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩98200.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (25 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩98200.00 (+0.4% vs entrée) · entrée ₩97835.73 · stop ₩90008.87 · T1 ₩100292.87 · R/R 0.31  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 163 % hors [0,100] (R² max 0.03). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : %B 1.13 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-27 : 98200.0 · ATR Wilder 4784.03 (4.87 %)_
- **Swing** : plage **91878.9 → 88879.85** (-6.44 % a -9.49 % sous la cloture, 0.63 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 91000.0-93300.0 (B) ; 88500.0-90500.0 (B). stop INDICATIF 83707.99 (-5.82 % sous le bas ; sous le support 86100.0-88400.0 (- 0,5 ATR)).
- **Deep** : plage **88879.85 → 79478.47** (-9.49 % a -19.06 % sous la cloture, 1.97 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 88500.0-90500.0 (B) ; 86100.0-88400.0 (B) ; 83300.0-85400.0 (B) ; 80600.0-82800.0 (B) ; 78000.0-80000.0 (A). stop INDICATIF 73107.99 (-8.02 % sous le bas ; sous le support 75500.0-77100.0 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.17 ATR sous le plus haut 20 s., RSI(2) 96.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 93700.0-95500.0 (B, -2.75 %) ; 91000.0-93300.0 (B, -4.99 %) ; 88500.0-90500.0 (B, -7.84 %) ; 86100.0-88400.0 (B, -9.98 %) ; 83300.0-85400.0 (B, -13.03 %) ; 80600.0-82800.0 (B, -15.68 %)
- Resistances reelles au-dessus : 101500.0-103700.0 (A, 3.36 %) ; 104100.0-106200.0 (A, 6.01 %) ; 106800.0-108800.0 (A, 8.76 %) ; 109500.0-110800.0 (B, 11.51 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.15 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.65 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 5.65 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.605 % | p01 -3.095 % | pire -5.539 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0037** [0.0002 ; 0.0227] _(largeur 2.2 pt, n_eff 173.1)_
   - swing : **0.378** [0.3281 ; 0.43] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.2681** [0.2235 ; 0.3166] _(largeur 9.3 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.07 %** | CVaR **-6.13 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 1.81 % contre 3.35 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.29 % vs -8.8 % si l'on extrapolait par √5 _(rapport 0.942 ; < 1 = le √5 surestime)_
- **β de baisse : 0.4677** (β de hausse 0.4099, asymétrie 1.1412) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : ₩-162.654 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 59.4 | bear 7.8 | side 32.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 604.0 (= 9 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.37% → cible +2.511% / stop −8.0%, p_fill 90%, n_eff≈96.3) : P(cible|rempli) **29%** · **EV/risk -0.023** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −0.646% → cible +5.631% / stop −5.037%, p_fill 88%, n_eff≈101.8) : P(cible|rempli) **25%** · **EV/risk -0.221** (×p_fill ; si rempli -1.27% du capital)
  - **deep** (entrée dip −0.85% → cible +17.832% / stop −8.916%, p_fill 93%, n_eff≈104.0) : P(cible|rempli) **2%** · **EV/risk -0.366** (×p_fill ; si rempli -3.51% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 68.5  _(momentum haussier)_
- **ADX** : 32.5  _(tendance etablie)_
- **MACD** : hist 589.618  _(bullish_recent)_
- **BB** : %B 1.13 · largeur 21.2%
- **ATR** : 4914.29 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.147  _(accumulation)_
- **Vol ratio** : 2.49  _(volume au-dessus de la moyenne)_
- **Choppiness** : 48.8  _(transition)_
- **MA** : MA20 86695.0 · MA50 79888.0 · MA200 90045.0  _(prix > MA20)_
- **Dist MA** : MA20 +13.3% · MA50 +22.9% · MA200 +9.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (405012 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
