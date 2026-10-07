# 005930

**Generated** : 2026-10-07T21:56:43.526031+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩268500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot ₩268500.00 (+6.8% vs entrée) · entrée ₩251339.47 · stop ₩241839.47 · T1 ₩261960.79 · R/R 1.12  
> ↳ ¼-Kelly 0.052 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩249575.28–₩253103.66 (mid ₩251339.47)
- Spot actuel : ₩268500.00 (+6.8% au-dessus de la zone — repli à attendre)
- Stop : ₩241839.47 (plancher anti-bruit (R/R<2) ; -3.78 % depuis l'entree)
- Targets : T1 ₩261960.79 · R/R 1.12 | T2 ₩272582.12 · R/R 2.24 | T3 ₩283203.44 · R/R 3.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩241839.47


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.93 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1219).
   - exécution **1.012 pt plus bas** dans le cas TYPIQUE (médiane), 1.012 au p90, **1.012 au pire**
   - perte réelle **10.942 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 9.93 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0008 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.482 % | p01 -4.95 % | pire -10.942 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4585** [0.3855 ; 0.5329] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3691** [0.3195 ; 0.4209] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3235** [0.2758 ; 0.3741] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (28.3 pt), swing (33.0 pt), deep (33.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.75 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.87 % contre 5.54 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.38 % vs -7.35 % si l'on extrapolait par √5 _(rapport 0.869 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1741** (β de hausse 1.3398, asymétrie 0.8763) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.288 | EV/share : ₩2738.189 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 36 % | T3 20 %
- Kelly (position) : f* 0.209 | ¼-Kelly 0.052 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 29.4 | bear 5.0 | side 65.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 535.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.904% → cible +1.822% / stop −1.5%, p_fill 38%, n_eff≈45.3) : P(cible|rempli) **38%** · **EV/risk -0.030** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −6.392% → cible +4.226% / stop −3.78%, p_fill 28%, n_eff≈32.4) : P(cible|rempli) **41%** · **EV/risk -0.025** (×p_fill ; si rempli -0.34% du capital)
  - **deep** (entrée dip −9.879% → cible +14.45% / stop −7.225%, p_fill 27%, n_eff≈29.8) : P(cible|rempli) **26%** · **EV/risk -0.032** (×p_fill ; si rempli -0.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→67% · +2.0%→43% · +3.0%→30% · +5.0%→18% · +8.0%→3%
- Range intraday médian 4.91% (p90 9.02%) · excursion haute méd. +1.77% / basse méd. −2.09%
- Profil de vol intra : ouverture 2.584% vs midi 1.124% vs clôture 1.267% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓1% ; spike-down 56% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.092)_ ; drift intra méd. -0.045% ; recovery-V 21%
- **σ réalisé intraday** 2.631% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 69% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 275968.75 (VA 275281.25–276931.25 ; dernier close 275300.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 48% · **stop −6.29%** sous le fill (sous le bruit) · cible +0.82% · R/R 0.13 (high win-rate)
- Gaps overnight (n=152) : méd. 0.32% · baisse 45% (gap-down >1% 31% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.43%) · haut méd +0.58% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.18%) · haut méd +0.73% · range méd 1.82%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.73%) · haut méd +0.92% · range méd 2.19%
- Excursion ouverture 60min (n=160) : bas méd −1.17% (p90 −3.4%) · haut méd +1.17% · range méd 2.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 276000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 65% (91/152) · gap 36% · délai 0.0min · rebond 47% (43/91) (MFE +0.92%)
   - −1.0% : fill 30min 43% · séance 56% (82/152) · gap 31% · délai 0.0min · rebond 58% (44/82) (MFE +1.3%)
   - −1.5% : fill 30min 36% · séance 46% (70/152) · gap 24% · délai 0.0min · rebond 57% (38/70) (MFE +1.5%)
   - −2.0% : fill 30min 29% · séance 40% (64/152) · gap 21% · délai 0.0min · rebond 56% (36/64) (MFE +1.24%)
   - −3.0% : fill 30min 24% · séance 34% (56/152) · gap 20% · délai 0.0min · rebond 47% (30/56) (MFE +0.92%)
   - −4.0% : fill 30min 18% · séance 28% (44/152) · gap 9% · délai 3.7min · rebond 54% (26/44) (MFE +1.19%)
   - −5.0% : fill 30min 9% · séance 18% (31/152) · gap 6% · délai 40.6min · rebond 48% (19/31) (MFE +0.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.76%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.45% (p90 −2.45%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.4%) → stop au-delà de −1.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=740 jambes) : jambe baissière méd −1.18% (p90 −2.82%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 98% (54/56) · rebond 52% (25/54)
      · −2.0% : fill 73% (45/56) · rebond 42% (21/45)
      · −3.0% : fill 70% (44/56) · rebond 44% (23/44)
      · −4.0% : fill 61% (36/56) · rebond 52% (21/36)
      · −5.0% : fill 39% (26/56) · rebond 38% (14/26)
   - **flat** (15 séances) :
      · −1.0% : fill 57% (11/15) · rebond 64% (6/11)
      · −2.0% : fill 41% (7/15) · rebond 85% (5/7)
      · −3.0% : fill 18% (4/15) · rebond 18% (1/4)
      · −4.0% : fill 12% (2/15) · rebond 0% (0/2)
      · −5.0% : fill 12% (2/15) · rebond 100% (2/2)
   - **gap-up** (81 séances) :
      · −1.0% : fill 25% (17/81) · rebond 72% (13/17)
      · −2.0% : fill 16% (12/81) · rebond 86% (10/12)
      · −3.0% : fill 10% (8/81) · rebond 78% (6/8)
      · −4.0% : fill 7% (6/81) · rebond 93% (5/6)
      · −5.0% : fill 3% (3/81) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 64% si les 15 1res min sont vertes (78 cas) · 22% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:17** → P(séance verte=clôture>ouverture) 81% si début vert vs 11% si rouge (base 43% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **81%** · continue >prix actuel 60% ; creux résiduel méd -1.13% (q20 -2.54%) → **SL/trailing à −2.54%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +3.01% → **scale +1.5% / runner +3.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **11%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.84%** (au-delà de la MAE q10 -5.84%), cible rebond +0.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +2.46%] · haut q95 +3.12% · bas q05 -3.57%
   - 60min (n=160) : retour [-2.81% .. +3.45%] · haut q95 +4.39% · bas q05 -3.67%
   - 2h (n=160) : retour [-4.15% .. +4.5%] · haut q95 +5.64% · bas q05 -5.14%
   - 4h (n=160) : retour [-5.6% .. +5.04%] · haut q95 +6.29% · bas q05 -7.01%
   - 6h (n=160) : retour [-5.93% .. +4.97%] · haut q95 +6.76% · bas q05 -7.24%
   - session (n=160) : retour [-5.53% .. +5.29%] · haut q95 +6.76% · bas q05 -7.24%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.26 · part idiosyncratique 0.74
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 62.7  _(momentum haussier)_
- **ADX** : 7.5  _(pas de tendance nette)_
- **MACD** : hist 410.121  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 14.9%
- **ATR** : 9500.0 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.007  _(neutre)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 46.0  _(transition)_
- **MA** : MA20 267075.0 · MA50 256830.0 · MA200 227978.31  _(prix > MA20)_
- **Dist MA** : MA20 +0.5% · MA50 +4.5% · MA200 +17.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (572064 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
