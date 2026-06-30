# AL2SI

**Generated** : 2026-06-30T21:43:27.284307+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €30.68  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €30.68 (+9.0% vs entrée) · entrée €28.15 · stop €26.44 · T1 €30.80 · R/R 1.55  
> ↳ P(T1 av. stop) 39 % · EV/risk 0.085 · ¼-Kelly 0.076 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −6.08% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €27.80–€28.50 (mid €28.15)
- Spot actuel : €30.68 (+9.0% au-dessus de la zone — repli à attendre)
- Stop : €26.44 (stop swing_plan-based (-27.95%))
- Targets : T1 €30.80 · R/R 1.55 | T2 €33.02 · R/R 2.85 | T3 €35.02 · R/R 4.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.44


## Edge, scénarios & sizing

- EV/risk : 0.085 | EV/share : €0.146 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 39 % | T3 39 %
- Kelly (position) : f* 0.305 | ¼-Kelly 0.076 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 21.3 | bear 41.7 | side 37.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→76% · +3.0%→65% · +5.0%→41% · +8.0%→22%
- Range intraday médian 7.78% (p90 15.26%) · excursion haute méd. +4.23% / basse méd. −3.06%
- Profil de vol intra : ouverture 5.378% vs midi 1.724% vs clôture 1.947% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑0%/↓2% ; spike-down 72% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.17 ; neutre — autocorr -0.013)_ ; drift intra méd. 0.714% ; recovery-V 38%
- **σ réalisé intraday** 8.651% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 68% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 29.879 (VA 27.653–30.833 ; dernier close 31.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 87% · **stop −6.52%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.39 (high win-rate)
- Gaps overnight (n=136) : méd. 0.21% · baisse 40% (gap-down >1% 24% · >2% 9%)
- Excursion ouverture 5min (n=137) : bas méd −0.91% (p90 −5.21%) · haut méd +1.03% · range méd 2.84%
- Excursion ouverture 15min (n=137) : bas méd −1.34% (p90 −5.98%) · haut méd +1.51% · range méd 3.4%
- Excursion ouverture 30min (n=137) : bas méd −1.48% (p90 −6.65%) · haut méd +1.79% · range méd 4.54%
- Excursion ouverture 60min (n=137) : bas méd −2.0% (p90 −7.18%) · haut méd +2.64% · range méd 5.47%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 31.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 78% (104/136) · gap 30% · délai 0.2min · rebond 65% (68/104) (MFE +2.66%)
   - −1.0% : fill 30min 57% · séance 75% (99/136) · gap 24% · délai 0.4min · rebond 70% (68/99) (MFE +2.52%)
   - −1.5% : fill 30min 49% · séance 69% (89/136) · gap 14% · délai 1.5min · rebond 64% (56/89) (MFE +1.73%)
   - −2.0% : fill 30min 41% · séance 59% (76/136) · gap 9% · délai 3.1min · rebond 63% (49/76) (MFE +1.35%)
   - −3.0% : fill 30min 28% · séance 51% (62/136) · gap 7% · délai 10.9min · rebond 78% (50/62) (MFE +2.22%)
   - −4.0% : fill 30min 22% · séance 42% (52/136) · gap 6% · délai 20.4min · rebond 74% (40/52) (MFE +2.67%)
   - −5.0% : fill 30min 19% · séance 38% (45/136) · gap 5% · délai 27.4min · rebond 87% (42/45) (MFE +2.53%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −5.86%) → stop au-delà de −3.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −5.86%) → stop au-delà de −4.29% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.75% (p90 −5.86%) → stop au-delà de −4.33% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1289 jambes) : jambe baissière méd −1.23% (p90 −3.25%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (45/49) · rebond 66% (30/45)
      · −2.0% : fill 84% (38/49) · rebond 52% (23/38)
      · −3.0% : fill 81% (34/49) · rebond 74% (27/34)
      · −4.0% : fill 67% (29/49) · rebond 68% (23/29)
      · −5.0% : fill 63% (27/49) · rebond 77% (24/27)
   - **flat** (28 séances) :
      · −1.0% : fill 78% (21/28) · rebond 74% (16/21)
      · −2.0% : fill 57% (15/28) · rebond 82% (11/15)
      · −3.0% : fill 41% (10/28) · rebond 90% (9/10)
      · −4.0% : fill 41% (10/28) · rebond 93% (9/10)
      · −5.0% : fill 31% (8/28) · rebond 100% (8/8)
   - **gap-up** (59 séances) :
      · −1.0% : fill 57% (33/59) · rebond 71% (22/33)
      · −2.0% : fill 40% (23/59) · rebond 66% (15/23)
      · −3.0% : fill 32% (18/59) · rebond 80% (14/18)
      · −4.0% : fill 24% (13/59) · rebond 70% (8/13)
      · −5.0% : fill 22% (10/59) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 53% en base · 66% si les 15 1res min sont vertes (67 cas) · 42% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=137) : COUDE à **31min** → P(séance verte=clôture>ouverture) 77% si début vert vs 29% si rouge (base 53% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 209min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **77%** · continue >prix actuel 58% ; creux résiduel méd -2.06% (q20 -4.49%) → **SL/trailing à −4.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.64% / q75 +5.92% → **scale +3.64% / runner +5.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=68) : edge inversé — récupère vert seulement **29%** (continue à baisser 58%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.86%** (au-delà de la MAE q10 -8.86%), cible rebond +2.14% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-4.92% .. +6.65%] · haut q95 +8.54% · bas q05 -7.72%
   - 60min (n=137) : retour [-5.55% .. +9.34%] · haut q95 +9.91% · bas q05 -8.04%
   - 2h (n=137) : retour [-5.27% .. +9.76%] · haut q95 +10.09% · bas q05 -8.18%
   - 4h (n=137) : retour [-8.39% .. +10.3%] · haut q95 +12.58% · bas q05 -11.13%
   - 6h (n=137) : retour [-7.96% .. +14.41%] · haut q95 +16.81% · bas q05 -11.28%
   - session (n=137) : retour [-9.97% .. +16.82%] · haut q95 +18.06% · bas q05 -15.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.16%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.26 · part idiosyncratique 0.74
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.4  _(survente)_
- **ADX** : 30.5  _(tendance etablie)_
- **MACD** : hist -1.34  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 124.1%
- **ATR** : 5.7 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.04  _(neutre)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 30.7  _(marche directionnel)_
- **MA** : MA20 39.69 · MA50 41.13 · MA200 22.61  _(prix < MA20)_
- **Dist MA** : MA20 -22.7% · MA50 -25.4% · MA200 +35.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92456 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
