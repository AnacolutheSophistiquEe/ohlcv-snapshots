# HOOD

**Generated** : 2026-08-20T20:21:49.444821+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $94.78  

> 🟡 **WAIT-FOR-DIP** — spot +0.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $94.78 (+0.7% vs entrée) · entrée $94.10 · stop $89.37 · T1 $97.91 · R/R 0.81  
> ↳ P(T1 av. stop) 54 % _(réel 5 s)_ · EV/risk 0.055 _(réel 5 s)_ (GBM -0.046) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $93.42–$94.78 (mid $94.10)
- Spot actuel : $94.78 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : $89.37 (stop swing_plan-based (-5.71%))
- Targets : T1 $97.91 · R/R 0.81 | T2 $101.72 · R/R 1.61 | T3 $105.53 · R/R 2.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $89.37


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.71 %)** : le gap seul le franchit 1.435 % des séances ; quand il le franchit, l'exécution est **3.652 points plus bas** → perte réelle **9.362 %** _(et non 5.71 %)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.456 % | p01 -7.299 % | pire -17.785 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1332** [0.0888 ; 0.1898] _(largeur 10.1 pt, n_eff 173.1)_
   - swing : **0.5122** [0.4596 ; 0.5646] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5581** [0.5054 ; 0.6098] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.9 pt), swing (32.0 pt), deep (31.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.31 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.08 % contre 4.31 % aujourd'hui, rapport 0.48)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.53 % vs -14.49 % si l'on extrapolait par √5 _(rapport 1.003 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7607** (β de hausse 1.6198, asymétrie 1.087) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.52× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.046 | EV/share : $-0.218 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 28 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 64.8 | bear 27.7 | side 7.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 474.0 (= 5 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.33% → cible +1.81% / stop −3.0%, p_fill 91%, n_eff≈37.5) : P(cible|rempli) **55%** · **EV/risk +0.019** (×p_fill ; si rempli +0.06% du capital)
  - **swing** (entrée dip −0.713% → cible +4.048% / stop −5.032%, p_fill 85%, n_eff≈34.9) : P(cible|rempli) **54%** · **EV/risk +0.055** (×p_fill ; si rempli +0.33% du capital)
  - **deep** (entrée dip −1.056% → cible +5.724% / stop −7.574%, p_fill 90%, n_eff≈36.5) : P(cible|rempli) **56%** · **EV/risk -0.054** (×p_fill ; si rempli -0.45% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→81% · +2.0%→57% · +3.0%→36% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.04% (p90 8.92%) · excursion haute méd. +2.18% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.682% vs midi 1.045% vs clôture 1.141% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑1%/↓0% ; spike-down 67% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.107 ; neutre — autocorr -0.015)_ ; drift intra méd. -0.021% ; recovery-V 33%
- **σ réalisé intraday** 3.434% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 45% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 95.7456 (VA 95.2094–98.4269 ; dernier close 95.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 29% · rebond 80% · **stop −4.62%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 50% (gap-down >1% 33% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.84% (p90 −2.37%) · haut méd +0.92% · range méd 2.11%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −3.66%) · haut méd +1.26% · range méd 2.82%
- Excursion ouverture 30min (n=160) : bas méd −1.35% (p90 −3.86%) · haut méd +1.7% · range méd 3.37%
- Excursion ouverture 60min (n=160) : bas méd −1.67% (p90 −3.91%) · haut méd +1.73% · range méd 3.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 95.78 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (124/159) · gap 40% · délai 0.0min · rebond 57% (66/124) (MFE +1.39%)
   - −1.0% : fill 30min 61% · séance 69% (109/159) · gap 33% · délai 0.0min · rebond 62% (64/109) (MFE +1.51%)
   - −1.5% : fill 30min 51% · séance 60% (99/159) · gap 25% · délai 0.0min · rebond 59% (57/99) (MFE +1.62%)
   - −2.0% : fill 30min 41% · séance 49% (87/159) · gap 16% · délai 0.1min · rebond 66% (54/87) (MFE +1.4%)
   - −3.0% : fill 30min 28% · séance 39% (68/159) · gap 7% · délai 6.5min · rebond 73% (46/68) (MFE +1.84%)
   - −4.0% : fill 30min 18% · séance 29% (50/159) · gap 3% · délai 10.8min · rebond 80% (34/50) (MFE +2.37%)
   - −5.0% : fill 30min 10% · séance 17% (33/159) · gap 2% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −2.44%) → stop au-delà de −1.6% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.42%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.43%) → stop au-delà de −1.53% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=762 jambes) : jambe baissière méd −1.12% (p90 −2.8%) · ~9.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 97% (70/73) · rebond 51% (36/70)
      · −2.0% : fill 82% (60/73) · rebond 62% (36/60)
      · −3.0% : fill 69% (50/73) · rebond 70% (33/50)
      · −4.0% : fill 53% (39/73) · rebond 83% (29/39)
      · −5.0% : fill 32% (27/73) · rebond 72% (20/27)
   - **flat** (20 séances) :
      · −1.0% : fill 64% (14/20) · rebond 80% (9/14)
      · −2.0% : fill 40% (11/20) · rebond 61% (7/11)
      · −3.0% : fill 14% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 13% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 6% (3/20) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 42% (25/66) · rebond 80% (19/25)
      · −2.0% : fill 19% (16/66) · rebond 88% (11/16)
      · −3.0% : fill 16% (12/66) · rebond 98% (11/12)
      · −4.0% : fill 8% (6/66) · rebond 88% (4/6)
      · −5.0% : fill 5% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 65% si les 15 1res min sont vertes (76 cas) · 34% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 78% si début vert vs 24% si rouge (base 49% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **78%** · continue >prix actuel 47% ; creux résiduel méd -1.26% (q20 -2.42%) → **SL/trailing à −2.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.25% / q75 +2.7% → **scale +1.25% / runner +2.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **24%** (continue à baisser 52%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.6%** (au-delà de la MAE q10 -3.6%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.49% .. +3.98%] · haut q95 +4.27% · bas q05 -5.22%
   - 60min (n=160) : retour [-3.65% .. +4.35%] · haut q95 +5.16% · bas q05 -5.26%
   - 2h (n=160) : retour [-4.55% .. +4.98%] · haut q95 +6.42% · bas q05 -5.58%
   - 4h (n=160) : retour [-4.64% .. +5.75%] · haut q95 +7.44% · bas q05 -6.14%
   - 6h (n=160) : retour [-5.69% .. +6.17%] · haut q95 +7.44% · bas q05 -7.06%
   - session (n=160) : retour [-5.16% .. +5.91%] · haut q95 +7.53% · bas q05 -7.21%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0% / strong 7.5%) · base = 12 séances trend-up (n_eff 9.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **27%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.43% / p90 2.14%) · ~4.0 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=45)
   - −1.0% → **70%** (reprise méd 33.9 min, n=21)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.14%** (p90, défaut prudent ; serré/agressif −1.43%) ; extension open→close méd +6.08% (q75 +9.71% / q95 +13.38%), MFE méd +6.85% / q90 +14.87%
   - Échelle scale-out : +6.85% (33%) / +11.38% (33%) / +14.87% (34%)
- **DÉSARMER** : repli > **−2.14%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.87% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +0.75%)


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 62.4  _(momentum haussier)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist 0.391  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 13.7%
- **ATR** : 4.74 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.204  _(distribution)_
- **Vol ratio** : 1.2  _(volume normal)_
- **Choppiness** : 53.1  _(transition)_
- **MA** : MA20 93.2 · MA50 99.87 · MA200 96.27  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 -5.1% · MA200 -1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (410429 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
