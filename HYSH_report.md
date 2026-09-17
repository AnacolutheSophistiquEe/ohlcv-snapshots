# 298040

**Generated** : 2026-09-17T00:25:11.711206+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩2806000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2806000.00 (+2.2% vs entrée) · entrée ₩2744920.04 · stop ₩2525326.44 · T1 ₩2809284.14 · R/R 0.29  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.017 _(réel 5 s)_ (GBM -0.133) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2732047.22–₩2757792.86 (mid ₩2744920.04)
- Spot actuel : ₩2806000.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : ₩2525326.44 (stop swing_plan-based (-10.11%))
- Targets : T1 ₩2809284.14 · R/R 0.29 | T2 ₩2873648.23 · R/R 0.59 | T3 ₩2938012.33 · R/R 0.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2525326.44


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.21 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.11 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1217).
   - exécution **1.576 pt plus bas** dans le cas TYPIQUE (médiane), 1.576 au p90, **1.576 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 10.11 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0013 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.477 % | p01 -4.658 % | pire -11.686 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0684** [0.0378 ; 0.1133] _(largeur 7.6 pt, n_eff 173.1)_
   - swing : **0.4182** [0.3671 ; 0.4707] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.3607** [0.3114 ; 0.4123] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 23.1 observations effectives », dont la borne haute a 95 % vaut environ 13.0 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.3 pt), swing (38.6 pt), deep (37.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 5.0 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.64 % contre 5.94 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.96 % vs -12.61 % si l'on extrapolait par √5 _(rapport 0.949 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0726** (β de hausse 0.9981, asymétrie 1.0746) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.133 | EV/share : ₩-29130.224 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 21 % | T3 20 %
- Kelly (position) : f* 0.095 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 8.5 | side 6.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.174% → cible +2.345% / stop −8.0%, p_fill 70%, n_eff≈30.2) : P(cible|rempli) **44%** · **EV/risk -0.017** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −4.787% → cible +5.243% / stop −5.59%, p_fill 53%, n_eff≈23.1) : P(cible|rempli) **45%** · **EV/risk -0.087** (×p_fill ; si rempli -0.92% du capital)
  - **deep** (entrée dip −7.406% → cible +7.415% / stop −8.622%, p_fill 55%, n_eff≈23.2) : P(cible|rempli) **63%** · **EV/risk +0.080** (×p_fill ; si rempli +1.27% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→61% · +2.0%→50% · +3.0%→36% · +5.0%→20% · +8.0%→5%
- Range intraday médian 6.81% (p90 10.49%) · excursion haute méd. +2.05% / basse méd. −3.94%
- Profil de vol intra : ouverture 4.524% vs midi 1.157% vs clôture 1.225% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓0% ; spike-down 82% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr -0.021)_ ; drift intra méd. -1.117% ; recovery-V 32%
- **σ réalisé intraday** 4.102% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 58% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 2704250.0 (VA 2689250.0–2731750.0 ; dernier close 2733000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 75% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.09% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.91% · baisse 33% (gap-down >1% 25% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.61% (p90 −3.25%) · haut méd +0.66% · range méd 2.47%
- Excursion ouverture 15min (n=160) : bas méd −2.07% (p90 −4.21%) · haut méd +0.79% · range méd 3.14%
- Excursion ouverture 30min (n=160) : bas méd −2.44% (p90 −4.36%) · haut méd +0.81% · range méd 3.89%
- Excursion ouverture 60min (n=160) : bas méd −2.6% (p90 −5.28%) · haut méd +1.03% · range méd 4.42%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2732000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 71% (108/159) · gap 30% · délai 0.1min · rebond 55% (64/108) (MFE +1.15%)
   - −1.0% : fill 30min 58% · séance 65% (100/159) · gap 25% · délai 0.3min · rebond 55% (58/100) (MFE +1.33%)
   - −1.5% : fill 30min 48% · séance 57% (89/159) · gap 23% · délai 1.2min · rebond 51% (52/89) (MFE +1.02%)
   - −2.0% : fill 30min 45% · séance 55% (80/159) · gap 19% · délai 2.8min · rebond 54% (43/80) (MFE +1.13%)
   - −3.0% : fill 30min 32% · séance 47% (68/159) · gap 12% · délai 6.3min · rebond 67% (44/68) (MFE +1.6%)
   - −4.0% : fill 30min 24% · séance 39% (58/159) · gap 7% · délai 14.3min · rebond 71% (43/58) (MFE +2.27%)
   - −5.0% : fill 30min 18% · séance 33% (45/159) · gap 5% · délai 24.2min · rebond 75% (33/45) (MFE +2.09%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.86% (p90 −3.39%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.97% (p90 −2.67%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −2.63%) → stop au-delà de −2.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=854 jambes) : jambe baissière méd −1.38% (p90 −3.37%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 100% (52/52) · rebond 46% (29/52)
      · −2.0% : fill 91% (43/52) · rebond 43% (21/43)
      · −3.0% : fill 91% (42/52) · rebond 63% (26/42)
      · −4.0% : fill 89% (39/52) · rebond 73% (28/39)
      · −5.0% : fill 75% (32/52) · rebond 84% (25/32)
   - **flat** (18 séances) :
      · −1.0% : fill 80% (14/18) · rebond 57% (9/14)
      · −2.0% : fill 77% (13/18) · rebond 41% (6/13)
      · −3.0% : fill 43% (8/18) · rebond 59% (5/8)
      · −4.0% : fill 34% (7/18) · rebond 44% (5/7)
      · −5.0% : fill 25% (3/18) · rebond 24% (1/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 43% (34/89) · rebond 66% (20/34)
      · −2.0% : fill 29% (24/89) · rebond 78% (16/24)
      · −3.0% : fill 23% (18/89) · rebond 78% (13/18)
      · −4.0% : fill 12% (12/89) · rebond 79% (10/12)
      · −5.0% : fill 11% (10/89) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 36% en base · 52% si les 15 1res min sont vertes (61 cas) · 29% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 72% si début vert vs 18% si rouge (base 36% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **72%** · continue >prix actuel 44% ; creux résiduel méd -1.9% (q20 -3.74%) → **SL/trailing à −3.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +3.78% → **scale +1.7% / runner +3.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=96) : edge inversé — récupère vert seulement **18%** (continue à baisser 58%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.68%** (au-delà de la MAE q10 -5.68%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.18% .. +4.34%] · haut q95 +6.12% · bas q05 -5.24%
   - 60min (n=160) : retour [-5.24% .. +3.84%] · haut q95 +6.26% · bas q05 -5.95%
   - 2h (n=160) : retour [-6.01% .. +3.88%] · haut q95 +6.45% · bas q05 -6.83%
   - 4h (n=160) : retour [-6.89% .. +4.98%] · haut q95 +6.46% · bas q05 -9.06%
   - 6h (n=160) : retour [-7.53% .. +5.18%] · haut q95 +6.64% · bas q05 -9.14%
   - session (n=160) : retour [-6.97% .. +5.41%] · haut q95 +6.64% · bas q05 -9.3%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **55%**. Lecture précoce 30 min : signature présente → 17% vs absente 0% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 39.7  _(momentum baissier)_
- **ADX** : 7.0  _(pas de tendance nette)_
- **MACD** : hist -13028.447  _(bearish_recent)_
- **BB** : %B 0.41 · largeur 17.1%
- **ATR** : 149357.14 (31.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.062  _(accumulation)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 47.4  _(transition)_
- **MA** : MA20 2851400.0 · MA50 2762340.0 · MA200 2790642.99  _(prix < MA20)_
- **Dist MA** : MA20 -1.6% · MA50 +1.6% · MA200 +0.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (483580 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
