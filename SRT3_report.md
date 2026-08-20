# SRT3

**Generated** : 2026-08-20T19:46:19.276013+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €248.90  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €248.90 (+2.5% vs entrée) · entrée €242.74 · stop €239.10 · T1 €245.52 · R/R 0.76  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk -0.005 _(réel 5 s)_ (GBM 0.077) · ¼-Kelly 0.038 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 76.2 > 70 (surachat) ; %B 1.08 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €242.19–€243.30 (mid €242.74)
- Spot actuel : €248.90 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : €239.10 (stop swing_plan-based (-8.58%))
- Targets : T1 €245.52 · R/R 0.76 | T2 €248.30 · R/R 1.53 | T3 €251.08 · R/R 2.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €239.10


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.58 %)** : le gap seul le franchit 0.236 % des séances ; quand il le franchit, l'exécution est **2.698 points plus bas** → perte réelle **11.278 %** _(et non 8.58 %)_
- Chocs d'ouverture : p05 -1.616 % | p01 -3.241 % | pire -14.205 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0381** [0.0168 ; 0.0746] _(largeur 5.8 pt, n_eff 173.1)_
   - swing : **0.3555** [0.3064 ; 0.407] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.49** [0.4376 ; 0.5426] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (50.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.18 %** | CVaR **-6.61 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.26 % si l'on extrapolait par √5 _(rapport 1.08 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0659** (β de hausse 1.1628, asymétrie 0.9167) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.352× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : 0.077 | EV/share : €0.281 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 65 % | T2 37 % | T3 19 %
- Kelly (position) : f* 0.151 | ¼-Kelly 0.038 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.5 | bear 81.5 | side 13.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 498.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.477% → cible +1.145% / stop −1.5%, p_fill 20%, n_eff≈12.1) : P(cible|rempli) **41%** · **EV/risk -0.005** (×p_fill ; si rempli -0.04% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→49% · +3.0%→26% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.37% (p90 6.59%) · excursion haute méd. +1.94% / basse méd. −1.45%
- Profil de vol intra : ouverture 2.048% vs midi 0.856% vs clôture 0.975% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.102 ; neutre — autocorr -0.024)_ ; drift intra méd. 0.043% ; recovery-V 28%
- **σ réalisé intraday** 2.528% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 72% / whipsaw 43%
- POC intraday (dernière séance, temps-au-prix) : 227.6337 (VA 226.1463–231.5012 ; dernier close 235.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 58% · rebond 74% · **stop −2.26%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.73 (high win-rate)
- Gaps overnight (n=159) : méd. 0.05% · baisse 49% (gap-down >1% 14% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.5% (p90 −1.84%) · haut méd +0.48% · range méd 1.21%
- Excursion ouverture 15min (n=160) : bas méd −0.59% (p90 −1.94%) · haut méd +0.62% · range méd 1.49%
- Excursion ouverture 30min (n=160) : bas méd −0.64% (p90 −2.1%) · haut méd +0.77% · range méd 1.71%
- Excursion ouverture 60min (n=160) : bas méd −0.75% (p90 −2.54%) · haut méd +0.78% · range méd 1.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 235.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 78% (126/159) · gap 25% · délai 0.3min · rebond 54% (65/126) (MFE +1.18%)
   - −1.0% : fill 30min 44% · séance 66% (106/159) · gap 14% · délai 2.7min · rebond 57% (59/106) (MFE +1.3%)
   - −1.5% : fill 30min 36% · séance 58% (97/159) · gap 6% · délai 4.7min · rebond 74% (63/97) (MFE +1.66%)
   - −2.0% : fill 30min 19% · séance 39% (75/159) · gap 3% · délai 50.4min · rebond 63% (46/75) (MFE +1.67%)
   - −3.0% : fill 30min 6% · séance 16% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 9% (21/159) · gap 0% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 7% (12/159) · gap 0% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.02%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.18% (p90 −2.32%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.66%) → stop au-delà de −1.53% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=440 jambes) : jambe baissière méd −1.04% (p90 −2.39%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 80% (58/70) · rebond 66% (36/58)
      · −2.0% : fill 50% (43/70) · rebond 58% (27/43)
      · −3.0% : fill 27% (28/70) · rebond 48% (15/28)
      · −4.0% : fill 13% (15/70) · rebond 71% (11/15)
      · −5.0% : fill 7% (7/70) · rebond 92% (6/7)
   - **flat** (33 séances) :
      · −1.0% : fill 68% (21/33) · rebond 54% (10/21)
      · −2.0% : fill 47% (16/33) · rebond 62% (8/16)
      · −3.0% : fill 16% (6/33) · rebond 66% (4/6)
      · −4.0% : fill 12% (4/33) · rebond 70% (3/4)
      · −5.0% : fill 12% (4/33) · rebond 24% (2/4)
   - **gap-up** (56 séances) :
      · −1.0% : fill 50% (27/56) · rebond 45% (13/27)
      · −2.0% : fill 23% (16/56) · rebond 77% (11/16)
      · −3.0% : fill 6% (6/56) · rebond 78% (4/6)
      · −4.0% : fill 4% (2/56) · rebond 100% (2/2)
      · −5.0% : fill 3% (1/56) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 56% si les 15 1res min sont vertes (87 cas) · 38% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 57% si début vert vs 38% si rouge (base 48% · écart 20 pts) ; prédictivité sature ensuite (plafond brut 268min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **57%** · continue >prix actuel 46% ; creux résiduel méd -1.42% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +2.35% → **scale +1.33% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **38%** (continue à baisser 53%) → **RÉDUIRE ~62%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.46%** (au-delà de la MAE q10 -4.46%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.91% .. +2.13%] · haut q95 +2.63% · bas q05 -3.32%
   - 60min (n=160) : retour [-2.99% .. +2.35%] · haut q95 +2.85% · bas q05 -3.71%
   - 2h (n=160) : retour [-2.19% .. +2.5%] · haut q95 +2.94% · bas q05 -3.83%
   - 4h (n=160) : retour [-2.54% .. +2.29%] · haut q95 +3.26% · bas q05 -3.83%
   - 6h (n=160) : retour [-2.62% .. +2.95%] · haut q95 +3.65% · bas q05 -4.08%
   - session (n=160) : retour [-3.62% .. +4.15%] · haut q95 +5.62% · bas q05 -4.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 76.2  _(surachat)_
- **ADX** : 13.5  _(pas de tendance nette)_
- **MACD** : hist 1.281  _(pas de croisement recent)_
- **BB** : %B 1.08 · largeur 14.0%
- **ATR** : 7.82 (30.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.002  _(neutre)_
- **Vol ratio** : 1.83  _(volume au-dessus de la moyenne)_
- **Choppiness** : 45.9  _(transition)_
- **MA** : MA20 230.13 · MA50 229.86 · MA200 231.92  _(prix > MA20)_
- **Dist MA** : MA20 +8.2% · MA50 +8.3% · MA200 +7.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (410979 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
