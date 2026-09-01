# 012450

**Generated** : 2026-09-01T00:19:41.478390+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1102000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1102000.00 (+3.7% vs entrée) · entrée ₩1062859.60 · stop ₩977830.83 · T1 ₩1086247.92 · R/R 0.28  
> ↳ P(T1 av. stop) 55 % _(réel 5 s)_ · EV/risk -0.003 _(réel 5 s)_ (GBM -0.115) · ¼-Kelly 0.026 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1058181.93–₩1067537.26 (mid ₩1062859.60)
- Spot actuel : ₩1102000.00 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : ₩977830.83 (stop swing_plan-based (-14.13%))
- Targets : T1 ₩1086247.92 · R/R 0.28 | T2 ₩1109636.25 · R/R 0.55 | T3 ₩1133024.57 · R/R 0.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩977830.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (14.13 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.13 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.828 % | pire -13.219 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0714** [0.04 ; 0.117] _(largeur 7.7 pt, n_eff 173.1)_
   - swing : **0.3769** [0.327 ; 0.4288] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.3029** [0.2562 ; 0.3528] _(largeur 9.7 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (45.2 pt), swing (49.0 pt), deep (49.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.4 %** | CVaR **-7.32 %** | vol 3.74 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 2.48 % contre 4.05 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.3 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.858 ; < 1 = le √5 surestime)_
- **β de baisse : 0.521** (β de hausse 0.298, asymétrie 1.7484) vs KS11 — 554 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.308× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.115 | EV/share : ₩-9784.633 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 21 % | T3 19 %
- Kelly (position) : f* 0.105 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 38.0 | bear 57.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.554% → cible +2.201% / stop −8.0%, p_fill 36%, n_eff≈16.2) : P(cible|rempli) **55%** · **EV/risk -0.003** (×p_fill ; si rempli -0.07% du capital)
  - **swing** (entrée dip −7.81% → cible +4.92% / stop −6.855%, p_fill 30%, n_eff≈12.7) : P(cible|rempli) **61%** · **EV/risk +0.050** (×p_fill ; si rempli +1.15% du capital)
  - **deep** (entrée dip −12.081% → cible +6.959% / stop −10.781%, p_fill 18%, n_eff≈12.4) : P(cible|rempli) **63%** · **EV/risk +0.013** (×p_fill ; si rempli +0.76% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist -1780.785  _(bearish_recent)_
- **BB** : %B 0.49 · largeur 24.6%
- **ATR** : 69642.86 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.074  _(accumulation)_
- **Vol ratio** : 0.44  _(volume atone)_
- **Choppiness** : 60.0  _(transition)_
- **MA** : MA20 1105500.0 · MA50 1037820.0 · MA200 1151035.47  _(prix < MA20)_
- **Dist MA** : MA20 -0.3% · MA50 +6.2% · MA200 -4.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (505964 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
