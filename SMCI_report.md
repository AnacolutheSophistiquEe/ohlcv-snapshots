# SMCI

**Generated** : 2026-07-17T22:01:26.599936+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $24.18  

> 🟡 **WAIT-FOR-DIP** — spot +5.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $24.18 (+5.1% vs entrée) · entrée $23.00 · stop $22.43 · T1 $23.74 · R/R 1.3  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.041 · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -31 % hors [0,100] (R² max 0.44). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $22.86–$23.15 (mid $23.00)
- Spot actuel : $24.18 (+5.1% au-dessus de la zone — repli à attendre)
- Stop : $22.43 (stop swing_plan-based (-13.87%))
- Targets : T1 $23.74 · R/R 1.3 | T2 $24.47 · R/R 2.58 | T3 $25.20 · R/R 3.86
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $22.43


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : $0.024 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 26 % | T3 26 %
- Kelly (position) : f* 0.059 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 7.3 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.862% → cible +3.184% / stop −2.5%, p_fill 26%, n_eff≈9.7) : P(cible|rempli) **22%** · **EV/risk -0.025** (×p_fill ; si rempli -0.24% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→62% · +3.0%→44% · +5.0%→28% · +8.0%→11%
- Range intraday médian 6.17% (p90 9.97%) · excursion haute méd. +2.55% / basse méd. −2.56%
- Profil de vol intra : ouverture 3.8% vs midi 1.207% vs clôture 1.527% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑0%/↓1% ; spike-down 69% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.143 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. -0.703% ; recovery-V 24%
- **σ réalisé intraday** 4.071% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 38% / bas 72% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 24.9947 (VA 24.8402–25.4068 ; dernier close 24.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 72% · **stop −4.55%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 44% (gap-down >1% 31% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.01%) · haut méd +0.92% · range méd 1.94%
- Excursion ouverture 15min (n=160) : bas méd −1.04% (p90 −3.1%) · haut méd +1.34% · range méd 2.71%
- Excursion ouverture 30min (n=160) : bas méd −1.35% (p90 −3.66%) · haut méd +1.45% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.62% (p90 −4.4%) · haut méd +1.66% · range méd 4.26%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 24.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 78% (126/159) · gap 39% · délai 0.0min · rebond 56% (71/126) (MFE +1.2%)
   - −1.0% : fill 30min 58% · séance 72% (114/159) · gap 31% · délai 0.0min · rebond 57% (63/114) (MFE +1.18%)
   - −1.5% : fill 30min 46% · séance 64% (98/159) · gap 25% · délai 0.6min · rebond 60% (58/98) (MFE +1.21%)
   - −2.0% : fill 30min 43% · séance 56% (89/159) · gap 21% · délai 1.8min · rebond 63% (55/89) (MFE +1.58%)
   - −3.0% : fill 30min 27% · séance 50% (70/159) · gap 14% · délai 20.3min · rebond 58% (41/70) (MFE +1.53%)
   - −4.0% : fill 30min 20% · séance 39% (51/159) · gap 10% · délai 22.7min · rebond 65% (31/51) (MFE +1.49%)
   - −5.0% : fill 30min 16% · séance 32% (42/159) · gap 7% · délai 23.7min · rebond 72% (28/42) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.5% (p90 −2.03%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −2.67%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −2.68%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=831 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 94% (66/68) · rebond 46% (34/66)
      · −2.0% : fill 87% (59/68) · rebond 57% (32/59)
      · −3.0% : fill 82% (52/68) · rebond 54% (29/52)
      · −4.0% : fill 67% (41/68) · rebond 65% (25/41)
      · −5.0% : fill 55% (34/68) · rebond 68% (22/34)
   - **flat** (17 séances) :
      · −1.0% : fill 94% (15/17) · rebond 86% (11/15)
      · −2.0% : fill 45% (10/17) · rebond 78% (7/10)
      · −3.0% : fill 10% (2/17) · rebond 100% (2/2)
      · −4.0% : fill 3% (1/17) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/17) · rebond 0% (0/0)
   - **gap-up** (74 séances) :
      · −1.0% : fill 48% (33/74) · rebond 68% (18/33)
      · −2.0% : fill 30% (20/74) · rebond 74% (16/20)
      · −3.0% : fill 27% (16/74) · rebond 65% (10/16)
      · −4.0% : fill 18% (9/74) · rebond 65% (5/9)
      · −5.0% : fill 16% (8/74) · rebond 81% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 67% si les 15 1res min sont vertes (73 cas) · 24% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 82% si début vert vs 16% si rouge (base 45% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **82%** · continue >prix actuel 52% ; creux résiduel méd -1.51% (q20 -3.05%) → **SL/trailing à −3.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.9% / q75 +3.64% → **scale +1.9% / runner +3.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **16%** (continue à baisser 60%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.14%** (au-delà de la MAE q10 -6.14%), cible rebond +1.87% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.13% .. +4.68%] · haut q95 +5.78% · bas q05 -4.4%
   - 60min (n=160) : retour [-4.28% .. +5.1%] · haut q95 +6.39% · bas q05 -5.65%
   - 2h (n=160) : retour [-4.79% .. +6.65%] · haut q95 +7.25% · bas q05 -5.83%
   - 4h (n=160) : retour [-6.18% .. +7.42%] · haut q95 +8.43% · bas q05 -6.98%
   - 6h (n=160) : retour [-6.49% .. +6.99%] · haut q95 +8.88% · bas q05 -8.36%
   - session (n=160) : retour [-7.35% .. +7.98%] · haut q95 +9.34% · bas q05 -8.75%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.83% / p90 2.16%) · ~4.0 replis/séance, durée méd 39.36 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.85 min, n=40)
   - −1.0% → **72%** (reprise méd 30.0 min, n=18)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.16%** (p90, défaut prudent ; serré/agressif −1.83%) ; extension open→close méd +7.84% (q75 +8.65% / q95 +9.89%), MFE méd +8.72% / q90 +10.35%
   - Échelle scale-out : +8.72% (33%) / +9.18% (33%) / +10.35% (34%)
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.1  _(survente)_
- **ADX** : 24.0  _(pas de tendance nette)_
- **MACD** : hist -0.226  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 39.3%
- **ATR** : 1.77 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.158  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 43.5  _(transition)_
- **MA** : MA20 28.79 · MA50 33.31 · MA200 34.06  _(prix < MA20)_
- **Dist MA** : MA20 -16.0% · MA50 -27.4% · MA200 -29.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87517 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
