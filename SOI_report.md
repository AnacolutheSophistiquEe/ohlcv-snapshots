# SOI

**Generated** : 2026-08-11T21:44:12.208460+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €122.15  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €122.15 (+2.0% vs entrée) · entrée €119.73 · stop €109.20 · T1 €136.10 · R/R 1.55  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk 0.009 _(réel 5 s)_ (GBM 0.154) · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -163 % hors [0,100] (R² max 0.72). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €117.71–€121.75 (mid €119.73)
- Spot actuel : €122.15 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : €109.20 (stop swing_plan-based (-10.6%))
- Targets : T1 €136.10 · R/R 1.55 | T2 €143.01 · R/R 2.21 | T3 €149.92 · R/R 2.87
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €109.20


## Edge, scénarios & sizing

- EV/risk : 0.154 | EV/share : €1.622 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 20 % | T3 15 %
- Kelly (position) : f* 0.04 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 9.9 | bear 83.4 | side 6.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 489.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.905% → cible +5.741% / stop −2.871%, p_fill 85%, n_eff≈34.9) : P(cible|rempli) **16%** · **EV/risk -0.080** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −1.984% → cible +13.672% / stop −8.791%, p_fill 73%, n_eff≈30.6) : P(cible|rempli) **34%** · **EV/risk +0.009** (×p_fill ; si rempli +0.11% du capital)
  - **deep** (entrée dip −3.066% → cible +11.885% / stop −13.333%, p_fill 87%, n_eff≈35.6) : P(cible|rempli) **25%** · **EV/risk -0.429** (×p_fill ; si rempli -6.58% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→70% · +3.0%→57% · +5.0%→40% · +8.0%→19%
- Range intraday médian 9.18% (p90 15.62%) · excursion haute méd. +3.57% / basse méd. −3.82%
- Profil de vol intra : ouverture 5.836% vs midi 1.653% vs clôture 2.524% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 44%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.109)_ ; drift intra méd. -0.134% ; recovery-V 43%
- **σ réalisé intraday** 5.527% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 61% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 121.6262 (VA 121.1418–123.2413 ; dernier close 122.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 63% · rebond 78% · **stop −8.34%** sous le fill (sous le bruit) · cible +2.87% · R/R 0.34 (high win-rate)
- Gaps overnight (n=149) : méd. 0.13% · baisse 46% (gap-down >1% 32% · >2% 22%)
- Excursion ouverture 5min (n=150) : bas méd −1.16% (p90 −3.72%) · haut méd +1.0% · range méd 2.92%
- Excursion ouverture 15min (n=150) : bas méd −1.42% (p90 −5.03%) · haut méd +1.56% · range méd 3.66%
- Excursion ouverture 30min (n=150) : bas méd −1.58% (p90 −5.32%) · haut méd +1.84% · range méd 4.2%
- Excursion ouverture 60min (n=150) : bas méd −1.75% (p90 −5.85%) · haut méd +1.89% · range méd 4.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 80% (118/149) · gap 38% · délai 0.0min · rebond 65% (77/118) (MFE +2.15%)
   - −1.0% : fill 30min 60% · séance 75% (112/149) · gap 32% · délai 0.2min · rebond 71% (81/112) (MFE +2.06%)
   - −1.5% : fill 30min 55% · séance 71% (102/149) · gap 28% · délai 0.2min · rebond 74% (75/102) (MFE +2.26%)
   - −2.0% : fill 30min 50% · séance 63% (93/149) · gap 22% · délai 0.4min · rebond 78% (74/93) (MFE +2.87%)
   - −3.0% : fill 30min 36% · séance 52% (76/149) · gap 15% · délai 0.8min · rebond 75% (60/76) (MFE +2.91%)
   - −4.0% : fill 30min 29% · séance 43% (61/149) · gap 7% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 22% · séance 40% (53/149) · gap 2% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −3.78%) → stop au-delà de −2.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −3.19%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.98% (p90 −2.84%) → stop au-delà de −2.13% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1313 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 98% (57/58) · rebond 63% (36/57)
      · −2.0% : fill 95% (55/58) · rebond 74% (43/55)
      · −3.0% : fill 82% (46/58) · rebond 74% (37/46)
      · −4.0% : fill 71% (40/58) · rebond 81% (33/40)
      · −5.0% : fill 64% (35/58) · rebond 87% (30/35)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (74 séances) :
      · −1.0% : fill 51% (38/74) · rebond 82% (31/38)
      · −2.0% : fill 29% (23/74) · rebond 87% (19/23)
      · −3.0% : fill 23% (19/74) · rebond 83% (15/19)
      · −4.0% : fill 17% (13/74) · rebond 55% (9/13)
      · −5.0% : fill 16% (10/74) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 52% en base · 69% si les 15 1res min sont vertes (71 cas) · 34% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=150) : COUDE à **37min** → P(séance verte=clôture>ouverture) 79% si début vert vs 28% si rouge (base 52% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **79%** · continue >prix actuel 59% ; creux résiduel méd -2.41% (q20 -5.57%) → **SL/trailing à −5.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.4% / q75 +5.15% → **scale +3.4% / runner +5.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **28%** (continue à baisser 60%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.62%** (au-delà de la MAE q10 -8.62%), cible rebond +2.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-5.22% .. +6.98%] · haut q95 +7.84% · bas q05 -6.52%
   - 60min (n=150) : retour [-5.92% .. +7.02%] · haut q95 +9.17% · bas q05 -6.93%
   - 2h (n=150) : retour [-6.02% .. +9.59%] · haut q95 +12.32% · bas q05 -7.46%
   - 4h (n=150) : retour [-6.8% .. +10.03%] · haut q95 +13.96% · bas q05 -8.12%
   - 6h (n=150) : retour [-7.64% .. +10.59%] · haut q95 +14.2% · bas q05 -9.53%
   - session (n=150) : retour [-11.11% .. +13.62%] · haut q95 +15.45% · bas q05 -12.68%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.0% des séances sont trend-up (mild 0% / strong 6.0%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 5% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.08% (p75 1.67% / p90 2.95%) · ~6.0 replis/séance, durée méd 38.95 min. P(nouveau plus-haut après repli) :
   - −0.5% → **94%** (reprise méd 20.0 min, n=57)
   - −1.0% → **92%** (reprise méd 34.22 min, n=33)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.95%** (p90, défaut prudent ; serré/agressif −1.67%) ; extension open→close méd +10.12% (q75 +13.85% / q95 +17.31%), MFE méd +10.12% / q90 +18.28%
   - Échelle scale-out : +10.12% (33%) / +16.57% (33%) / +18.28% (34%)
- **DÉSARMER** : repli > **−2.95%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.28% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +3.01%)


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 68.1  _(momentum haussier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist 3.16  _(pas de croisement recent)_
- **BB** : %B 0.81 · largeur 46.9%
- **ATR** : 10.53 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.021  _(neutre)_
- **Vol ratio** : 0.32  _(volume atone)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 106.47 · MA50 116.84 · MA200 73.41  _(prix > MA20)_
- **Dist MA** : MA20 +14.7% · MA50 +4.5% · MA200 +66.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (99519 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
