# SRT3

**Generated** : 2026-07-01T00:03:20.759914+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €227.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €227.70 (+1.0% vs entrée) · entrée €225.52 · stop €218.75 · T1 €228.62 · R/R 0.46  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.025 _(réel 5 s)_ (GBM 0.027) · ¼-Kelly 0.04 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €224.90–€226.14 (mid €225.52)
- Spot actuel : €227.70 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : €218.75 (stop swing_plan-based (-3.61%))
- Targets : T1 €228.62 · R/R 0.46 | T2 €231.72 · R/R 0.92 | T3 €234.82 · R/R 1.37
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €218.75


## Edge, scénarios & sizing

- EV/risk : 0.027 | EV/share : €0.182 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 62 % | T2 34 % | T3 12 %
- Kelly (position) : f* 0.161 | ¼-Kelly 0.04 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 68.5 | bear 12.3 | side 19.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.959% → cible +1.375% / stop −3.0%, p_fill 63%, n_eff≈26.5) : P(cible|rempli) **40%** · **EV/risk -0.025** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −2.105% → cible +3.074% / stop −1.537%, p_fill 62%, n_eff≈25.1) : P(cible|rempli) **50%** · **EV/risk +0.277** (×p_fill ; si rempli +0.69% du capital)
  - **deep** (entrée dip −3.257% → cible +4.347% / stop −2.174%, p_fill 61%, n_eff≈21.9) : P(cible|rempli) **30%** · **EV/risk -0.091** (×p_fill ; si rempli -0.32% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→71% · +2.0%→45% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.59%) · excursion haute méd. +1.84% / basse méd. −1.97%
- Profil de vol intra : ouverture 2.029% vs midi 0.891% vs clôture 1.025% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.014)_ ; drift intra méd. 0.004% ; recovery-V 23%
- **σ réalisé intraday** 2.456% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 65% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 229.0656 (VA 227.0344–229.8469 ; dernier close 226.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 59% · rebond 67% · **stop −2.61%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.32% (p90 −1.81%) · haut méd +0.48% · range méd 1.17%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.91%) · haut méd +0.66% · range méd 1.46%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.05%) · haut méd +0.74% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −2.46%) · haut méd +0.8% · range méd 1.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 226.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 75% (122/159) · gap 28% · délai 0.2min · rebond 50% (57/122) (MFE +1.0%)
   - −1.0% : fill 30min 42% · séance 62% (102/159) · gap 17% · délai 0.7min · rebond 56% (57/102) (MFE +1.15%)
   - −1.5% : fill 30min 33% · séance 59% (90/159) · gap 11% · délai 7.0min · rebond 67% (55/90) (MFE +1.56%)
   - −2.0% : fill 30min 22% · séance 43% (68/159) · gap 6% · délai 19.3min · rebond 59% (43/68) (MFE +1.34%)
   - −3.0% : fill 30min 7% · séance 24% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 13% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 8% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.12% (p90 −1.89%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.93%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.18% (p90 −2.2%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=414 jambes) : jambe baissière méd −1.04% (p90 −2.38%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 83% (62/75) · rebond 64% (39/62)
      · −2.0% : fill 61% (42/75) · rebond 62% (28/42)
      · −3.0% : fill 43% (29/75) · rebond 56% (17/29)
      · −4.0% : fill 23% (16/75) · rebond 71% (12/16)
      · −5.0% : fill 12% (7/75) · rebond 92% (6/7)
   - **flat** (36 séances) :
      · −1.0% : fill 59% (20/36) · rebond 40% (9/20)
      · −2.0% : fill 44% (14/36) · rebond 45% (7/14)
      · −3.0% : fill 19% (6/36) · rebond 49% (4/6)
      · −4.0% : fill 12% (3/36) · rebond 44% (2/3)
      · −5.0% : fill 12% (3/36) · rebond 44% (2/3)
   - **gap-up** (48 séances) :
      · −1.0% : fill 39% (20/48) · rebond 52% (9/20)
      · −2.0% : fill 19% (12/48) · rebond 72% (8/12)
      · −3.0% : fill 6% (5/48) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/48) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/48) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 60% si les 15 1res min sont vertes (89 cas) · 42% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:17** → P(séance verte=clôture>ouverture) 77% si début vert vs 30% si rouge (base 52% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **77%** · continue >prix actuel 52% ; creux résiduel méd -0.89% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.16% / q75 +2.49% → **scale +1.16% / runner +2.49%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **30%** (continue à baisser 49%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.07%** (au-delà de la MAE q10 -3.07%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.23% .. +2.12%] · haut q95 +2.65% · bas q05 -2.77%
   - 60min (n=160) : retour [-2.53% .. +2.32%] · haut q95 +2.82% · bas q05 -3.19%
   - 2h (n=160) : retour [-2.29% .. +2.62%] · haut q95 +3.11% · bas q05 -3.28%
   - 4h (n=160) : retour [-2.72% .. +2.72%] · haut q95 +3.3% · bas q05 -3.55%
   - 6h (n=160) : retour [-2.74% .. +3.52%] · haut q95 +4.03% · bas q05 -3.98%
   - session (n=160) : retour [-3.67% .. +4.74%] · haut q95 +5.64% · bas q05 -4.55%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.2%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.55
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.4  _(momentum baissier)_
- **ADX** : 13.7  _(pas de tendance nette)_
- **MACD** : hist -0.255  _(pas de croisement recent)_
- **BB** : %B 0.48 · largeur 18.0%
- **ATR** : 9.83 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.167  _(distribution)_
- **Vol ratio** : 0.28  _(volume atone)_
- **Choppiness** : 52.0  _(transition)_
- **MA** : MA20 228.67 · MA50 226.18 · MA200 229.15  _(prix < MA20)_
- **Dist MA** : MA20 -0.4% · MA50 +0.7% · MA200 -0.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92479 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
