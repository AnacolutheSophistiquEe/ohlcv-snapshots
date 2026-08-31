# 012450

**Generated** : 2026-08-31T00:19:40.114594+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1157000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1157000.00 (+4.8% vs entrée) · entrée ₩1104109.60 · stop ₩1015780.83 · T1 ₩1169517.86 · R/R 0.74  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.029 _(réel 5 s)_ (GBM -0.106) · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 149 % hors [0,100] (R² max 0.60). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1099357.02–₩1108862.18 (mid ₩1104109.60)
- Spot actuel : ₩1157000.00 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : ₩1015780.83 (stop swing_plan-based (-16.1%))
- Targets : T1 ₩1169517.86 · R/R 0.74 | T2 ₩1172350.07 · R/R 0.77 | T3 ₩1175182.29 · R/R 0.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1015780.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (16.1 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 16.1 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.828 % | pire -13.219 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.075** [0.0427 ; 0.1214] _(largeur 7.9 pt, n_eff 173.1)_
   - swing : **0.386** [0.3358 ; 0.4381] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.3047** [0.258 ; 0.3547] _(largeur 9.7 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first, p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.8 observations effectives », dont la borne haute a 95 % vaut environ 20.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (15.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 840 séances)** : VaR **-5.51 %** | CVaR **-7.45 %** | vol 3.83 %/j
   - _fenêtre arrêtée : rupture de regime a 900 seances en arriere (volatilite 2.55 % contre 4.08 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.3 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.858 ; < 1 = le √5 surestime)_
- **β de baisse : 0.521** (β de hausse 0.2991, asymétrie 1.7417) vs KS11 — 554 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.308× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.106 | EV/share : ₩-9362.849 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 19 % | T3 19 %
- Kelly (position) : f* 0.073 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 40.9 | bear 54.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.576% → cible +5.924% / stop −8.0%, p_fill 27%, n_eff≈14.8) : P(cible|rempli) **0%** · **EV/risk -0.029** (×p_fill ; si rempli -0.88% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→66% · +2.0%→45% · +3.0%→34% · +5.0%→19% · +8.0%→4%
- Range intraday médian 6.39% (p90 9.56%) · excursion haute méd. +1.91% / basse méd. −3.01%
- Profil de vol intra : ouverture 4.549% vs midi 1.24% vs clôture 1.312% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.063)_ ; drift intra méd. -0.299% ; recovery-V 36%
- **σ réalisé intraday** 4.24% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 48% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 1124812.5 (VA 1119187.5–1131562.5 ; dernier close 1157000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 33% · rebond 77% · **stop −4.96%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.48% · baisse 34% (gap-down >1% 18% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −1.51% (p90 −4.05%) · haut méd +0.97% · range méd 2.91%
- Excursion ouverture 15min (n=160) : bas méd −1.93% (p90 −4.96%) · haut méd +1.12% · range méd 3.64%
- Excursion ouverture 30min (n=160) : bas méd −2.13% (p90 −5.35%) · haut méd +1.27% · range méd 4.09%
- Excursion ouverture 60min (n=160) : bas méd −2.19% (p90 −5.65%) · haut méd +1.42% · range méd 4.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1157000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 73% (119/159) · gap 25% · délai 0.0min · rebond 59% (65/119) (MFE +1.29%)
   - −1.0% : fill 30min 58% · séance 67% (107/159) · gap 18% · délai 0.1min · rebond 61% (59/107) (MFE +1.6%)
   - −1.5% : fill 30min 48% · séance 57% (95/159) · gap 13% · délai 0.5min · rebond 57% (51/95) (MFE +1.25%)
   - −2.0% : fill 30min 43% · séance 52% (85/159) · gap 7% · délai 1.8min · rebond 62% (51/85) (MFE +1.35%)
   - −3.0% : fill 30min 34% · séance 44% (64/159) · gap 3% · délai 5.1min · rebond 72% (42/64) (MFE +1.62%)
   - −4.0% : fill 30min 18% · séance 33% (49/159) · gap 1% · délai 9.7min · rebond 77% (37/49) (MFE +2.19%)
   - −5.0% : fill 30min 13% · séance 22% (35/159) · gap 1% · délai 8.6min · rebond 84% (30/35) (MFE +1.88%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −2.29%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.69%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.74%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=784 jambes) : jambe baissière méd −1.19% (p90 −3.2%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 100% (44/44) · rebond 53% (19/44)
      · −2.0% : fill 86% (39/44) · rebond 55% (21/39)
      · −3.0% : fill 82% (36/44) · rebond 72% (24/36)
      · −4.0% : fill 61% (28/44) · rebond 77% (20/28)
      · −5.0% : fill 44% (22/44) · rebond 82% (19/22)
   - **flat** (25 séances) :
      · −1.0% : fill 69% (21/25) · rebond 77% (14/21)
      · −2.0% : fill 57% (18/25) · rebond 72% (11/18)
      · −3.0% : fill 34% (9/25) · rebond 62% (5/9)
      · −4.0% : fill 32% (8/25) · rebond 79% (6/8)
      · −5.0% : fill 15% (4/25) · rebond 55% (2/4)
   - **gap-up** (90 séances) :
      · −1.0% : fill 48% (42/90) · rebond 64% (26/42)
      · −2.0% : fill 32% (28/90) · rebond 67% (19/28)
      · −3.0% : fill 26% (19/90) · rebond 78% (13/19)
      · −4.0% : fill 17% (13/90) · rebond 74% (11/13)
      · −5.0% : fill 11% (9/90) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 69% si les 15 1res min sont vertes (55 cas) · 23% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 80% si début vert vs 14% si rouge (base 42% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=56) : tient le vert **80%** · continue >prix actuel 50% ; creux résiduel méd -1.62% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.83% / q75 +3.75% → **scale +1.83% / runner +3.75%**, sortie à la clôture
  - **si ROUGE au coude** (n=104) : edge inversé — récupère vert seulement **14%** (continue à baisser 44%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.67%** (au-delà de la MAE q10 -5.67%), cible rebond +2.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.46% .. +3.71%] · haut q95 +5.3% · bas q05 -6.31%
   - 60min (n=160) : retour [-5.19% .. +4.54%] · haut q95 +6.5% · bas q05 -7.02%
   - 2h (n=160) : retour [-6.69% .. +5.14%] · haut q95 +7.09% · bas q05 -8.39%
   - 4h (n=160) : retour [-7.34% .. +5.79%] · haut q95 +7.84% · bas q05 -8.86%
   - 6h (n=160) : retour [-6.8% .. +5.9%] · haut q95 +8.2% · bas q05 -9.01%
   - session (n=160) : retour [-6.86% .. +5.83%] · haut q95 +8.2% · bas q05 -9.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 56.4  _(momentum haussier)_
- **ADX** : 15.7  _(pas de tendance nette)_
- **MACD** : hist 1556.059  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 29.2%
- **ATR** : 69928.57 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.112  _(accumulation)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 60.2  _(transition)_
- **MA** : MA20 1096250.0 · MA50 1039560.0 · MA200 1150237.25  _(prix > MA20)_
- **Dist MA** : MA20 +5.5% · MA50 +11.3% · MA200 +0.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (617571 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
