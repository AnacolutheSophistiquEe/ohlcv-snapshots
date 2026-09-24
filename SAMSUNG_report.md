# 005930

**Generated** : 2026-09-24T22:00:52.783717+00:00  
**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩285500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)  
> ↳ spot ₩285500.00 (+11.2% vs entrée) · entrée ₩256714.00 · stop ₩247178.29 · T1 ₩265391.31 · R/R 0.91  
> ↳ P(T1 av. stop) 60 % · EV/risk 0.42 · ¼-Kelly 0.041 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -87 % hors [0,100] (R² max 0.80). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 72.0 > 70 (surachat) ; %B 1.07 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩254978.54–₩258449.46 (mid ₩256714.00)
- Spot actuel : ₩285500.00 (+11.2% au-dessus de la zone — repli à attendre)
- Stop : ₩247178.29 (stop swing_plan-based (-13.42%))
- Targets : T1 ₩265391.31 · R/R 0.91 | T2 ₩274068.61 · R/R 1.82 | T3 ₩282745.92 · R/R 2.73
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩247178.29


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.09 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.42 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1221).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.42 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.481 % | p01 -4.947 % | pire -10.942 % _(sur 1221 séances)_
- **P(stop avant cible)** _(source : daily, 1222 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0319** [0.0129 ; 0.0663] _(largeur 5.3 pt, n_eff 173.1)_
   - swing : **0.3612** [0.3119 ; 0.4128] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.2938** [0.2476 ; 0.3434] _(largeur 9.6 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 11.0 observations effectives », dont la borne haute a 95 % vaut environ 27.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (47.0 pt), swing (51.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.74 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.73 % contre 5.72 % aujourd'hui, rapport 0.48)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.42 % vs -7.3 % si l'on extrapolait par √5 _(rapport 0.88 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1699** (β de hausse 1.3393, asymétrie 0.8735) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.268 | EV/share : ₩2550.712 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 43 % | T3 29 %
- Kelly (position) : f* 0.163 | ¼-Kelly 0.041 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.4 | bear 5.0 | side 61.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.587% → cible +1.512% / stop −8.0%, p_fill 23%, n_eff≈14.9) : P(cible|rempli) **45%** · **EV/risk -0.016** (×p_fill ; si rempli -0.56% du capital)
  - **swing** (entrée dip −10.08% → cible +3.38% / stop −3.715%, p_fill 17%, n_eff≈11.0) : P(cible|rempli) **63%** · **EV/risk +0.042** (×p_fill ; si rempli +0.90% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→46% · +3.0%→36% · +5.0%→22% · +8.0%→4%
- Range intraday médian 6.16% (p90 9.84%) · excursion haute méd. +1.88% / basse méd. −3.0%
- Profil de vol intra : ouverture 3.103% vs midi 1.331% vs clôture 1.544% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓1% ; spike-down 67% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.088)_ ; drift intra méd. -0.38% ; recovery-V 24%
- **σ réalisé intraday** 3.594% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 68% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 254825.0 (VA 254525.0–258725.0 ; dernier close 256000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 51% · **stop −6.12%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.17 (high win-rate)
- Gaps overnight (n=159) : méd. 0.85% · baisse 44% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.64%) · haut méd +0.6% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.35%) · haut méd +0.8% · range méd 2.07%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.13%) · haut méd +1.01% · range méd 2.44%
- Excursion ouverture 60min (n=160) : bas méd −1.56% (p90 −3.58%) · haut méd +1.23% · range méd 3.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 255500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 68% (97/159) · gap 38% · délai 0.0min · rebond 46% (48/97) (MFE +0.92%)
   - −1.0% : fill 30min 46% · séance 60% (88/159) · gap 36% · délai 0.0min · rebond 57% (49/88) (MFE +1.3%)
   - −1.5% : fill 30min 43% · séance 53% (77/159) · gap 29% · délai 0.0min · rebond 60% (45/77) (MFE +1.52%)
   - −2.0% : fill 30min 37% · séance 51% (72/159) · gap 25% · délai 0.0min · rebond 62% (44/72) (MFE +1.83%)
   - −3.0% : fill 30min 30% · séance 44% (62/159) · gap 23% · délai 0.0min · rebond 51% (34/62) (MFE +1.05%)
   - −4.0% : fill 30min 21% · séance 34% (47/159) · gap 10% · délai 5.8min · rebond 50% (27/47) (MFE +1.06%)
   - −5.0% : fill 30min 13% · séance 25% (36/159) · gap 9% · délai 18.2min · rebond 51% (23/36) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.88%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −2.88%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.71%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=772 jambes) : jambe baissière méd −1.21% (p90 −3.02%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 97% (59/62) · rebond 49% (29/59)
      · −2.0% : fill 89% (51/62) · rebond 51% (27/51)
      · −3.0% : fill 84% (48/62) · rebond 46% (25/48)
      · −4.0% : fill 70% (38/62) · rebond 46% (21/38)
      · −5.0% : fill 52% (30/62) · rebond 41% (17/30)
   - **flat** (14 séances) :
      · −1.0% : fill 73% (11/14) · rebond 58% (6/11)
      · −2.0% : fill 48% (7/14) · rebond 81% (5/7)
      · −3.0% : fill 33% (5/14) · rebond 33% (2/5)
      · −4.0% : fill 24% (3/14) · rebond 25% (1/3)
      · −5.0% : fill 24% (3/14) · rebond 100% (3/3)
   - **gap-up** (83 séances) :
      · −1.0% : fill 30% (18/83) · rebond 77% (14/18)
      · −2.0% : fill 22% (14/83) · rebond 88% (12/14)
      · −3.0% : fill 15% (9/83) · rebond 82% (7/9)
      · −4.0% : fill 8% (6/83) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/83) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 60% si les 15 1res min sont vertes (79 cas) · 22% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 72% si début vert vs 9% si rouge (base 40% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 216min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **72%** · continue >prix actuel 62% ; creux résiduel méd -1.3% (q20 -4.5%) → **SL/trailing à −4.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.16% / q75 +4.03% → **scale +2.16% / runner +4.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **9%** (continue à baisser 69%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.34%** (au-delà de la MAE q10 -6.34%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +2.61%] · haut q95 +3.44% · bas q05 -3.68%
   - 60min (n=160) : retour [-3.07% .. +4.19%] · haut q95 +4.93% · bas q05 -4.26%
   - 2h (n=160) : retour [-4.5% .. +4.63%] · haut q95 +5.86% · bas q05 -5.54%
   - 4h (n=160) : retour [-5.86% .. +5.26%] · haut q95 +6.82% · bas q05 -7.38%
   - 6h (n=160) : retour [-6.62% .. +5.26%] · haut q95 +6.92% · bas q05 -7.66%
   - session (n=160) : retour [-6.16% .. +5.39%] · haut q95 +6.92% · bas q05 -8.38%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 72.0  _(surachat)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist 2640.344  _(bullish_recent)_
- **BB** : %B 1.07 · largeur 15.7%
- **ATR** : 9535.71 (45.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.1  _(accumulation)_
- **Vol ratio** : 1.25  _(volume normal)_
- **Choppiness** : 46.1  _(transition)_
- **MA** : MA20 261900.0 · MA50 255380.0 · MA200 222131.75  _(prix > MA20)_
- **Dist MA** : MA20 +9.0% · MA50 +11.8% · MA200 +28.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (591195 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
