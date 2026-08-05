# SMCI

**Generated** : 2026-08-05T00:23:12.065729+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $31.69  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $31.69 (+0.5% vs entrée) · entrée $31.53 · stop $30.78 · T1 $32.66 · R/R 1.51  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.186 _(réel 5 s)_ (GBM 0.014) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.37% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $31.37–$31.69 (mid $31.53)
- Spot actuel : $31.69 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $30.78 (stop swing_plan-based (-8.81%))
- Targets : T1 $32.66 · R/R 1.51 | T2 $33.78 · R/R 3.0 | T3 $34.91 · R/R 4.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $30.78


## Edge, scénarios & sizing

- EV/risk : 0.014 | EV/share : $0.011 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 23 % | T3 23 %
- Kelly (position) : f* 0.043 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 66.3 | bear 7.5 | side 26.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 285.0 (= 9 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.511% → cible +3.577% / stop −2.371%, p_fill 90%, n_eff≈36.2) : P(cible|rempli) **27%** · **EV/risk -0.186** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −0.945% → cible +7.999% / stop −7.94%, p_fill 86%, n_eff≈34.2) : P(cible|rempli) **24%** · **EV/risk -0.419** (×p_fill ; si rempli -3.85% du capital)
  - **deep** (entrée dip −1.281% → cible +32.048% / stop −16.024%, p_fill 84%, n_eff≈34.2) : P(cible|rempli) **17%** · **EV/risk -0.053** (×p_fill ; si rempli -1.01% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→76% · +2.0%→62% · +3.0%→44% · +5.0%→25% · +8.0%→11%
- Range intraday médian 6.47% (p90 10.14%) · excursion haute méd. +2.55% / basse méd. −2.68%
- Profil de vol intra : ouverture 4.011% vs midi 1.23% vs clôture 1.595% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓1% ; spike-down 69% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -0.383% ; recovery-V 20%
- **σ réalisé intraday** 4.196% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 59% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 28.7569 (VA 28.4669–28.7931 ; dernier close 28.65)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 78% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 46% (gap-down >1% 34% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.38%) · haut méd +0.93% · range méd 2.0%
- Excursion ouverture 15min (n=160) : bas méd −1.19% (p90 −3.28%) · haut méd +1.38% · range méd 2.81%
- Excursion ouverture 30min (n=160) : bas méd −1.4% (p90 −3.82%) · haut méd +1.47% · range méd 3.77%
- Excursion ouverture 60min (n=160) : bas méd −1.9% (p90 −4.98%) · haut méd +1.67% · range méd 4.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.65 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (125/159) · gap 42% · délai 0.0min · rebond 56% (73/125) (MFE +1.27%)
   - −1.0% : fill 30min 57% · séance 72% (114/159) · gap 34% · délai 0.0min · rebond 59% (66/114) (MFE +1.31%)
   - −1.5% : fill 30min 46% · séance 64% (98/159) · gap 26% · délai 0.0min · rebond 61% (60/98) (MFE +1.44%)
   - −2.0% : fill 30min 43% · séance 55% (87/159) · gap 19% · délai 0.4min · rebond 63% (54/87) (MFE +1.58%)
   - −3.0% : fill 30min 30% · séance 50% (72/159) · gap 13% · délai 10.9min · rebond 60% (44/72) (MFE +1.73%)
   - −4.0% : fill 30min 22% · séance 39% (53/159) · gap 8% · délai 15.4min · rebond 68% (33/53) (MFE +1.68%)
   - −5.0% : fill 30min 16% · séance 34% (44/159) · gap 5% · délai 39.0min · rebond 78% (31/44) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.15%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −3.29%) → stop au-delà de −1.84% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.81%) → stop au-delà de −1.86% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=866 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 95% (68/70) · rebond 51% (37/68)
      · −2.0% : fill 86% (60/70) · rebond 57% (34/60)
      · −3.0% : fill 82% (54/70) · rebond 55% (31/54)
      · −4.0% : fill 67% (42/70) · rebond 67% (26/42)
      · −5.0% : fill 57% (35/70) · rebond 76% (24/35)
   - **flat** (13 séances) :
      · −1.0% : fill 96% (12/13) · rebond 87% (9/12)
      · −2.0% : fill 45% (8/13) · rebond 76% (5/8)
      · −3.0% : fill 11% (2/13) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 49% (34/76) · rebond 69% (20/34)
      · −2.0% : fill 27% (19/76) · rebond 77% (15/19)
      · −3.0% : fill 25% (16/76) · rebond 70% (11/16)
      · −4.0% : fill 18% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 17% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 70% si les 15 1res min sont vertes (72 cas) · 22% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 79% si début vert vs 10% si rouge (base 44% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **79%** · continue >prix actuel 42% ; creux résiduel méd -1.75% (q20 -3.13%) → **SL/trailing à −3.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.61% / q75 +2.69% → **scale +1.61% / runner +2.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **10%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.52%** (au-delà de la MAE q10 -5.52%), cible rebond +1.87% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.21% .. +4.68%] · haut q95 +6.17% · bas q05 -4.53%
   - 60min (n=160) : retour [-4.5% .. +5.48%] · haut q95 +6.59% · bas q05 -5.34%
   - 2h (n=160) : retour [-5.07% .. +6.65%] · haut q95 +8.35% · bas q05 -5.85%
   - 4h (n=160) : retour [-5.61% .. +7.44%] · haut q95 +8.7% · bas q05 -6.92%
   - 6h (n=160) : retour [-6.35% .. +6.87%] · haut q95 +9.3% · bas q05 -7.64%
   - session (n=160) : retour [-7.76% .. +7.85%] · haut q95 +9.45% · bas q05 -8.37%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.84% / p90 2.17%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 14.9 min, n=37)
   - −1.0% → **72%** (reprise méd 30.0 min, n=17)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.17%** (p90, défaut prudent ; serré/agressif −1.84%) ; extension open→close méd +7.84% (q75 +8.68% / q95 +9.89%), MFE méd +8.72% / q90 +10.39%
   - Échelle scale-out : +8.72% (33%) / +9.19% (33%) / +10.39% (34%)
- **DÉSARMER** : repli > **−2.17%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.39% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 60.9  _(momentum haussier)_
- **ADX** : 16.3  _(pas de tendance nette)_
- **MACD** : hist 0.554  _(pas de croisement recent)_
- **BB** : %B 0.93 · largeur 32.1%
- **ATR** : 2.49 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.03  _(neutre)_
- **Vol ratio** : 1.2  _(volume normal)_
- **Choppiness** : 50.5  _(transition)_
- **MA** : MA20 27.87 · MA50 32.26 · MA200 32.54  _(prix > MA20)_
- **Dist MA** : MA20 +13.7% · MA50 -1.8% · MA200 -2.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91955 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
