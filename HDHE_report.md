# 267260

**Generated** : 2026-08-27T00:18:22.557574+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩733000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩733000.00 (+4.0% vs entrée) · entrée ₩704576.24 · stop ₩648210.14 · T1 ₩739394.58 · R/R 0.62  
> ↳ P(T1 av. stop) 13 % _(réel 5 s)_ · EV/risk -0.006 _(réel 5 s)_ (GBM -0.202) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩699590.54–₩709561.95 (mid ₩704576.24)
- Spot actuel : ₩733000.00 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : ₩648210.14 (stop swing_plan-based (-14.07%))
- Targets : T1 ₩739394.58 · R/R 0.62 | T2 ₩759264.88 · R/R 0.97 | T3 ₩779135.18 · R/R 1.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩648210.14


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.07 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.07 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.639 % | p01 -4.805 % | pire -11.715 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.088** [0.0526 ; 0.1371] _(largeur 8.4 pt, n_eff 173.1)_
   - swing : **0.4416** [0.3899 ; 0.4943] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.3913** [0.3409 ; 0.4435] _(largeur 10.3 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.1 pt), swing (41.0 pt), deep (42.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.59 %** | CVaR **-8.78 %** | vol 4.37 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.99 % contre 5.13 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.73 % vs -11.9 % si l'on extrapolait par √5 _(rapport 0.902 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0384** (β de hausse 0.822, asymétrie 1.2633) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.202 | EV/share : ₩-11355.849 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.002 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.6 | bear 7.1 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.88% → cible +4.942% / stop −8.0%, p_fill 47%, n_eff≈21.6) : P(cible|rempli) **13%** · **EV/risk -0.006** (×p_fill ; si rempli -0.11% du capital)
  - **swing** (entrée dip −8.53% → cible +7.887% / stop −6.056%, p_fill 24%, n_eff≈15.3) : P(cible|rempli) **19%** · **EV/risk -0.114** (×p_fill ; si rempli -2.84% du capital)
  - **deep** (entrée dip −13.18% → cible +11.155% / stop −9.571%, p_fill 31%, n_eff≈15.1) : P(cible|rempli) **17%** · **EV/risk -0.167** (×p_fill ; si rempli -5.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→44% · +3.0%→36% · +5.0%→11% · +8.0%→4%
- Range intraday médian 6.79% (p90 10.49%) · excursion haute méd. +1.6% / basse méd. −4.07%
- Profil de vol intra : ouverture 4.417% vs midi 1.21% vs clôture 1.27% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 84% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. -1.505% ; recovery-V 27%
- **σ réalisé intraday** 4.396% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 65% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 718850.0 (VA 715350.0–720950.0 ; dernier close 719000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 38% · rebond 75% · **stop −5.38%** sous le fill (sous le bruit) · cible +2.12% · R/R 0.39 (high win-rate)
- Gaps overnight (n=158) : méd. 1.09% · baisse 34% (gap-down >1% 17% · >2% 11%)
- Excursion ouverture 5min (n=159) : bas méd −1.87% (p90 −4.01%) · haut méd +0.95% · range méd 2.93%
- Excursion ouverture 15min (n=159) : bas méd −2.09% (p90 −4.63%) · haut méd +1.04% · range méd 3.47%
- Excursion ouverture 30min (n=159) : bas méd −2.31% (p90 −4.97%) · haut méd +1.06% · range méd 3.81%
- Excursion ouverture 60min (n=159) : bas méd −2.67% (p90 −5.52%) · haut méd +1.12% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 718000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 72% (106/158) · gap 26% · délai 0.1min · rebond 52% (56/106) (MFE +1.06%)
   - −1.0% : fill 30min 51% · séance 68% (98/158) · gap 17% · délai 0.3min · rebond 60% (59/98) (MFE +1.32%)
   - −1.5% : fill 30min 46% · séance 64% (87/158) · gap 13% · délai 0.8min · rebond 66% (56/87) (MFE +1.36%)
   - −2.0% : fill 30min 40% · séance 59% (78/158) · gap 11% · délai 1.1min · rebond 74% (56/78) (MFE +1.77%)
   - −3.0% : fill 30min 32% · séance 50% (63/158) · gap 7% · délai 4.8min · rebond 76% (48/63) (MFE +2.06%)
   - −4.0% : fill 30min 22% · séance 38% (48/158) · gap 4% · délai 18.6min · rebond 75% (34/48) (MFE +2.12%)
   - −5.0% : fill 30min 13% · séance 29% (38/158) · gap 3% · délai 37.4min · rebond 72% (27/38) (MFE +2.14%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −3.32%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.97% (p90 −3.32%) → stop au-delà de −2.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.63% (p90 −4.83%) → stop au-delà de −3.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=815 jambes) : jambe baissière méd −1.22% (p90 −3.34%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 100% (46/46) · rebond 52% (24/46)
      · −2.0% : fill 95% (40/46) · rebond 71% (26/40)
      · −3.0% : fill 90% (36/46) · rebond 75% (26/36)
      · −4.0% : fill 76% (30/46) · rebond 72% (21/30)
      · −5.0% : fill 57% (24/46) · rebond 77% (18/24)
   - **flat** (17 séances) :
      · −1.0% : fill 96% (16/17) · rebond 70% (11/16)
      · −2.0% : fill 85% (13/17) · rebond 73% (11/13)
      · −3.0% : fill 65% (11/17) · rebond 50% (8/11)
      · −4.0% : fill 58% (8/17) · rebond 62% (4/8)
      · −5.0% : fill 58% (8/17) · rebond 73% (6/8)
   - **gap-up** (95 séances) :
      · −1.0% : fill 46% (36/95) · rebond 65% (24/36)
      · −2.0% : fill 35% (25/95) · rebond 78% (19/25)
      · −3.0% : fill 25% (16/95) · rebond 89% (14/16)
      · −4.0% : fill 14% (10/95) · rebond 92% (9/10)
      · −5.0% : fill 8% (6/95) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 34% en base · 48% si les 15 1res min sont vertes (69 cas) · 27% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=159) : COUDE à **1:19** → P(séance verte=clôture>ouverture) 69% si début vert vs 12% si rouge (base 34% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **69%** · continue >prix actuel 41% ; creux résiduel méd -1.87% (q20 -3.48%) → **SL/trailing à −3.48%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.35% → **scale +1.46% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **12%** (continue à baisser 48%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.26%** (au-delà de la MAE q10 -5.26%), cible rebond +1.52% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-5.07% .. +2.68%] · haut q95 +3.91% · bas q05 -5.58%
   - 60min (n=159) : retour [-5.64% .. +2.6%] · haut q95 +4.36% · bas q05 -6.01%
   - 2h (n=159) : retour [-6.77% .. +3.66%] · haut q95 +4.93% · bas q05 -7.35%
   - 4h (n=159) : retour [-6.94% .. +3.76%] · haut q95 +5.24% · bas q05 -8.41%
   - 6h (n=159) : retour [-7.61% .. +3.71%] · haut q95 +6.2% · bas q05 -9.23%
   - session (n=159) : retour [-7.47% .. +3.89%] · haut q95 +6.26% · bas q05 -9.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 40.7  _(momentum baissier)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist 4022.343  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 33.0%
- **ATR** : 40605.26 (25.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.072  _(accumulation)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 50.7  _(transition)_
- **MA** : MA20 728613.92 · MA50 830626.53 · MA200 922273.75  _(prix > MA20)_
- **Dist MA** : MA20 +0.6% · MA50 -11.8% · MA200 -20.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (530534 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
