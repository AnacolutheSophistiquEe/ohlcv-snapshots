# SMCI

**Generated** : 2026-07-21T21:59:44.062615+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $25.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $25.50 (+0.4% vs entrée) · entrée $25.40 · stop $24.93 · T1 $25.99 · R/R 1.26  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk -0.233 _(réel 5 s)_ (GBM 0.043) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.85% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $25.31–$25.50 (mid $25.40)
- Spot actuel : $25.50 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $24.93 (stop swing_plan-based (-3.22%))
- Targets : T1 $25.99 · R/R 1.26 | T2 $26.57 · R/R 2.49 | T3 $27.16 · R/R 3.74
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $24.93


## Edge, scénarios & sizing

- EV/risk : 0.043 | EV/share : $0.020 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 25 % | T3 24 %
- Kelly (position) : f* 0.05 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 7.3 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.384% → cible +2.303% / stop −1.853%, p_fill 95%, n_eff≈38.2) : P(cible|rempli) **34%** · **EV/risk -0.233** (×p_fill ; si rempli -0.46% du capital)
  - **swing** (entrée dip −0.662% → cible +5.15% / stop −2.575%, p_fill 85%, n_eff≈33.9) : P(cible|rempli) **17%** · **EV/risk -0.448** (×p_fill ; si rempli -1.36% du capital)
  - **deep** (entrée dip −0.881% → cible +7.283% / stop −3.641%, p_fill 89%, n_eff≈34.4) : P(cible|rempli) **20%** · **EV/risk -0.411** (×p_fill ; si rempli -1.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→64% · +3.0%→45% · +5.0%→28% · +8.0%→11%
- Range intraday médian 6.17% (p90 9.97%) · excursion haute méd. +2.57% / basse méd. −2.43%
- Profil de vol intra : ouverture 3.788% vs midi 1.213% vs clôture 1.521% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; mean-reverting — autocorr -0.053)_ ; drift intra méd. -0.756% ; recovery-V 21%
- **σ réalisé intraday** 3.997% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 70% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 24.2019 (VA 24.0331–24.4081 ; dernier close 23.83)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 73% · **stop −4.39%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 45% (gap-down >1% 32% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.78% (p90 −2.32%) · haut méd +0.91% · range méd 1.94%
- Excursion ouverture 15min (n=160) : bas méd −1.04% (p90 −3.28%) · haut méd +1.23% · range méd 2.71%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.81%) · haut méd +1.37% · range méd 3.55%
- Excursion ouverture 60min (n=160) : bas méd −1.72% (p90 −4.38%) · haut méd +1.58% · range méd 4.26%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 23.83 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 79% (127/159) · gap 40% · délai 0.0min · rebond 58% (73/127) (MFE +1.32%)
   - −1.0% : fill 30min 58% · séance 73% (115/159) · gap 32% · délai 0.0min · rebond 59% (65/115) (MFE +1.23%)
   - −1.5% : fill 30min 47% · séance 65% (99/159) · gap 24% · délai 0.5min · rebond 62% (59/99) (MFE +1.42%)
   - −2.0% : fill 30min 43% · séance 56% (89/159) · gap 21% · délai 1.1min · rebond 64% (55/89) (MFE +1.59%)
   - −3.0% : fill 30min 28% · séance 50% (71/159) · gap 14% · délai 18.8min · rebond 59% (42/71) (MFE +1.6%)
   - −4.0% : fill 30min 21% · séance 39% (52/159) · gap 10% · délai 16.1min · rebond 67% (32/52) (MFE +1.63%)
   - −5.0% : fill 30min 18% · séance 33% (43/159) · gap 6% · délai 19.2min · rebond 73% (29/43) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.64%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −3.11%) → stop au-delà de −1.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −3.25%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=837 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 94% (67/69) · rebond 48% (35/67)
      · −2.0% : fill 88% (60/69) · rebond 59% (33/60)
      · −3.0% : fill 82% (53/69) · rebond 56% (30/53)
      · −4.0% : fill 69% (42/69) · rebond 67% (26/42)
      · −5.0% : fill 57% (35/69) · rebond 71% (23/35)
   - **flat** (16 séances) :
      · −1.0% : fill 94% (14/16) · rebond 88% (11/14)
      · −2.0% : fill 44% (9/16) · rebond 77% (6/9)
      · −3.0% : fill 10% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 3% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (74 séances) :
      · −1.0% : fill 50% (34/74) · rebond 71% (19/34)
      · −2.0% : fill 29% (20/74) · rebond 74% (16/20)
      · −3.0% : fill 26% (16/74) · rebond 65% (10/16)
      · −4.0% : fill 18% (9/74) · rebond 65% (5/9)
      · −5.0% : fill 16% (8/74) · rebond 81% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 65% si les 15 1res min sont vertes (73 cas) · 23% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 75% si début vert vs 12% si rouge (base 43% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **75%** · continue >prix actuel 47% ; creux résiduel méd -1.68% (q20 -2.84%) → **SL/trailing à −2.84%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +3.0% → **scale +1.59% / runner +3.0%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **12%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +4.68%] · haut q95 +5.65% · bas q05 -4.38%
   - 60min (n=160) : retour [-4.23% .. +5.1%] · haut q95 +6.33% · bas q05 -5.53%
   - 2h (n=160) : retour [-4.79% .. +6.65%] · haut q95 +7.25% · bas q05 -5.83%
   - 4h (n=160) : retour [-5.91% .. +7.42%] · haut q95 +8.34% · bas q05 -6.96%
   - 6h (n=160) : retour [-6.48% .. +6.99%] · haut q95 +8.83% · bas q05 -8.2%
   - session (n=160) : retour [-7.29% .. +7.86%] · haut q95 +9.27% · bas q05 -8.58%


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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.0  _(momentum baissier)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist -0.155  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 36.8%
- **ATR** : 1.57 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.315  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 50.2  _(transition)_
- **MA** : MA20 27.95 · MA50 32.93 · MA200 33.81  _(prix < MA20)_
- **Dist MA** : MA20 -8.8% · MA50 -22.6% · MA200 -24.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88279 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
