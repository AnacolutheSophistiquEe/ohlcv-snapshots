# HOOD

**Generated** : 2026-07-17T00:33:12.136766+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $106.02  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot $106.02 (+4.9% vs entrée) · entrée $101.06 · stop $98.25 · T1 $106.68 · R/R 2.0  
> ↳ P(T1 av. stop) 47 % _(réel 5 s)_ · EV/risk 0.119 _(réel 5 s)_ (GBM -0.055) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $99.94–$102.19 (mid $101.06)
- Spot actuel : $106.02 (+4.9% au-dessus de la zone — repli à attendre)
- Stop : $98.25 (stop swing_plan-based (-7.33%))
- Targets : T1 $106.68 · R/R 2.0 | T2 $112.31 · R/R 4.0 | T3 $117.93 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $98.25


## Edge, scénarios & sizing

- EV/risk : -0.055 | EV/share : $-0.154 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 14 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 11.4 | bear 6.3 | side 82.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 424.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.124% → cible +2.488% / stop −3.0%, p_fill 52%, n_eff≈21.7) : P(cible|rempli) **36%** · **EV/risk -0.001** (×p_fill ; si rempli -0.01% du capital)
  - **swing** (entrée dip −4.678% → cible +5.564% / stop −2.782%, p_fill 28%, n_eff≈12.0) : P(cible|rempli) **47%** · **EV/risk +0.119** (×p_fill ; si rempli +1.19% du capital)
  - **deep** (entrée dip −7.23% → cible +7.869% / stop −3.934%, p_fill 26%, n_eff≈10.9) : P(cible|rempli) **51%** · **EV/risk +0.128** (×p_fill ; si rempli +1.92% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→55% · +3.0%→36% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.05% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.571% vs midi 1.08% vs clôture 1.059% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑1%/↓0% ; spike-down 67% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr 0.023)_ ; drift intra méd. 0.66% ; recovery-V 40%
- **σ réalisé intraday** 3.846% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 45% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 114.9622 (VA 114.3053–115.9477 ; dernier close 115.54)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 87% · **stop −4.57%** sous le fill (sous le bruit) · cible +2.72% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 51% (gap-down >1% 32% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −1.93%) · haut méd +1.03% · range méd 2.08%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.01%) · haut méd +1.26% · range méd 2.73%
- Excursion ouverture 30min (n=160) : bas méd −1.33% (p90 −3.79%) · haut méd +1.56% · range méd 3.41%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −3.85%) · haut méd +1.71% · range méd 3.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 115.54 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (122/159) · gap 41% · délai 0.0min · rebond 59% (62/122) (MFE +1.56%)
   - −1.0% : fill 30min 58% · séance 66% (108/159) · gap 32% · délai 0.0min · rebond 63% (62/108) (MFE +1.64%)
   - −1.5% : fill 30min 49% · séance 60% (100/159) · gap 22% · délai 0.6min · rebond 57% (55/100) (MFE +1.74%)
   - −2.0% : fill 30min 42% · séance 54% (89/159) · gap 14% · délai 1.1min · rebond 67% (54/89) (MFE +1.44%)
   - −3.0% : fill 30min 29% · séance 40% (66/159) · gap 7% · délai 10.8min · rebond 70% (43/66) (MFE +1.91%)
   - −4.0% : fill 30min 17% · séance 30% (50/159) · gap 3% · délai 22.3min · rebond 77% (32/50) (MFE +2.21%)
   - −5.0% : fill 30min 10% · séance 19% (31/159) · gap 1% · délai 29.8min · rebond 87% (25/31) (MFE +2.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.46%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −2.43%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.43%) → stop au-delà de −1.65% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=760 jambes) : jambe baissière méd −1.16% (p90 −2.72%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 96% (68/71) · rebond 62% (37/68)
      · −2.0% : fill 80% (57/71) · rebond 63% (33/57)
      · −3.0% : fill 64% (45/71) · rebond 66% (28/45)
      · −4.0% : fill 51% (36/71) · rebond 80% (25/36)
      · −5.0% : fill 34% (25/71) · rebond 84% (20/25)
   - **flat** (21 séances) :
      · −1.0% : fill 71% (16/21) · rebond 76% (11/16)
      · −2.0% : fill 54% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 19% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/21) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (24/67) · rebond 61% (14/24)
      · −2.0% : fill 26% (20/67) · rebond 85% (14/20)
      · −3.0% : fill 21% (15/67) · rebond 96% (13/15)
      · −4.0% : fill 14% (9/67) · rebond 87% (6/9)
      · −5.0% : fill 7% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 68% si les 15 1res min sont vertes (71 cas) · 40% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 78% si début vert vs 30% si rouge (base 53% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 55% ; creux résiduel méd -1.73% (q20 -3.85%) → **SL/trailing à −3.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +3.69% → **scale +1.65% / runner +3.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **30%** (continue à baisser 44%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.81%** (au-delà de la MAE q10 -3.81%), cible rebond +2.36% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.85% .. +4.58%] · haut q95 +5.12% · bas q05 -4.91%
   - 60min (n=160) : retour [-3.66% .. +4.53%] · haut q95 +6.36% · bas q05 -5.01%
   - 2h (n=160) : retour [-4.45% .. +6.58%] · haut q95 +7.6% · bas q05 -5.85%
   - 4h (n=160) : retour [-4.69% .. +7.27%] · haut q95 +8.43% · bas q05 -6.45%
   - 6h (n=160) : retour [-5.68% .. +6.82%] · haut q95 +8.44% · bas q05 -7.44%
   - session (n=160) : retour [-5.11% .. +7.15%] · haut q95 +8.72% · bas q05 -7.47%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **40%**. Lecture précoce 30 min : signature présente → 21% vs absente 4% (base 8%)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 61.5  _(momentum haussier)_
- **ADX** : 28.1  _(tendance etablie)_
- **MACD** : hist -0.677  _(bearish_recent)_
- **BB** : %B 0.44 · largeur 25.2%
- **ATR** : 6.69 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.002  _(neutre)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 107.55 · MA50 92.56 · MA200 101.93  _(prix < MA20)_
- **Dist MA** : MA20 -1.4% · MA50 +14.5% · MA200 +4.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91346 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
