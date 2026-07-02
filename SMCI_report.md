# SMCI

**Generated** : 2026-07-02T21:49:43.359720+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $27.22  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $27.22 (+1.6% vs entrée) · entrée $26.78 · stop $25.43 · T1 $29.48 · R/R 2.0  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.154 _(réel 5 s)_ (GBM 0.053) · ¼-Kelly 0.058 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.05% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $26.49–$27.07 (mid $26.78)
- Spot actuel : $27.22 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : $25.43 (stop swing_plan-based (-15.13%))
- Targets : T1 $29.48 · R/R 2.0 | T2 $30.28 · R/R 2.59 | T3 $31.08 · R/R 3.19
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $25.43


## Edge, scénarios & sizing

- EV/risk : 0.053 | EV/share : $0.072 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.233 | ¼-Kelly 0.058 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.3 | bear 33.6 | side 55.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.613% → cible +10.096% / stop −5.048%, p_fill 63%, n_eff≈25.3) : P(cible|rempli) **4%** · **EV/risk -0.154** (×p_fill ; si rempli -1.24% du capital)
  - **swing** (entrée dip −3.557% → cible +33.349% / stop −12.0%, p_fill 59%, n_eff≈22.1) : P(cible|rempli) **3%** · **EV/risk -0.167** (×p_fill ; si rempli -3.38% du capital)
  - **deep** (entrée dip −5.495% → cible +16.941% / stop −8.471%, p_fill 57%, n_eff≈20.8) : P(cible|rempli) **47%** · **EV/risk +0.207** (×p_fill ; si rempli +3.05% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→65% · +3.0%→45% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.17% (p90 11.21%) · excursion haute méd. +2.75% / basse méd. −2.54%
- Profil de vol intra : ouverture 3.771% vs midi 1.267% vs clôture 1.478% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑0%/↓1% ; spike-down 66% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.153 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. -0.171% ; recovery-V 26%
- **σ réalisé intraday** 4.518% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 64% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 28.2131 (VA 27.8969–28.2706 ; dernier close 27.65)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 66% · **stop −4.79%** sous le fill (sous le bruit) · cible +1.94% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 46% (gap-down >1% 32% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.82% (p90 −2.41%) · haut méd +0.91% · range méd 1.94%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.28%) · haut méd +1.21% · range méd 2.61%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.97%) · haut méd +1.38% · range méd 3.47%
- Excursion ouverture 60min (n=160) : bas méd −1.62% (p90 −4.46%) · haut méd +1.68% · range méd 4.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.65 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 75% (125/159) · gap 42% · délai 0.0min · rebond 56% (72/125) (MFE +1.19%)
   - −1.0% : fill 30min 60% · séance 69% (112/159) · gap 32% · délai 0.0min · rebond 58% (63/112) (MFE +1.22%)
   - −1.5% : fill 30min 51% · séance 64% (97/159) · gap 27% · délai 0.2min · rebond 64% (59/97) (MFE +1.45%)
   - −2.0% : fill 30min 46% · séance 58% (87/159) · gap 22% · délai 1.1min · rebond 67% (55/87) (MFE +1.8%)
   - −3.0% : fill 30min 28% · séance 50% (67/159) · gap 17% · délai 10.7min · rebond 57% (39/67) (MFE +1.8%)
   - −4.0% : fill 30min 22% · séance 41% (49/159) · gap 12% · délai 15.0min · rebond 65% (30/49) (MFE +1.48%)
   - −5.0% : fill 30min 18% · séance 33% (40/159) · gap 8% · délai 15.7min · rebond 66% (26/40) (MFE +1.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.45%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.84%) → stop au-delà de −1.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −2.75%) → stop au-delà de −1.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=818 jambes) : jambe baissière méd −1.22% (p90 −2.76%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (67/68) · rebond 53% (37/67)
      · −2.0% : fill 89% (59/68) · rebond 56% (32/59)
      · −3.0% : fill 82% (51/68) · rebond 57% (29/51)
      · −4.0% : fill 70% (40/68) · rebond 68% (25/40)
      · −5.0% : fill 55% (33/68) · rebond 63% (21/33)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (14/16) · rebond 81% (10/14)
      · −2.0% : fill 60% (10/16) · rebond 78% (7/10)
      · −3.0% : fill 13% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 40% (31/75) · rebond 62% (16/31)
      · −2.0% : fill 29% (18/75) · rebond 96% (16/18)
      · −3.0% : fill 25% (14/75) · rebond 54% (8/14)
      · −4.0% : fill 18% (8/75) · rebond 56% (4/8)
      · −5.0% : fill 16% (7/75) · rebond 75% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 74% si les 15 1res min sont vertes (71 cas) · 28% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 80% si début vert vs 21% si rouge (base 49% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **80%** · continue >prix actuel 55% ; creux résiduel méd -1.22% (q20 -3.2%) → **SL/trailing à −3.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.07% / q75 +3.42% → **scale +2.07% / runner +3.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **21%** (continue à baisser 59%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.41%** (au-delà de la MAE q10 -6.41%), cible rebond +1.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.2% .. +4.68%] · haut q95 +6.23% · bas q05 -4.52%
   - 60min (n=160) : retour [-4.48% .. +5.44%] · haut q95 +6.59% · bas q05 -5.81%
   - 2h (n=160) : retour [-5.01% .. +6.65%] · haut q95 +8.37% · bas q05 -5.85%
   - 4h (n=160) : retour [-6.76% .. +7.45%] · haut q95 +8.71% · bas q05 -7.86%
   - 6h (n=160) : retour [-6.82% .. +7.8%] · haut q95 +9.35% · bas q05 -9.52%
   - session (n=160) : retour [-8.59% .. +8.73%] · haut q95 +9.45% · bas q05 -9.84%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.83% / p90 2.16%) · ~4.0 replis/séance, durée méd 39.36 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.85 min, n=40)
   - −1.0% → **72%** (reprise méd 30.0 min, n=18)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.16%** (p90, défaut prudent ; serré/agressif −1.83%) ; extension open→close méd +7.84% (q75 +8.65% / q95 +9.89%), MFE méd +8.72% / q90 +10.35%
   - Échelle scale-out : +8.72% (33%) / +9.18% (33%) / +10.35% (34%)
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.55
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.8  _(momentum baissier)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist -0.753  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 70.0%
- **ATR** : 2.56 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.149  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 48.0  _(transition)_
- **MA** : MA20 32.96 · MA50 33.46 · MA200 35.02  _(prix < MA20)_
- **Dist MA** : MA20 -17.4% · MA50 -18.7% · MA200 -22.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90396 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
