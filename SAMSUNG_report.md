# 005930

**Generated** : 2026-09-30T00:18:48.225436+00:00  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩272500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩272500.00 (+7.6% vs entrée) · entrée ₩253139.47 · stop ₩243460.90 · T1 ₩262252.35 · R/R 0.94  
> ↳ ¼-Kelly 0.061 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩251316.90–₩254962.05 (mid ₩253139.47)
- Spot actuel : ₩272500.00 (+7.6% au-dessus de la zone — repli à attendre)
- Stop : ₩243460.90 (plancher anti-bruit (R/R<2) ; -3.82 % depuis l'entree)
- Targets : T1 ₩262252.35 · R/R 0.94 | T2 ₩271365.22 · R/R 1.88 | T3 ₩280478.09 · R/R 2.82
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩243460.90


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.11 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.66 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **0.282 pt plus bas** dans le cas TYPIQUE (médiane), 0.282 au p90, **0.282 au pire**
   - perte réelle **10.942 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 10.66 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0002 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.482 % | p01 -4.951 % | pire -10.942 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0339** [0.0141 ; 0.069] _(largeur 5.5 pt, n_eff 173.1)_
   - swing : **0.3492** [0.3004 ; 0.4006] _(largeur 10.0 pt, n_eff 345.6)_
   - deep : **0.3022** [0.2556 ; 0.3521] _(largeur 9.7 pt, n_eff 345.6)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 24.6 observations effectives », dont la borne haute a 95 % vaut environ 12.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.8 pt), swing (33.3 pt), deep (36.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.76 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.86 % contre 5.59 % aujourd'hui, rapport 0.51)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.38 % vs -7.36 % si l'on extrapolait par √5 _(rapport 0.868 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1727** (β de hausse 1.3385, asymétrie 0.8761) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.3 | EV/share : ₩2900.200 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 42 % | T3 28 %
- Kelly (position) : f* 0.243 | ¼-Kelly 0.061 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 22.4 | bear 5.0 | side 72.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 531.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.228% → cible +1.61% / stop −8.0%, p_fill 37%, n_eff≈38.1) : P(cible|rempli) **50%** · **EV/risk -0.032** (×p_fill ; si rempli -0.68% du capital)
  - **swing** (entrée dip −7.108% → cible +3.6% / stop −3.823%, p_fill 29%, n_eff≈32.2) : P(cible|rempli) **49%** · **EV/risk -0.016** (×p_fill ; si rempli -0.21% du capital)
  - **deep** (entrée dip −10.982% → cible +5.091% / stop −5.985%, p_fill 24%, n_eff≈24.6) : P(cible|rempli) **63%** · **EV/risk +0.037** (×p_fill ; si rempli +0.93% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→68% · +2.0%→44% · +3.0%→31% · +5.0%→18% · +8.0%→3%
- Range intraday médian 4.97% (p90 9.02%) · excursion haute méd. +1.84% / basse méd. −2.33%
- Profil de vol intra : ouverture 2.62% vs midi 1.136% vs clôture 1.287% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 66% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.087)_ ; drift intra méd. -0.324% ; recovery-V 25%
- **σ réalisé intraday** 3.565% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 68% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 254825.0 (VA 254525.0–258725.0 ; dernier close 256000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 48% · **stop −6.27%** sous le fill (sous le bruit) · cible +0.84% · R/R 0.13 (high win-rate)
- Gaps overnight (n=153) : méd. 0.68% · baisse 45% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.65% (p90 −1.64%) · haut méd +0.6% · range méd 1.41%
- Excursion ouverture 15min (n=160) : bas méd −0.92% (p90 −2.34%) · haut méd +0.8% · range méd 2.07%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.09%) · haut méd +1.01% · range méd 2.41%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −3.57%) · haut méd +1.29% · range méd 3.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 255500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 67% (92/153) · gap 38% · délai 0.0min · rebond 47% (45/92) (MFE +0.92%)
   - −1.0% : fill 30min 46% · séance 60% (85/153) · gap 36% · délai 0.0min · rebond 57% (47/85) (MFE +1.3%)
   - −1.5% : fill 30min 42% · séance 52% (72/153) · gap 28% · délai 0.0min · rebond 56% (40/72) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 50% (67/153) · gap 25% · délai 0.0min · rebond 59% (40/67) (MFE +1.6%)
   - −3.0% : fill 30min 29% · séance 42% (57/153) · gap 23% · délai 0.0min · rebond 47% (30/57) (MFE +0.92%)
   - −4.0% : fill 30min 20% · séance 34% (44/153) · gap 10% · délai 5.8min · rebond 48% (24/44) (MFE +0.99%)
   - −5.0% : fill 30min 12% · séance 24% (33/153) · gap 8% · délai 44.7min · rebond 48% (20/33) (MFE +0.84%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.88%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −2.88%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.67%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=747 jambes) : jambe baissière méd −1.2% (p90 −3.02%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 97% (55/57) · rebond 46% (26/55)
      · −2.0% : fill 88% (47/57) · rebond 48% (24/47)
      · −3.0% : fill 83% (44/57) · rebond 43% (22/44)
      · −4.0% : fill 71% (36/57) · rebond 44% (19/36)
      · −5.0% : fill 52% (28/57) · rebond 38% (15/28)
   - **flat** (15 séances) :
      · −1.0% : fill 72% (11/15) · rebond 53% (5/11)
      · −2.0% : fill 45% (7/15) · rebond 79% (5/7)
      · −3.0% : fill 30% (5/15) · rebond 22% (2/5)
      · −4.0% : fill 19% (2/15) · rebond 0% (0/2)
      · −5.0% : fill 19% (2/15) · rebond 100% (2/2)
   - **gap-up** (81 séances) :
      · −1.0% : fill 29% (19/81) · rebond 86% (16/19)
      · −2.0% : fill 21% (13/81) · rebond 86% (11/13)
      · −3.0% : fill 13% (8/81) · rebond 78% (6/8)
      · −4.0% : fill 9% (6/81) · rebond 93% (5/6)
      · −5.0% : fill 4% (3/81) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 60% si les 15 1res min sont vertes (78 cas) · 23% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 72% si début vert vs 9% si rouge (base 41% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 216min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **72%** · continue >prix actuel 62% ; creux résiduel méd -1.24% (q20 -4.38%) → **SL/trailing à −4.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.17% / q75 +4.03% → **scale +2.17% / runner +4.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **9%** (continue à baisser 68%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.36%** (au-delà de la MAE q10 -6.36%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +2.63%] · haut q95 +3.39% · bas q05 -3.66%
   - 60min (n=160) : retour [-3.08% .. +4.22%] · haut q95 +4.95% · bas q05 -3.95%
   - 2h (n=160) : retour [-4.51% .. +4.68%] · haut q95 +5.86% · bas q05 -5.56%
   - 4h (n=160) : retour [-5.86% .. +5.29%] · haut q95 +6.82% · bas q05 -7.42%
   - 6h (n=160) : retour [-6.7% .. +5.28%] · haut q95 +6.93% · bas q05 -7.69%
   - session (n=160) : retour [-6.18% .. +5.4%] · haut q95 +6.93% · bas q05 -8.4%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.26 · part idiosyncratique 0.74
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.6  _(neutre)_
- **ADX** : 9.7  _(pas de tendance nette)_
- **MACD** : hist 1893.536  _(pas de croisement recent)_
- **BB** : %B 0.73 · largeur 16.1%
- **ATR** : 9678.57 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.094  _(accumulation)_
- **Vol ratio** : 0.94  _(volume normal)_
- **Choppiness** : 46.7  _(transition)_
- **MA** : MA20 262875.0 · MA50 255380.0 · MA200 223831.41  _(prix > MA20)_
- **Dist MA** : MA20 +3.7% · MA50 +6.7% · MA200 +21.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (562614 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
