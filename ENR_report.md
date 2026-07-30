# ENR

**Generated** : 2026-07-30T00:05:28.570433+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €135.68  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €135.68 (+3.6% vs entrée) · entrée €130.95 · stop €128.76 · T1 €133.33 · R/R 1.09  
> ↳ P(T1 av. stop) 43 % · EV/risk -0.006 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.68% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -109 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €130.48–€131.43 (mid €130.95)
- Spot actuel : €135.68 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : €128.76 (stop swing_plan-based (-9.54%))
- Targets : T1 €133.33 · R/R 1.09 | T2 €135.71 · R/R 2.17 | T3 €138.09 · R/R 3.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.76


## Edge, scénarios & sizing

- EV/risk : -0.006 | EV/share : €-0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 18 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.8 | bear 44.5 | side 47.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.481% → cible +1.816% / stop −1.678%, p_fill 30%, n_eff≈11.0) : P(cible|rempli) **7%** · **EV/risk -0.122** (×p_fill ; si rempli -0.67% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→60% · +2.0%→44% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.95% (p90 6.24%) · excursion haute méd. +1.47% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.042% vs midi 0.912% vs clôture 1.163% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.015)_ ; drift intra méd. -0.576% ; recovery-V 16%
- **σ réalisé intraday** 2.657% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 69% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 145.517 (VA 140.723–146.927 ; dernier close 137.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 63% · **stop −4.13%** sous le fill (sous le bruit) · cible +1.33% · R/R 0.32 (high win-rate)
- Gaps overnight (n=159) : méd. 0.26% · baisse 42% (gap-down >1% 24% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.76%) · haut méd +0.45% · range méd 1.2%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.6% · range méd 1.54%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.31%) · haut méd +0.61% · range méd 1.86%
- Excursion ouverture 60min (n=160) : bas méd −0.93% (p90 −2.57%) · haut méd +0.7% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 137.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 73% (117/159) · gap 31% · délai 0.2min · rebond 52% (62/117) (MFE +1.08%)
   - −1.0% : fill 30min 52% · séance 69% (107/159) · gap 24% · délai 1.2min · rebond 61% (65/107) (MFE +1.34%)
   - −1.5% : fill 30min 41% · séance 62% (92/159) · gap 20% · délai 10.8min · rebond 64% (60/92) (MFE +1.51%)
   - −2.0% : fill 30min 25% · séance 48% (69/159) · gap 13% · délai 17.9min · rebond 58% (42/69) (MFE +1.38%)
   - −3.0% : fill 30min 15% · séance 34% (50/159) · gap 4% · délai 130.7min · rebond 60% (34/50) (MFE +1.41%)
   - −4.0% : fill 30min 7% · séance 23% (38/159) · gap 3% · délai 271.7min · rebond 59% (26/38) (MFE +1.22%)
   - −5.0% : fill 30min 3% · séance 17% (23/159) · gap 1% · délai 219.5min · rebond 63% (15/23) (MFE +1.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.54% (p90 −1.97%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −1.7%) → stop au-delà de −0.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.14%) → stop au-delà de −0.71% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=499 jambes) : jambe baissière méd −1.04% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 97% (50/51) · rebond 60% (29/50)
      · −2.0% : fill 77% (38/51) · rebond 58% (24/38)
      · −3.0% : fill 61% (31/51) · rebond 50% (20/31)
      · −4.0% : fill 45% (25/51) · rebond 53% (17/25)
      · −5.0% : fill 36% (17/51) · rebond 59% (11/17)
   - **flat** (28 séances) :
      · −1.0% : fill 67% (21/28) · rebond 74% (15/21)
      · −2.0% : fill 28% (9/28) · rebond 56% (4/9)
      · −3.0% : fill 14% (5/28) · rebond 80% (3/5)
      · −4.0% : fill 12% (4/28) · rebond 76% (2/4)
      · −5.0% : fill 8% (2/28) · rebond 74% (1/2)
   - **gap-up** (80 séances) :
      · −1.0% : fill 48% (36/80) · rebond 55% (21/36)
      · −2.0% : fill 33% (22/80) · rebond 60% (14/22)
      · −3.0% : fill 20% (14/80) · rebond 77% (11/14)
      · −4.0% : fill 10% (9/80) · rebond 69% (7/9)
      · −5.0% : fill 6% (4/80) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 83% si les 15 1res min sont vertes (76 cas) · 24% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 83% si début vert vs 24% si rouge (base 49% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **83%** · continue >prix actuel 65% ; creux résiduel méd -1.26% (q20 -2.86%) → **SL/trailing à −2.86%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.3% / q75 +3.32% → **scale +2.3% / runner +3.32%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **24%** (continue à baisser 66%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.59%** (au-delà de la MAE q10 -4.59%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.06%] · haut q95 +2.6% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.43% .. +2.25%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.58%] · haut q95 +2.96% · bas q05 -3.74%
   - 4h (n=160) : retour [-3.05% .. +2.67%] · haut q95 +3.86% · bas q05 -4.23%
   - 6h (n=160) : retour [-3.68% .. +3.52%] · haut q95 +4.33% · bas q05 -4.49%
   - session (n=160) : retour [-5.38% .. +4.33%] · haut q95 +5.39% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 1.3% / strong 3.7%) · base = 8 séances trend-up (n_eff 6.1)
- **ARMER** : fenêtre la + prédictive = **30 min** → P(reste trend-up à la clôture) **19%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.14% / p90 1.33%) · ~3.0 replis/séance, durée méd 68.37 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 40.0 min, n=24)
   - −1.0% → **100%** (reprise méd 77.51 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.33%** (p90, défaut prudent ; serré/agressif −1.14%) ; extension open→close méd +4.34% (q75 +4.76% / q95 +6.23%), MFE méd +4.72% / q90 +6.39%
   - Échelle scale-out : +4.72% (33%) / +5.59% (33%) / +6.39% (34%)
- **DÉSARMER** : repli > **−1.33%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.39% : P(retournement après) 0% (mèche méd 0.4%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.53%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-04 — ENR earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-04 — ENR earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 29.5  _(survente)_
- **ADX** : 21.6  _(pas de tendance nette)_
- **MACD** : hist -1.465  _(pas de croisement recent)_
- **BB** : %B -0.01 · largeur 22.1%
- **ATR** : 7.32 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.138  _(distribution)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 50.0  _(transition)_
- **MA** : MA20 153.01 · MA50 158.5 · MA200 144.12  _(prix < MA20)_
- **Dist MA** : MA20 -11.3% · MA50 -14.4% · MA200 -5.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (95547 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
