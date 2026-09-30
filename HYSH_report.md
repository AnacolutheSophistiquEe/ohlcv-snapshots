# 298040

**Generated** : 2026-09-30T00:20:55.833268+00:00  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩2804000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩2804000.00 (+2.0% vs entrée) · entrée ₩2748350.03 · stop ₩2528482.03 · T1 ₩2800865.55 · R/R 0.24  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2737846.93–₩2758853.14 (mid ₩2748350.03)
- Spot actuel : ₩2804000.00 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : ₩2528482.03 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩2800865.55 · R/R 0.24 | T2 ₩2853381.06 · R/R 0.48 | T3 ₩2905896.58 · R/R 0.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2528482.03


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.20 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.64 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **3.046 pt plus bas** dans le cas TYPIQUE (médiane), 3.046 au p90, **3.046 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 8.64 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0025 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.476 % | p01 -4.657 % | pire -11.686 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0631** [0.0339 ; 0.1067] _(largeur 7.3 pt, n_eff 173.1)_
   - swing : **0.4553** [0.4034 ; 0.508] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.3771** [0.3272 ; 0.429] _(largeur 10.2 pt, n_eff 345.6)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 53.6 observations effectives », dont la borne haute a 95 % vaut environ 5.6 %.
- ⚠ **5 s — échantillon insuffisant sur : deep (25.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.94 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.49 % contre 5.73 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.96 % vs -12.6 % si l'on extrapolait par √5 _(rapport 0.949 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0758** (β de hausse 0.9975, asymétrie 1.0785) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.072 | EV/share : ₩-15857.098 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 28 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 9.8 | side 5.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.989% → cible +1.911% / stop −8.0%, p_fill 73%, n_eff≈76.9) : P(cible|rempli) **52%** · **EV/risk -0.049** (×p_fill ; si rempli -0.54% du capital)
  - **swing** (entrée dip −4.363% → cible +4.273% / stop −4.472%, p_fill 56%, n_eff≈63.8) : P(cible|rempli) **49%** · **EV/risk -0.049** (×p_fill ; si rempli -0.39% du capital)
  - **deep** (entrée dip −6.744% → cible +6.042% / stop −6.88%, p_fill 50%, n_eff≈53.6) : P(cible|rempli) **43%** · **EV/risk -0.124** (×p_fill ; si rempli -1.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→65% · +2.0%→52% · +3.0%→35% · +5.0%→20% · +8.0%→6%
- Range intraday médian 6.35% (p90 9.57%) · excursion haute méd. +2.16% / basse méd. −3.4%
- Profil de vol intra : ouverture 4.058% vs midi 1.063% vs clôture 1.083% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 82% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr -0.019)_ ; drift intra méd. -1.083% ; recovery-V 32%
- **σ réalisé intraday** 4.052% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 57% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 2704250.0 (VA 2689250.0–2731750.0 ; dernier close 2733000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 75% · **stop −4.28%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.52 (high win-rate)
- Gaps overnight (n=153) : méd. 0.91% · baisse 34% (gap-down >1% 25% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.61% (p90 −3.25%) · haut méd +0.67% · range méd 2.45%
- Excursion ouverture 15min (n=160) : bas méd −2.06% (p90 −4.21%) · haut méd +0.8% · range méd 3.14%
- Excursion ouverture 30min (n=160) : bas méd −2.45% (p90 −4.35%) · haut méd +0.84% · range méd 3.88%
- Excursion ouverture 60min (n=160) : bas méd −2.61% (p90 −5.28%) · haut méd +1.05% · range méd 4.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2732000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 69% (101/153) · gap 31% · délai 0.0min · rebond 54% (60/101) (MFE +1.13%)
   - −1.0% : fill 30min 58% · séance 65% (94/153) · gap 25% · délai 0.4min · rebond 52% (54/94) (MFE +1.29%)
   - −1.5% : fill 30min 49% · séance 57% (85/153) · gap 22% · délai 1.0min · rebond 50% (50/85) (MFE +1.01%)
   - −2.0% : fill 30min 46% · séance 55% (78/153) · gap 18% · délai 2.5min · rebond 54% (43/78) (MFE +1.08%)
   - −3.0% : fill 30min 34% · séance 46% (64/153) · gap 12% · délai 5.3min · rebond 66% (42/64) (MFE +1.49%)
   - −4.0% : fill 30min 26% · séance 41% (56/153) · gap 7% · délai 19.2min · rebond 72% (42/56) (MFE +2.33%)
   - −5.0% : fill 30min 17% · séance 35% (44/153) · gap 5% · délai 53.0min · rebond 75% (32/44) (MFE +2.24%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.81% (p90 −3.47%) → stop au-delà de −2.44% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −3.09%) → stop au-delà de −2.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.68%) → stop au-delà de −2.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=879 jambes) : jambe baissière méd −1.37% (p90 −3.36%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 100% (47/47) · rebond 45% (26/47)
      · −2.0% : fill 94% (42/47) · rebond 48% (22/42)
      · −3.0% : fill 94% (41/47) · rebond 63% (26/41)
      · −4.0% : fill 91% (37/47) · rebond 72% (26/37)
      · −5.0% : fill 76% (30/47) · rebond 83% (23/30)
   - **flat** (19 séances) :
      · −1.0% : fill 79% (14/19) · rebond 48% (8/14)
      · −2.0% : fill 76% (13/19) · rebond 31% (5/13)
      · −3.0% : fill 41% (8/19) · rebond 57% (5/8)
      · −4.0% : fill 41% (8/19) · rebond 54% (6/8)
      · −5.0% : fill 32% (4/19) · rebond 40% (2/4)
   - **gap-up** (87 séances) :
      · −1.0% : fill 42% (33/87) · rebond 64% (20/33)
      · −2.0% : fill 28% (23/87) · rebond 78% (16/23)
      · −3.0% : fill 20% (15/87) · rebond 78% (11/15)
      · −4.0% : fill 13% (11/87) · rebond 86% (10/11)
      · −5.0% : fill 12% (10/87) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 37% en base · 54% si les 15 1res min sont vertes (60 cas) · 29% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 73% si début vert vs 19% si rouge (base 37% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **73%** · continue >prix actuel 43% ; creux résiduel méd -1.91% (q20 -3.78%) → **SL/trailing à −3.78%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +3.76% → **scale +1.67% / runner +3.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **19%** (continue à baisser 56%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.74%** (au-delà de la MAE q10 -5.74%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.18% .. +4.36%] · haut q95 +5.93% · bas q05 -5.24%
   - 60min (n=160) : retour [-5.23% .. +3.9%] · haut q95 +6.32% · bas q05 -5.98%
   - 2h (n=160) : retour [-6.0% .. +3.89%] · haut q95 +6.47% · bas q05 -7.07%
   - 4h (n=160) : retour [-6.94% .. +5.08%] · haut q95 +6.5% · bas q05 -9.11%
   - 6h (n=160) : retour [-7.55% .. +4.97%] · haut q95 +6.86% · bas q05 -9.17%
   - session (n=160) : retour [-6.98% .. +5.31%] · haut q95 +6.86% · bas q05 -9.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.13 · part idiosyncratique 0.87
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.6  _(momentum baissier)_
- **ADX** : 6.2  _(pas de tendance nette)_
- **MACD** : hist -4314.034  _(bearish_recent)_
- **BB** : %B 0.37 · largeur 11.4%
- **ATR** : 119928.57 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.129  _(distribution)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 61.8  _(marche en range (choppy))_
- **MA** : MA20 2847400.0 · MA50 2773900.0 · MA200 2824443.37  _(prix < MA20)_
- **Dist MA** : MA20 -1.5% · MA50 +1.1% · MA200 -0.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (554824 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
