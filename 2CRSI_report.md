# AL2SI

**Generated** : 2026-06-30T00:08:46.348850+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €31.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €31.20 (+0.8% vs entrée) · entrée €30.96 · stop €29.15 · T1 €33.02 · R/R 1.14  
> ↳ P(T1 av. stop) 8 % _(réel 5 s)_ · EV/risk -0.321 _(réel 5 s)_ (GBM 0.082) · ¼-Kelly 0.066 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.84% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €30.71–€31.20 (mid €30.96)
- Spot actuel : €31.20 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €29.15 (stop swing_plan-based (-8.73%))
- Targets : T1 €33.02 · R/R 1.14 | T2 €35.02 · R/R 2.24 | T3 €38.64 · R/R 4.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €29.15


## Edge, scénarios & sizing

- EV/risk : 0.082 | EV/share : €0.148 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 39 % | T3 39 %
- Kelly (position) : f* 0.266 | ¼-Kelly 0.066 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 24.1 | bear 48.5 | side 27.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.789% → cible +6.669% / stop −5.837%, p_fill 82%, n_eff≈32.6) : P(cible|rempli) **8%** · **EV/risk -0.321** (×p_fill ; si rempli -2.28% du capital)
  - **swing** (entrée dip −1.738% → cible +14.232% / stop −7.116%, p_fill 79%, n_eff≈29.9) : P(cible|rempli) **20%** · **EV/risk -0.254** (×p_fill ; si rempli -2.28% du capital)
  - **deep** (entrée dip −2.5% → cible +40.511% / stop −18.0%, p_fill 73%, n_eff≈27.8) : P(cible|rempli) **11%** · **EV/risk -0.174** (×p_fill ; si rempli -4.32% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→76% · +3.0%→65% · +5.0%→41% · +8.0%→21%
- Range intraday médian 7.78% (p90 14.23%) · excursion haute méd. +4.23% / basse méd. −3.18%
- Profil de vol intra : ouverture 5.381% vs midi 1.71% vs clôture 1.954% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.17 ; neutre — autocorr -0.01)_ ; drift intra méd. 0.206% ; recovery-V 34%
- **σ réalisé intraday** 8.652% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 67% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 26.1498 (VA 25.6073–27.5602 ; dernier close 27.94)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 39% · rebond 87% · **stop −6.52%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.39 (high win-rate)
- Gaps overnight (n=135) : méd. 0.21% · baisse 40% (gap-down >1% 25% · >2% 10%)
- Excursion ouverture 5min (n=136) : bas méd −0.9% (p90 −5.32%) · haut méd +1.01% · range méd 2.73%
- Excursion ouverture 15min (n=136) : bas méd −1.37% (p90 −6.01%) · haut méd +1.5% · range méd 3.39%
- Excursion ouverture 30min (n=136) : bas méd −1.51% (p90 −6.67%) · haut méd +1.69% · range méd 4.49%
- Excursion ouverture 60min (n=136) : bas méd −2.05% (p90 −7.31%) · haut méd +2.54% · range méd 5.42%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 77% (103/135) · gap 30% · délai 0.2min · rebond 64% (67/103) (MFE +2.42%)
   - −1.0% : fill 30min 58% · séance 75% (98/135) · gap 25% · délai 0.4min · rebond 69% (67/98) (MFE +2.06%)
   - −1.5% : fill 30min 50% · séance 70% (89/135) · gap 14% · délai 1.5min · rebond 64% (56/89) (MFE +1.73%)
   - −2.0% : fill 30min 42% · séance 60% (76/135) · gap 10% · délai 3.1min · rebond 63% (49/76) (MFE +1.35%)
   - −3.0% : fill 30min 29% · séance 52% (62/135) · gap 7% · délai 10.9min · rebond 78% (50/62) (MFE +2.22%)
   - −4.0% : fill 30min 22% · séance 43% (52/135) · gap 6% · délai 20.4min · rebond 74% (40/52) (MFE +2.67%)
   - −5.0% : fill 30min 20% · séance 39% (45/135) · gap 6% · délai 27.4min · rebond 87% (42/45) (MFE +2.53%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −5.86%) → stop au-delà de −3.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.82% (p90 −5.86%) → stop au-delà de −4.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −5.86%) → stop au-delà de −4.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1275 jambes) : jambe baissière méd −1.23% (p90 −3.26%) · ~19.0 jambes/séance
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
   - **gap-up** (58 séances) :
      · −1.0% : fill 55% (32/58) · rebond 68% (21/32)
      · −2.0% : fill 41% (23/58) · rebond 66% (15/23)
      · −3.0% : fill 33% (18/58) · rebond 80% (14/18)
      · −4.0% : fill 25% (13/58) · rebond 70% (8/13)
      · −5.0% : fill 23% (10/58) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 52% en base · 65% si les 15 1res min sont vertes (66 cas) · 42% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=136) : COUDE à **29min** → P(séance verte=clôture>ouverture) 78% si début vert vs 28% si rouge (base 52% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 209min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 59% ; creux résiduel méd -1.63% (q20 -4.37%) → **SL/trailing à −4.37%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.11% / q75 +6.03% → **scale +3.11% / runner +6.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=66) : edge inversé — récupère vert seulement **28%** (continue à baisser 60%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −9.36%** (au-delà de la MAE q10 -9.36%), cible rebond +1.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-4.93% .. +6.72%] · haut q95 +8.6% · bas q05 -7.73%
   - 60min (n=136) : retour [-5.63% .. +9.38%] · haut q95 +9.93% · bas q05 -8.11%
   - 2h (n=136) : retour [-5.27% .. +9.81%] · haut q95 +10.1% · bas q05 -8.23%
   - 4h (n=136) : retour [-8.54% .. +10.36%] · haut q95 +12.67% · bas q05 -11.22%
   - 6h (n=136) : retour [-8.2% .. +14.46%] · haut q95 +17.17% · bas q05 -11.29%
   - session (n=136) : retour [-10.0% .. +17.35%] · haut q95 +18.44% · bas q05 -15.52%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.16%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.27 · part idiosyncratique 0.73
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.0  _(survente)_
- **ADX** : 30.9  _(tendance etablie)_
- **MACD** : hist -1.864  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 124.5%
- **ATR** : 6.02 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.038  _(neutre)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 31.2  _(marche directionnel)_
- **MA** : MA20 41.09 · MA50 41.31 · MA200 22.5  _(prix < MA20)_
- **Dist MA** : MA20 -24.1% · MA50 -24.5% · MA200 +38.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94001 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
