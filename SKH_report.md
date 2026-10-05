# 000660

**Generated** : 2026-10-05T00:15:50.763897+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1841000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1841000.00 (+2.2% vs entrée) · entrée ₩1800711.10 · stop ₩1773700.43 · T1 ₩1837568.24 · R/R 1.36  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.117 _(réel 5 s)_ (GBM -0.022) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -131 % hors [0,100] (R² max 1.00). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1793933.13–₩1807489.07 (mid ₩1800711.10)
- Spot actuel : ₩1841000.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1773700.43 (plancher anti-bruit 5 s — stop EV-optimal −1.5% (first-passage 5 s réel) ; -1.50 % depuis l'entree)
- Targets : T1 ₩1837568.24 · R/R 1.36 | T2 ₩1874425.38 · R/R 2.73 | T3 ₩1911282.53 · R/R 4.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1773700.43


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.48 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.35 %)** : le gap seul le franchit 0.246 % des séances (3 fois sur 1219).
   - exécution **0.988 pt plus bas** dans le cas TYPIQUE (médiane), 1.405 au p90, **1.51 au pire**
   - perte réelle **10.381 %** en moyenne _(tirée par la queue)_, jusqu'à **10.86 %** — au lieu des 9.35 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0025 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.443 % | p01 -6.994 % | pire -10.86 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4763** [0.4028 ; 0.5506] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4632** [0.4111 ; 0.5159] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4178** [0.3667 ; 0.4703] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.7 pt), deep (27.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.71 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.92 % contre 6.64 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.74 % si l'on extrapolait par √5 _(rapport 0.875 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4161** (β de hausse 1.6213, asymétrie 0.8735) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.022 | EV/share : ₩-590.250 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 19 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 7.0 | side 8.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.193% → cible +2.047% / stop −1.5%, p_fill 55%, n_eff≈62.8) : P(cible|rempli) **31%** · **EV/risk -0.117** (×p_fill ; si rempli -0.32% du capital)
  - **swing** (entrée dip −4.814% → cible +9.531% / stop −4.765%, p_fill 45%, n_eff≈50.9) : P(cible|rempli) **26%** · **EV/risk -0.062** (×p_fill ; si rempli -0.67% du capital)
  - **deep** (entrée dip −7.444% → cible +12.638% / stop −6.489%, p_fill 41%, n_eff≈45.2) : P(cible|rempli) **34%** · **EV/risk -0.007** (×p_fill ; si rempli -0.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→54% · +3.0%→38% · +5.0%→21% · +8.0%→8%
- Range intraday médian 5.51% (p90 10.55%) · excursion haute méd. +2.19% / basse méd. −2.54%
- Profil de vol intra : ouverture 2.923% vs midi 1.197% vs clôture 1.401% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 57% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.174% ; recovery-V 21%
- **σ réalisé intraday** 2.966% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 58% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1845912.5 (VA 1837812.5–1847937.5 ; dernier close 1843000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 70% · **stop −7.14%** sous le fill (sous le bruit) · cible +2.04% · R/R 0.29 (high win-rate)
- Gaps overnight (n=152) : méd. 0.6% · baisse 45% (gap-down >1% 29% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.8%) · haut méd +0.76% · range méd 1.36%
- Excursion ouverture 15min (n=160) : bas méd −0.84% (p90 −2.29%) · haut méd +0.95% · range méd 1.86%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −3.02%) · haut méd +1.28% · range méd 2.47%
- Excursion ouverture 60min (n=160) : bas méd −1.23% (p90 −3.82%) · haut méd +1.38% · range méd 2.98%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1841000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 63% (93/152) · gap 37% · délai 0.0min · rebond 60% (53/93) (MFE +1.37%)
   - −1.0% : fill 30min 45% · séance 59% (86/152) · gap 29% · délai 0.0min · rebond 61% (55/86) (MFE +1.52%)
   - −1.5% : fill 30min 36% · séance 53% (78/152) · gap 24% · délai 0.1min · rebond 69% (53/78) (MFE +1.6%)
   - −2.0% : fill 30min 30% · séance 42% (69/152) · gap 22% · délai 0.0min · rebond 61% (45/69) (MFE +1.77%)
   - −3.0% : fill 30min 26% · séance 38% (59/152) · gap 18% · délai 0.8min · rebond 69% (40/59) (MFE +1.74%)
   - −4.0% : fill 30min 21% · séance 31% (50/152) · gap 12% · délai 1.0min · rebond 64% (35/50) (MFE +2.2%)
   - −5.0% : fill 30min 13% · séance 24% (38/152) · gap 7% · délai 12.9min · rebond 70% (25/38) (MFE +2.04%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.29% (p90 −2.29%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −2.55%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.65%) → stop au-delà de −2.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=831 jambes) : jambe baissière méd −1.2% (p90 −3.25%) · ~10.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 97% (59/60) · rebond 57% (33/59)
      · −2.0% : fill 73% (50/60) · rebond 49% (28/50)
      · −3.0% : fill 70% (45/60) · rebond 62% (28/45)
      · −4.0% : fill 62% (41/60) · rebond 59% (27/41)
      · −5.0% : fill 46% (31/60) · rebond 62% (18/31)
   - **flat** (10 séances) :
      · −1.0% : fill 27% (6/10) · rebond 100% (6/6)
      · −2.0% : fill 14% (3/10) · rebond 100% (3/3)
      · −3.0% : fill 10% (2/10) · rebond 100% (2/2)
      · −4.0% : fill 0% (0/10) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/10) · rebond 0% (0/0)
   - **gap-up** (82 séances) :
      · −1.0% : fill 33% (21/82) · rebond 66% (16/21)
      · −2.0% : fill 23% (16/82) · rebond 87% (14/16)
      · −3.0% : fill 17% (12/82) · rebond 86% (10/12)
      · −4.0% : fill 11% (9/82) · rebond 83% (8/9)
      · −5.0% : fill 10% (7/82) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 58% si les 15 1res min sont vertes (84 cas) · 28% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 70% si début vert vs 11% si rouge (base 45% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 223min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=89) : tient le vert **70%** · continue >prix actuel 54% ; creux résiduel méd -1.24% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.89% → **scale +1.55% / runner +2.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **11%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.13%** (au-delà de la MAE q10 -6.13%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.02% .. +2.58%] · haut q95 +3.28% · bas q05 -3.89%
   - 60min (n=160) : retour [-3.3% .. +4.21%] · haut q95 +4.7% · bas q05 -5.02%
   - 2h (n=160) : retour [-4.39% .. +4.41%] · haut q95 +5.98% · bas q05 -6.58%
   - 4h (n=160) : retour [-6.22% .. +5.15%] · haut q95 +6.66% · bas q05 -7.39%
   - 6h (n=160) : retour [-6.31% .. +5.01%] · haut q95 +7.83% · bas q05 -8.0%
   - session (n=160) : retour [-6.86% .. +5.54%] · haut q95 +8.01% · bas q05 -8.13%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 000660 = **volatil sans tendance propre (choppy)** (vol intra méd 3.1%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.25 · part idiosyncratique 0.75
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 49.0  _(neutre)_
- **ADX** : 9.9  _(pas de tendance nette)_
- **MACD** : hist 3071.117  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 17.2%
- **ATR** : 73714.29 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.025  _(neutre)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 1782050.0 · MA50 1684917.99 · MA200 1417721.04  _(prix > MA20)_
- **Dist MA** : MA20 +3.3% · MA50 +9.3% · MA200 +29.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (545219 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
