# 267260

**Generated** : 2026-09-01T21:53:00.173343+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩769000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩769000.00 (+1.0% vs entrée) · entrée ₩761598.65 · stop ₩700670.75 · T1 ₩778918.41 · R/R 0.28  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk -0.025 _(réel 5 s)_ (GBM -0.183) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩758134.69–₩765062.60 (mid ₩761598.65)
- Spot actuel : ₩769000.00 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : ₩700670.75 (stop swing_plan-based (-8.02%))
- Targets : T1 ₩778918.41 · R/R 0.28 | T2 ₩796238.18 · R/R 0.57 | T3 ₩813557.95 · R/R 0.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩700670.75


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.02 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **3.695 pt plus bas** dans le cas TYPIQUE (médiane), 3.695 au p90, **3.695 au pire**
   - perte réelle **11.715 %** en moyenne _(tirée par la queue)_, jusqu'à **11.715 %** — au lieu des 8.02 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.003 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.638 % | p01 -4.805 % | pire -11.715 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0807** [0.047 ; 0.1283] _(largeur 8.1 pt, n_eff 173.1)_
   - swing : **0.3872** [0.337 ; 0.4393] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.3637** [0.3143 ; 0.4154] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 38.4 observations effectives », dont la borne haute a 95 % vaut environ 7.8 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 34.9 observations effectives », dont la borne haute a 95 % vaut environ 8.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.0 pt), swing (30.3 pt), deep (31.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.59 %** | CVaR **-8.78 %** | vol 4.42 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.84 % contre 4.98 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.73 % vs -11.89 % si l'on extrapolait par √5 _(rapport 0.902 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0381** (β de hausse 0.8321, asymétrie 1.2475) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.183 | EV/share : ₩-11164.215 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 17 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.6 | bear 7.0 | side 7.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.967% → cible +2.274% / stop −8.0%, p_fill 98%, n_eff≈40.1) : P(cible|rempli) **50%** · **EV/risk -0.025** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −2.112% → cible +5.085% / stop −6.035%, p_fill 94%, n_eff≈38.4) : P(cible|rempli) **58%** · **EV/risk -0.008** (×p_fill ; si rempli -0.05% du capital)
  - **deep** (entrée dip −3.268% → cible +7.191% / stop −9.161%, p_fill 83%, n_eff≈34.9) : P(cible|rempli) **46%** · **EV/risk -0.197** (×p_fill ; si rempli -2.16% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→42% · +3.0%→35% · +5.0%→12% · +8.0%→4%
- Range intraday médian 6.79% (p90 10.49%) · excursion haute méd. +1.58% / basse méd. −4.07%
- Profil de vol intra : ouverture 4.497% vs midi 1.221% vs clôture 1.302% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 84% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; mean-reverting — autocorr -0.051)_ ; drift intra méd. -0.875% ; recovery-V 34%
- **σ réalisé intraday** 4.212% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 62% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 770850.0 (VA 770150.0–779250.0 ; dernier close 783000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 76% · **stop −4.72%** sous le fill (sous le bruit) · cible +2.45% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. 0.91% · baisse 36% (gap-down >1% 18% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −1.72% (p90 −3.94%) · haut méd +0.89% · range méd 2.94%
- Excursion ouverture 15min (n=160) : bas méd −2.06% (p90 −4.4%) · haut méd +1.01% · range méd 3.57%
- Excursion ouverture 30min (n=160) : bas méd −2.27% (p90 −4.88%) · haut méd +1.05% · range méd 3.81%
- Excursion ouverture 60min (n=160) : bas méd −2.58% (p90 −5.16%) · haut méd +1.09% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 781000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 74% (109/159) · gap 29% · délai 0.1min · rebond 52% (58/109) (MFE +1.09%)
   - −1.0% : fill 30min 55% · séance 70% (101/159) · gap 18% · délai 0.3min · rebond 60% (61/101) (MFE +1.35%)
   - −1.5% : fill 30min 49% · séance 65% (90/159) · gap 15% · délai 0.6min · rebond 66% (59/90) (MFE +1.37%)
   - −2.0% : fill 30min 40% · séance 58% (80/159) · gap 10% · délai 1.1min · rebond 73% (57/80) (MFE +1.72%)
   - −3.0% : fill 30min 32% · séance 48% (65/159) · gap 7% · délai 3.5min · rebond 77% (50/65) (MFE +2.06%)
   - −4.0% : fill 30min 23% · séance 38% (50/159) · gap 3% · délai 11.5min · rebond 77% (36/50) (MFE +2.1%)
   - −5.0% : fill 30min 16% · séance 29% (40/159) · gap 3% · délai 11.6min · rebond 76% (29/40) (MFE +2.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.92% (p90 −3.7%) → stop au-delà de −2.64% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −3.19%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.43%) → stop au-delà de −3.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=827 jambes) : jambe baissière méd −1.22% (p90 −3.29%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 100% (49/49) · rebond 49% (25/49)
      · −2.0% : fill 96% (43/49) · rebond 70% (28/43)
      · −3.0% : fill 86% (38/49) · rebond 78% (28/38)
      · −4.0% : fill 74% (32/49) · rebond 76% (23/32)
      · −5.0% : fill 58% (26/49) · rebond 81% (20/26)
   - **flat** (18 séances) :
      · −1.0% : fill 96% (17/18) · rebond 74% (12/17)
      · −2.0% : fill 72% (13/18) · rebond 73% (11/13)
      · −3.0% : fill 56% (11/18) · rebond 50% (8/11)
      · −4.0% : fill 50% (8/18) · rebond 62% (4/8)
      · −5.0% : fill 50% (8/18) · rebond 73% (6/8)
   - **gap-up** (92 séances) :
      · −1.0% : fill 47% (35/92) · rebond 68% (24/35)
      · −2.0% : fill 33% (24/92) · rebond 78% (18/24)
      · −3.0% : fill 24% (16/92) · rebond 89% (14/16)
      · −4.0% : fill 13% (10/92) · rebond 92% (9/10)
      · −5.0% : fill 8% (6/92) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 37% en base · 48% si les 15 1res min sont vertes (68 cas) · 32% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:18** → P(séance verte=clôture>ouverture) 72% si début vert vs 17% si rouge (base 37% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **72%** · continue >prix actuel 42% ; creux résiduel méd -1.79% (q20 -3.64%) → **SL/trailing à −3.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +2.66% → **scale +1.57% / runner +2.66%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **17%** (continue à baisser 40%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.88%** (au-delà de la MAE q10 -4.88%), cible rebond +1.59% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.07% .. +2.74%] · haut q95 +4.3% · bas q05 -5.45%
   - 60min (n=160) : retour [-5.62% .. +2.58%] · haut q95 +4.5% · bas q05 -6.01%
   - 2h (n=160) : retour [-6.45% .. +3.64%] · haut q95 +4.86% · bas q05 -7.2%
   - 4h (n=160) : retour [-6.89% .. +3.44%] · haut q95 +5.11% · bas q05 -8.36%
   - 6h (n=160) : retour [-7.16% .. +4.57%] · haut q95 +6.06% · bas q05 -8.97%
   - session (n=160) : retour [-7.36% .. +5.22%] · haut q95 +6.06% · bas q05 -9.43%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 54.9  _(neutre)_
- **ADX** : 15.3  _(pas de tendance nette)_
- **MACD** : hist 9810.269  _(pas de croisement recent)_
- **BB** : %B 0.56 · largeur 16.7%
- **ATR** : 45428.57 (37.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.257  _(accumulation)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 47.6  _(transition)_
- **MA** : MA20 761778.82 · MA50 806496.24 · MA200 920284.56  _(prix > MA20)_
- **Dist MA** : MA20 +0.9% · MA50 -4.6% · MA200 -16.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (501610 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
