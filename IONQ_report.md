# IONQ

**Generated** : 2026-08-20T20:15:17.831590+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $41.58  

> 🟡 **WAIT-FOR-DIP** — spot +3.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $41.58 (+3.7% vs entrée) · entrée $40.09 · stop $37.16 · T1 $42.88 · R/R 0.95  
> ↳ P(T1 av. stop) 61 % _(réel 5 s)_ · EV/risk 0.079 _(réel 5 s)_ (GBM -0.049) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $39.54–$40.65 (mid $40.09)
- Spot actuel : $41.58 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $37.16 (stop swing_plan-based (-10.61%))
- Targets : T1 $42.88 · R/R 0.95 | T2 $45.67 · R/R 1.9 | T3 $48.46 · R/R 2.86
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $37.16


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.69 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.61 %)** : le gap seul le franchit 0.319 % des séances ; quand il le franchit, l'exécution est **3.356 points plus bas** → perte réelle **13.966 %** _(et non 10.61 %)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.033 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2814** [0.2184 ; 0.3516] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.5459** [0.4932 ; 0.5978] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5743** [0.5217 ; 0.6256] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.8 pt), swing (34.6 pt), deep (34.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.5 %** | CVaR **-10.11 %** | vol 6.16 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 10.32 % contre 5.85 % aujourd'hui, rapport 1.76)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.22 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2336** (β de hausse 1.9826, asymétrie 1.1266) vs IWM — 601 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.049 | EV/share : $-0.144 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 25 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 50.4 | bear 36.8 | side 12.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 249.0 (= 6 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.619% → cible +8.479% / stop −4.239%, p_fill 68%, n_eff≈28.1) : P(cible|rempli) **3%** · **EV/risk +0.003** (×p_fill ; si rempli +0.02% du capital)
  - **swing** (entrée dip −3.559% → cible +6.958% / stop −7.311%, p_fill 55%, n_eff≈28.0) : P(cible|rempli) **61%** · **EV/risk +0.079** (×p_fill ; si rempli +1.05% du capital)
  - **deep** (entrée dip −5.504% → cible +9.839% / stop −11.192%, p_fill 61%, n_eff≈29.7) : P(cible|rempli) **47%** · **EV/risk -0.121** (×p_fill ; si rempli -2.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→84% · +2.0%→69% · +3.0%→60% · +5.0%→32% · +8.0%→16%
- Range intraday médian 7.64% (p90 12.17%) · excursion haute méd. +3.66% / basse méd. −2.68%
- Profil de vol intra : ouverture 5.272% vs midi 1.467% vs clôture 1.696% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; neutre — autocorr 0.013)_ ; drift intra méd. 0.261% ; recovery-V 31%
- **σ réalisé intraday** 4.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 50% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 43.3866 (VA 43.0419–43.9284 ; dernier close 43.38)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 85% · **stop −5.12%** sous le fill (sous le bruit) · cible +3.03% · R/R 0.59 (high win-rate)
- Gaps overnight (n=159) : méd. -0.46% · baisse 56% (gap-down >1% 38% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.17% (p90 −2.84%) · haut méd +1.33% · range méd 2.79%
- Excursion ouverture 15min (n=160) : bas méd −1.6% (p90 −4.04%) · haut méd +1.52% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.16%) · haut méd +2.01% · range méd 4.57%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −5.66%) · haut méd +2.31% · range méd 5.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.38 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 83% (134/159) · gap 49% · délai 0.0min · rebond 65% (90/134) (MFE +1.89%)
   - −1.0% : fill 30min 70% · séance 76% (126/159) · gap 38% · délai 0.0min · rebond 74% (93/126) (MFE +2.36%)
   - −1.5% : fill 30min 62% · séance 70% (119/159) · gap 33% · délai 0.0min · rebond 66% (80/119) (MFE +2.18%)
   - −2.0% : fill 30min 56% · séance 63% (109/159) · gap 18% · délai 0.0min · rebond 71% (75/109) (MFE +2.36%)
   - −3.0% : fill 30min 46% · séance 55% (94/159) · gap 9% · délai 6.0min · rebond 76% (70/94) (MFE +2.79%)
   - −4.0% : fill 30min 31% · séance 43% (75/159) · gap 6% · délai 14.8min · rebond 77% (58/75) (MFE +2.83%)
   - −5.0% : fill 30min 19% · séance 35% (63/159) · gap 3% · délai 24.1min · rebond 85% (55/63) (MFE +3.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.93%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.91% (p90 −3.47%) → stop au-delà de −2.36% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.88% (p90 −2.76%) → stop au-delà de −1.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1130 jambes) : jambe baissière méd −1.3% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (79 séances) :
      · −1.0% : fill 100% (79/79) · rebond 73% (59/79)
      · −2.0% : fill 90% (73/79) · rebond 77% (56/73)
      · −3.0% : fill 78% (64/79) · rebond 76% (49/64)
      · −4.0% : fill 60% (48/79) · rebond 76% (38/48)
      · −5.0% : fill 48% (40/79) · rebond 80% (33/40)
   - **flat** (14 séances) :
      · −1.0% : fill 70% (11/14) · rebond 87% (7/11)
      · −2.0% : fill 57% (10/14) · rebond 62% (4/10)
      · −3.0% : fill 48% (8/14) · rebond 68% (4/8)
      · −4.0% : fill 48% (8/14) · rebond 81% (4/8)
      · −5.0% : fill 28% (7/14) · rebond 91% (6/7)
   - **gap-up** (66 séances) :
      · −1.0% : fill 46% (36/66) · rebond 74% (27/36)
      · −2.0% : fill 29% (26/66) · rebond 51% (15/26)
      · −3.0% : fill 25% (22/66) · rebond 79% (17/22)
      · −4.0% : fill 20% (19/66) · rebond 79% (16/19)
      · −5.0% : fill 18% (16/66) · rebond 100% (16/16)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 56% si les 15 1res min sont vertes (80 cas) · 34% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 69% si début vert vs 23% si rouge (base 46% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 234min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **69%** · continue >prix actuel 41% ; creux résiduel méd -2.95% (q20 -4.64%) → **SL/trailing à −4.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.01% / q75 +4.76% → **scale +2.01% / runner +4.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **23%** (continue à baisser 53%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.75%** (au-delà de la MAE q10 -4.75%), cible rebond +2.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.13% .. +6.95%] · haut q95 +7.88% · bas q05 -5.68%
   - 60min (n=160) : retour [-5.0% .. +6.15%] · haut q95 +8.45% · bas q05 -6.22%
   - 2h (n=160) : retour [-6.0% .. +8.2%] · haut q95 +9.12% · bas q05 -7.0%
   - 4h (n=160) : retour [-7.1% .. +7.39%] · haut q95 +10.23% · bas q05 -8.1%
   - 6h (n=160) : retour [-7.21% .. +8.58%] · haut q95 +11.16% · bas q05 -8.35%
   - session (n=160) : retour [-6.68% .. +9.12%] · haut q95 +11.26% · bas q05 -8.36%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 60.7  _(momentum haussier)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist 0.646  _(pas de croisement recent)_
- **BB** : %B 0.56 · largeur 45.7%
- **ATR** : 2.93 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.025  _(neutre)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 45.0  _(transition)_
- **MA** : MA20 40.49 · MA50 44.78 · MA200 44.93  _(prix > MA20)_
- **Dist MA** : MA20 +2.7% · MA50 -7.2% · MA200 -7.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (409365 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
