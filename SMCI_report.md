# SMCI

**Generated** : 2026-07-20T21:59:34.506623+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $23.83  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $23.83 (+4.8% vs entrée) · entrée $22.74 · stop $22.17 · T1 $23.40 · R/R 1.16  
> ↳ P(T1 av. stop) 18 % _(réel 5 s)_ · EV/risk -0.013 _(réel 5 s)_ (GBM 0.031) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $22.61–$22.87 (mid $22.74)
- Spot actuel : $23.83 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : $22.17 (stop swing_plan-based (-12.93%))
- Targets : T1 $23.40 · R/R 1.16 | T2 $24.05 · R/R 2.3 | T3 $24.71 · R/R 3.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $22.17


## Edge, scénarios & sizing

- EV/risk : 0.031 | EV/share : $0.018 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 26 % | T3 26 %
- Kelly (position) : f* 0.049 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 7.3 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.564% → cible +2.878% / stop −2.5%, p_fill 32%, n_eff≈12.4) : P(cible|rempli) **18%** · **EV/risk -0.013** (×p_fill ; si rempli -0.10% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→79% · +2.0%→64% · +3.0%→45% · +5.0%→28% · +8.0%→11%
- Range intraday médian 6.22% (p90 9.97%) · excursion haute méd. +2.57% / basse méd. −2.56%
- Profil de vol intra : ouverture 3.8% vs midi 1.214% vs clôture 1.527% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. -0.696% ; recovery-V 22%
- **σ réalisé intraday** 4.072% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 68% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 24.5184 (VA 23.8989–24.6954 ; dernier close 24.18)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 73% · **stop −4.39%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.27% · baisse 46% (gap-down >1% 32% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.39%) · haut méd +0.91% · range méd 1.95%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −3.28%) · haut méd +1.24% · range méd 2.77%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.82%) · haut méd +1.39% · range méd 3.63%
- Excursion ouverture 60min (n=160) : bas méd −1.66% (p90 −4.4%) · haut méd +1.6% · range méd 4.3%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 24.18 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 78% (127/159) · gap 40% · délai 0.0min · rebond 57% (72/127) (MFE +1.23%)
   - −1.0% : fill 30min 59% · séance 72% (115/159) · gap 32% · délai 0.0min · rebond 58% (64/115) (MFE +1.22%)
   - −1.5% : fill 30min 48% · séance 64% (99/159) · gap 25% · délai 0.1min · rebond 61% (59/99) (MFE +1.3%)
   - −2.0% : fill 30min 44% · séance 57% (90/159) · gap 21% · délai 1.1min · rebond 64% (56/90) (MFE +1.59%)
   - −3.0% : fill 30min 28% · séance 51% (71/159) · gap 14% · délai 18.8min · rebond 59% (42/71) (MFE +1.6%)
   - −4.0% : fill 30min 21% · séance 40% (52/159) · gap 10% · délai 16.1min · rebond 67% (32/52) (MFE +1.63%)
   - −5.0% : fill 30min 18% · séance 33% (43/159) · gap 6% · délai 19.2min · rebond 73% (29/43) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.64%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −3.11%) → stop au-delà de −1.63% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −3.25%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=836 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 94% (67/69) · rebond 48% (35/67)
      · −2.0% : fill 88% (60/69) · rebond 59% (33/60)
      · −3.0% : fill 82% (53/69) · rebond 56% (30/53)
      · −4.0% : fill 69% (42/69) · rebond 67% (26/42)
      · −5.0% : fill 57% (35/69) · rebond 71% (23/35)
   - **flat** (17 séances) :
      · −1.0% : fill 94% (15/17) · rebond 86% (11/15)
      · −2.0% : fill 45% (10/17) · rebond 78% (7/10)
      · −3.0% : fill 10% (2/17) · rebond 100% (2/2)
      · −4.0% : fill 3% (1/17) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/17) · rebond 0% (0/0)
   - **gap-up** (73 séances) :
      · −1.0% : fill 48% (33/73) · rebond 68% (18/33)
      · −2.0% : fill 30% (20/73) · rebond 74% (16/20)
      · −3.0% : fill 28% (16/73) · rebond 65% (10/16)
      · −4.0% : fill 18% (9/73) · rebond 65% (5/9)
      · −5.0% : fill 16% (8/73) · rebond 81% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 67% si les 15 1res min sont vertes (72 cas) · 23% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 75% si début vert vs 12% si rouge (base 44% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **75%** · continue >prix actuel 47% ; creux résiduel méd -1.67% (q20 -2.84%) → **SL/trailing à −2.84%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.97% → **scale +1.59% / runner +2.97%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **12%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.68%** (au-delà de la MAE q10 -5.68%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +4.68%] · haut q95 +5.72% · bas q05 -4.39%
   - 60min (n=160) : retour [-4.25% .. +5.1%] · haut q95 +6.36% · bas q05 -5.59%
   - 2h (n=160) : retour [-4.79% .. +6.65%] · haut q95 +7.25% · bas q05 -5.83%
   - 4h (n=160) : retour [-6.17% .. +7.42%] · haut q95 +8.38% · bas q05 -6.97%
   - 6h (n=160) : retour [-6.48% .. +6.99%] · haut q95 +8.85% · bas q05 -8.28%
   - session (n=160) : retour [-7.32% .. +7.91%] · haut q95 +9.31% · bas q05 -8.67%


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
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.0  _(survente)_
- **ADX** : 25.0  _(tendance etablie)_
- **MACD** : hist -0.267  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 42.2%
- **ATR** : 1.57 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.249  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 46.1  _(transition)_
- **MA** : MA20 28.45 · MA50 33.09 · MA200 33.94  _(prix < MA20)_
- **Dist MA** : MA20 -16.2% · MA50 -28.0% · MA200 -29.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87279 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
