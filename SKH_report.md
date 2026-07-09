# 000660

**Generated** : 2026-07-09T21:26:21.622433+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2186000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2186000.00 (+2.2% vs entrée) · entrée ₩2138166.61 · stop ₩2055730.90 · T1 ₩2224329.73 · R/R 1.05  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.134 _(réel 5 s)_ (GBM 0.005) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.86% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2120933.99–₩2155399.24 (mid ₩2138166.61)
- Spot actuel : ₩2186000.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : ₩2055730.90 (stop swing_plan-based (-9.1%))
- Targets : T1 ₩2224329.73 · R/R 1.05 | T2 ₩2310492.85 · R/R 2.09 | T3 ₩2396655.96 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2055730.90


## Edge, scénarios & sizing

- EV/risk : 0.005 | EV/share : ₩433.414 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.087 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.8 | bear 62.2 | side 30.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.189% → cible +4.03% / stop −3.855%, p_fill 66%, n_eff≈23.7) : P(cible|rempli) **29%** · **EV/risk -0.134** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −4.811% → cible +9.011% / stop −4.505%, p_fill 51%, n_eff≈16.9) : P(cible|rempli) **36%** · **EV/risk +0.004** (×p_fill ; si rempli +0.04% du capital)
  - **deep** (entrée dip −7.443% → cible +12.743% / stop −6.372%, p_fill 37%, n_eff≈11.7) : P(cible|rempli) **33%** · **EV/risk -0.001** (×p_fill ; si rempli -0.01% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→94% · +1.0%→81% · +2.0%→56% · +3.0%→38% · +5.0%→22% · +8.0%→12%
- Range intraday médian 5.84% (p90 10.58%) · excursion haute méd. +2.25% / basse méd. −2.45%
- Profil de vol intra : ouverture 2.748% vs midi 1.136% vs clôture 1.372% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (129 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 15% · trend ↑3%/↓0% ; spike-down 63% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. 0.12% ; recovery-V 30%
- **σ réalisé intraday** 4.752% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 69% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 2160975.0 (VA 2112025.0–2218825.0 ; dernier close 2199000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 47% · rebond 84% · **stop −7.46%** sous le fill (sous le bruit) · cible +2.67% · R/R 0.36 (high win-rate)
- Gaps overnight (n=128) : méd. -0.05% · baisse 51% (gap-down >1% 37% · >2% 28%)
- Excursion ouverture 5min (n=129) : bas méd −0.46% (p90 −1.29%) · haut méd +1.0% · range méd 1.47%
- Excursion ouverture 15min (n=129) : bas méd −0.77% (p90 −2.08%) · haut méd +1.21% · range méd 2.02%
- Excursion ouverture 30min (n=129) : bas méd −0.96% (p90 −2.98%) · haut méd +1.35% · range méd 2.62%
- Excursion ouverture 60min (n=129) : bas méd −1.26% (p90 −3.45%) · haut méd +1.74% · range méd 3.26%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2199000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 64% (78/128) · gap 40% · délai 0.0min · rebond 54% (40/78) (MFE +1.29%)
   - −1.0% : fill 30min 53% · séance 60% (71/128) · gap 37% · délai 0.0min · rebond 65% (44/71) (MFE +1.64%)
   - −1.5% : fill 30min 47% · séance 57% (65/128) · gap 34% · délai 0.0min · rebond 68% (41/65) (MFE +1.8%)
   - −2.0% : fill 30min 40% · séance 52% (59/128) · gap 28% · délai 0.0min · rebond 67% (39/59) (MFE +1.91%)
   - −3.0% : fill 30min 38% · séance 47% (51/128) · gap 22% · délai 5.8min · rebond 84% (39/51) (MFE +2.67%)
   - −4.0% : fill 30min 25% · séance 37% (38/128) · gap 12% · délai 11.9min · rebond 77% (29/38) (MFE +2.71%)
   - −5.0% : fill 30min 11% · séance 28% (30/128) · gap 8% · délai 32.1min · rebond 74% (23/30) (MFE +2.41%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.26% (p90 −2.69%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −3.06%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −3.37%) → stop au-delà de −1.74% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=627 jambes) : jambe baissière méd −1.29% (p90 −3.39%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 97% (53/55) · rebond 56% (29/53)
      · −2.0% : fill 85% (45/55) · rebond 64% (27/45)
      · −3.0% : fill 80% (40/55) · rebond 81% (29/40)
      · −4.0% : fill 68% (33/55) · rebond 73% (24/33)
      · −5.0% : fill 54% (27/55) · rebond 70% (20/27)
   - **flat** (11 séances) :
      · −1.0% : fill 88% (8/11) · rebond 81% (6/8)
      · −2.0% : fill 70% (6/11) · rebond 80% (5/6)
      · −3.0% : fill 60% (5/11) · rebond 100% (5/5)
      · −4.0% : fill 31% (2/11) · rebond 100% (2/2)
      · −5.0% : fill 14% (1/11) · rebond 100% (1/1)
   - **gap-up** (62 séances) :
      · −1.0% : fill 20% (10/62) · rebond 98% (9/10)
      · −2.0% : fill 16% (8/62) · rebond 75% (7/8)
      · −3.0% : fill 14% (6/62) · rebond 91% (5/6)
      · −4.0% : fill 8% (3/62) · rebond 100% (3/3)
      · −5.0% : fill 5% (2/62) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=129) : 49% en base · 55% si les 15 1res min sont vertes (71 cas) · 39% si rouges (58 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=129) : COUDE à **1:36** → P(séance verte=clôture>ouverture) 72% si début vert vs 20% si rouge (base 49% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 209min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **72%** · continue >prix actuel 48% ; creux résiduel méd -1.42% (q20 -4.98%) → **SL/trailing à −4.98%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +3.54% → **scale +1.29% / runner +3.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=56) : edge inversé — récupère vert seulement **20%** (continue à baisser 56%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.31%** (au-delà de la MAE q10 -6.31%), cible rebond +1.59% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=129) : retour [-2.19% .. +3.1%] · haut q95 +3.74% · bas q05 -3.43%
   - 60min (n=129) : retour [-3.37% .. +5.76%] · haut q95 +5.83% · bas q05 -4.61%
   - 2h (n=129) : retour [-4.17% .. +5.84%] · haut q95 +8.09% · bas q05 -5.2%
   - 4h (n=129) : retour [-5.13% .. +7.29%] · haut q95 +8.76% · bas q05 -7.18%
   - 6h (n=129) : retour [-6.25% .. +7.84%] · haut q95 +9.96% · bas q05 -8.64%
   - session (n=129) : retour [-5.47% .. +8.17%] · haut q95 +9.96% · bas q05 -8.7%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.0% des séances sont trend-up (mild 0% / strong 7.0%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 21% vs absente 2% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.7  _(momentum baissier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist -87503.533  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 40.7%
- **ATR** : 274785.71 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.09  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 2486550.0 · MA50 2125164.49 · MA200 1066364.77  _(prix < MA20)_
- **Dist MA** : MA20 -12.1% · MA50 +2.9% · MA200 +105.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87920 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
