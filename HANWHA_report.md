# 012450

**Generated** : 2026-09-02T00:19:14.713676+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1058000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1058000.00 (+2.7% vs entrée) · entrée ₩1029859.60 · stop ₩947470.83 · T1 ₩1053376.68 · R/R 0.29  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk -0.009 _(réel 5 s)_ (GBM -0.119) · ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1025156.18–₩1034563.01 (mid ₩1029859.60)
- Spot actuel : ₩1058000.00 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : ₩947470.83 (stop swing_plan-based (-12.28%))
- Targets : T1 ₩1053376.68 · R/R 0.29 | T2 ₩1076893.76 · R/R 0.57 | T3 ₩1100410.84 · R/R 0.86
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩947470.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.28 %)** : le gap seul le franchit 0.164 % des séances (2 fois sur 1217).
   - exécution **0.908 pt plus bas** dans le cas TYPIQUE (médiane), 0.933 au p90, **0.939 au pire**
   - perte réelle **13.188 %** en moyenne _(tirée par la queue)_, jusqu'à **13.219 %** — au lieu des 12.28 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0015 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.828 % | pire -13.219 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.072** [0.0404 ; 0.1177] _(largeur 7.7 pt, n_eff 173.1)_
   - swing : **0.3752** [0.3254 ; 0.4271] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.329** [0.281 ; 0.3798] _(largeur 9.9 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (39.6 pt), swing (42.6 pt), deep (44.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.4 %** | CVaR **-7.32 %** | vol 3.74 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 2.49 % contre 4.06 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.3 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.858 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5205** (β de hausse 0.3009, asymétrie 1.73) vs KS11 — 553 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.308× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.119 | EV/share : ₩-9821.923 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 20 % | T3 19 %
- Kelly (position) : f* 0.101 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 38.4 | bear 56.6 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.663% → cible +2.284% / stop −8.0%, p_fill 50%, n_eff≈22.0) : P(cible|rempli) **50%** · **EV/risk -0.009** (×p_fill ; si rempli -0.14% du capital)
  - **swing** (entrée dip −5.853% → cible +5.106% / stop −6.827%, p_fill 39%, n_eff≈17.7) : P(cible|rempli) **61%** · **EV/risk +0.043** (×p_fill ; si rempli +0.75% du capital)
  - **deep** (entrée dip −9.039% → cible +7.221% / stop −10.599%, p_fill 26%, n_eff≈17.1) : P(cible|rempli) **48%** · **EV/risk -0.052** (×p_fill ; si rempli -2.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→68% · +2.0%→45% · +3.0%→34% · +5.0%→19% · +8.0%→4%
- Range intraday médian 6.4% (p90 9.56%) · excursion haute méd. +1.91% / basse méd. −3.01%
- Profil de vol intra : ouverture 4.524% vs midi 1.243% vs clôture 1.331% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.065)_ ; drift intra méd. -0.511% ; recovery-V 34%
- **σ réalisé intraday** 4.193% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 51% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 1115437.5 (VA 1092937.5–1134187.5 ; dernier close 1100000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 34% · rebond 78% · **stop −4.47%** sous le fill (sous le bruit) · cible +2.11% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.45% · baisse 34% (gap-down >1% 18% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −1.53% (p90 −4.05%) · haut méd +0.98% · range méd 2.9%
- Excursion ouverture 15min (n=160) : bas méd −1.89% (p90 −4.94%) · haut méd +1.09% · range méd 3.63%
- Excursion ouverture 30min (n=160) : bas méd −2.09% (p90 −5.32%) · haut méd +1.15% · range méd 4.06%
- Excursion ouverture 60min (n=160) : bas méd −2.17% (p90 −5.58%) · haut méd +1.39% · range méd 4.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1102000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 74% (119/159) · gap 25% · délai 0.0min · rebond 60% (65/119) (MFE +1.35%)
   - −1.0% : fill 30min 59% · séance 68% (108/159) · gap 18% · délai 0.2min · rebond 62% (60/108) (MFE +1.62%)
   - −1.5% : fill 30min 50% · séance 58% (96/159) · gap 13% · délai 0.7min · rebond 58% (52/96) (MFE +1.31%)
   - −2.0% : fill 30min 42% · séance 53% (86/159) · gap 6% · délai 1.8min · rebond 64% (52/86) (MFE +1.47%)
   - −3.0% : fill 30min 33% · séance 45% (65/159) · gap 3% · délai 6.3min · rebond 69% (42/65) (MFE +1.58%)
   - −4.0% : fill 30min 18% · séance 34% (50/159) · gap 1% · délai 16.1min · rebond 78% (38/50) (MFE +2.11%)
   - −5.0% : fill 30min 13% · séance 23% (36/159) · gap 1% · délai 8.9min · rebond 77% (30/36) (MFE +1.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.28%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.69%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.74%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=787 jambes) : jambe baissière méd −1.19% (p90 −3.21%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 100% (44/44) · rebond 53% (19/44)
      · −2.0% : fill 86% (39/44) · rebond 55% (21/39)
      · −3.0% : fill 82% (36/44) · rebond 72% (24/36)
      · −4.0% : fill 61% (28/44) · rebond 77% (20/28)
      · −5.0% : fill 44% (22/44) · rebond 82% (19/22)
   - **flat** (26 séances) :
      · −1.0% : fill 72% (22/26) · rebond 80% (15/22)
      · −2.0% : fill 61% (19/26) · rebond 77% (12/19)
      · −3.0% : fill 40% (10/26) · rebond 47% (5/10)
      · −4.0% : fill 39% (9/26) · rebond 84% (7/9)
      · −5.0% : fill 23% (5/26) · rebond 32% (2/5)
   - **gap-up** (89 séances) :
      · −1.0% : fill 48% (42/89) · rebond 64% (26/42)
      · −2.0% : fill 32% (28/89) · rebond 67% (19/28)
      · −3.0% : fill 26% (19/89) · rebond 78% (13/19)
      · −4.0% : fill 17% (13/89) · rebond 74% (11/13)
      · −5.0% : fill 11% (9/89) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 69% si les 15 1res min sont vertes (55 cas) · 22% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 82% si début vert vs 15% si rouge (base 41% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=55) : tient le vert **82%** · continue >prix actuel 50% ; creux résiduel méd -1.8% (q20 -3.0%) → **SL/trailing à −3.0%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.28% / q75 +3.88% → **scale +2.28% / runner +3.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=105) : edge inversé — récupère vert seulement **15%** (continue à baisser 52%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.67%** (au-delà de la MAE q10 -5.67%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.42% .. +3.71%] · haut q95 +5.26% · bas q05 -6.31%
   - 60min (n=160) : retour [-5.18% .. +4.51%] · haut q95 +6.41% · bas q05 -6.98%
   - 2h (n=160) : retour [-6.68% .. +5.06%] · haut q95 +7.07% · bas q05 -8.39%
   - 4h (n=160) : retour [-7.34% .. +5.78%] · haut q95 +7.84% · bas q05 -8.85%
   - 6h (n=160) : retour [-6.8% .. +5.85%] · haut q95 +8.14% · bas q05 -8.99%
   - session (n=160) : retour [-6.85% .. +5.78%] · haut q95 +8.14% · bas q05 -8.99%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 45.6  _(neutre)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist -6879.845  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 19.2%
- **ATR** : 68000.0 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.043  _(neutre)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 58.2  _(transition)_
- **MA** : MA20 1112450.0 · MA50 1036540.0 · MA200 1151514.49  _(prix < MA20)_
- **Dist MA** : MA20 -4.9% · MA50 +2.1% · MA200 -8.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (501035 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
