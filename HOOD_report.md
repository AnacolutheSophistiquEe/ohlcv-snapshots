# HOOD

**Generated** : 2026-08-05T00:31:04.217264+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $93.51  

> 🟡 **WAIT-FOR-DIP** — spot +3.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $93.51 (+3.2% vs entrée) · entrée $90.60 · stop $87.88 · T1 $92.53 · R/R 0.71  
> ↳ P(T1 av. stop) 49 % _(réel 5 s)_ · EV/risk 0.036 _(réel 5 s)_ (GBM 0.014) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $90.21–$90.99 (mid $90.60)
- Spot actuel : $93.51 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : $87.88 (stop swing_plan-based (-13.86%))
- Targets : T1 $92.53 · R/R 0.71 | T2 $94.46 · R/R 1.42 | T3 $96.39 · R/R 2.13
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $87.88


## Edge, scénarios & sizing

- EV/risk : 0.014 | EV/share : $0.037 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 26 % | T3 21 %
- Kelly (position) : f* 0.043 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.3 | bear 14.1 | side 80.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.113% → cible +2.131% / stop −3.0%, p_fill 41%, n_eff≈14.8) : P(cible|rempli) **49%** · **EV/risk +0.036** (×p_fill ; si rempli +0.26% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→80% · +2.0%→56% · +3.0%→36% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.17% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.726% vs midi 1.075% vs clôture 1.13% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑1%/↓0% ; spike-down 71% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr 0.02)_ ; drift intra méd. -0.176% ; recovery-V 36%
- **σ réalisé intraday** 3.853% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 49% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 91.7149 (VA 90.4846–92.0664 ; dernier close 90.35)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 33% · rebond 79% · **stop −4.7%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.12% · baisse 54% (gap-down >1% 35% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −2.7%) · haut méd +0.88% · range méd 2.17%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −3.91%) · haut méd +1.24% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.52% (p90 −4.29%) · haut méd +1.7% · range méd 3.55%
- Excursion ouverture 60min (n=160) : bas méd −1.99% (p90 −4.68%) · haut méd +1.72% · range méd 3.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 90.35 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 82% (126/159) · gap 44% · délai 0.0min · rebond 58% (65/126) (MFE +1.38%)
   - −1.0% : fill 30min 64% · séance 72% (112/159) · gap 35% · délai 0.0min · rebond 63% (67/112) (MFE +1.53%)
   - −1.5% : fill 30min 53% · séance 64% (102/159) · gap 24% · délai 0.2min · rebond 59% (58/102) (MFE +1.74%)
   - −2.0% : fill 30min 44% · séance 55% (90/159) · gap 16% · délai 0.5min · rebond 66% (55/90) (MFE +1.47%)
   - −3.0% : fill 30min 33% · séance 44% (68/159) · gap 9% · délai 6.6min · rebond 76% (47/68) (MFE +2.11%)
   - −4.0% : fill 30min 20% · séance 33% (51/159) · gap 4% · délai 11.9min · rebond 79% (34/51) (MFE +2.33%)
   - −5.0% : fill 30min 13% · séance 21% (33/159) · gap 3% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −2.61%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.64% (p90 −2.45%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.51%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=748 jambes) : jambe baissière méd −1.14% (p90 −2.84%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 97% (71/74) · rebond 56% (38/71)
      · −2.0% : fill 82% (60/74) · rebond 61% (35/60)
      · −3.0% : fill 71% (49/74) · rebond 73% (33/49)
      · −4.0% : fill 57% (39/74) · rebond 81% (28/39)
      · −5.0% : fill 38% (27/74) · rebond 72% (20/27)
   - **flat** (22 séances) :
      · −1.0% : fill 75% (17/22) · rebond 81% (12/17)
      · −2.0% : fill 46% (12/22) · rebond 59% (7/12)
      · −3.0% : fill 16% (6/22) · rebond 23% (2/6)
      · −4.0% : fill 15% (5/22) · rebond 16% (1/5)
      · −5.0% : fill 7% (3/22) · rebond 82% (2/3)
   - **gap-up** (63 séances) :
      · −1.0% : fill 42% (24/63) · rebond 73% (17/24)
      · −2.0% : fill 26% (18/63) · rebond 88% (13/18)
      · −3.0% : fill 22% (13/63) · rebond 98% (12/13)
      · −4.0% : fill 11% (7/63) · rebond 88% (5/7)
      · −5.0% : fill 6% (3/63) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 64% si les 15 1res min sont vertes (72 cas) · 35% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 73% si début vert vs 27% si rouge (base 48% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **73%** · continue >prix actuel 53% ; creux résiduel méd -1.61% (q20 -3.28%) → **SL/trailing à −3.28%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +3.37% → **scale +1.69% / runner +3.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **27%** (continue à baisser 54%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +2.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.56% .. +4.12%] · haut q95 +4.62% · bas q05 -5.26%
   - 60min (n=160) : retour [-3.67% .. +4.36%] · haut q95 +5.74% · bas q05 -5.56%
   - 2h (n=160) : retour [-4.76% .. +4.98%] · haut q95 +6.66% · bas q05 -6.02%
   - 4h (n=160) : retour [-4.79% .. +5.91%] · haut q95 +8.24% · bas q05 -6.76%
   - 6h (n=160) : retour [-5.75% .. +6.57%] · haut q95 +8.24% · bas q05 -7.13%
   - session (n=160) : retour [-5.38% .. +6.09%] · haut q95 +8.24% · bas q05 -7.55%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 19% vs absente 3% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.42% / p90 2.12%) · ~4.0 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=47)
   - −1.0% → **70%** (reprise méd 32.75 min, n=22)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.12%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.08% (q75 +9.69% / q95 +13.38%), MFE méd +6.77% / q90 +14.84%
   - Échelle scale-out : +6.77% (33%) / +11.24% (33%) / +14.84% (34%)
- **DÉSARMER** : repli > **−2.12%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.84% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +0.61%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.6  _(survente)_
- **ADX** : 23.3  _(pas de tendance nette)_
- **MACD** : hist -1.932  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 38.8%
- **ATR** : 6.56 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.111  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 41.4  _(transition)_
- **MA** : MA20 101.37 · MA50 97.28 · MA200 98.87  _(prix < MA20)_
- **Dist MA** : MA20 -7.7% · MA50 -3.9% · MA200 -5.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87913 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
