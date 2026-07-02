# AL2SI

**Generated** : 2026-07-02T00:09:19.195865+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €37.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €37.20 (+1.5% vs entrée) · entrée €36.66 · stop €33.72 · T1 €42.74 · R/R 2.07  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.099 _(réel 5 s)_ (GBM 0.055) · ¼-Kelly 0.084 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €36.20–€37.11 (mid €36.66)
- Spot actuel : €37.20 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : €33.72 (stop swing_plan-based (-14.84%))
- Targets : T1 €42.74 · R/R 2.07 | T2 €44.47 · R/R 2.66 | T3 €46.19 · R/R 3.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €33.72


## Edge, scénarios & sizing

- EV/risk : 0.055 | EV/share : €0.161 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 39 % | T3 39 %
- Kelly (position) : f* 0.336 | ¼-Kelly 0.084 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.8 | bear 20.3 | side 60.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.467% → cible +16.61% / stop −8.0%, p_fill 78%, n_eff≈29.2) : P(cible|rempli) **3%** · **EV/risk -0.099** (×p_fill ; si rempli -1.02% du capital)
  - **swing** (entrée dip −3.227% → cible +39.565% / stop −12.0%, p_fill 63%, n_eff≈22.5) : P(cible|rempli) **7%** · **EV/risk -0.285** (×p_fill ; si rempli -5.44% du capital)
  - **deep** (entrée dip −4.975% → cible +69.604% / stop −18.0%, p_fill 61%, n_eff≈21.5) : P(cible|rempli) **0%** · **EV/risk -0.255** (×p_fill ; si rempli -7.54% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→75% · +3.0%→64% · +5.0%→40% · +8.0%→21%
- Range intraday médian 7.53% (p90 15.26%) · excursion haute méd. +4.16% / basse méd. −3.18%
- Profil de vol intra : ouverture 5.407% vs midi 1.696% vs clôture 1.922% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑0%/↓2% ; spike-down 72% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.164 ; neutre — autocorr -0.014)_ ; drift intra méd. 0.538% ; recovery-V 36%
- **σ réalisé intraday** 8.552% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 65% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 30.926 (VA 30.302–30.978 ; dernier close 30.34)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 88% · **stop −6.02%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.47 (high win-rate)
- Gaps overnight (n=137) : méd. 0.21% · baisse 39% (gap-down >1% 24% · >2% 9%)
- Excursion ouverture 5min (n=138) : bas méd −0.94% (p90 −5.57%) · haut méd +1.04% · range méd 2.98%
- Excursion ouverture 15min (n=138) : bas méd −1.37% (p90 −5.95%) · haut méd +1.5% · range méd 3.75%
- Excursion ouverture 30min (n=138) : bas méd −1.51% (p90 −6.63%) · haut méd +1.69% · range méd 4.59%
- Excursion ouverture 60min (n=138) : bas méd −2.05% (p90 −7.05%) · haut méd +2.54% · range méd 5.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 30.34 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 78% (105/137) · gap 29% · délai 0.2min · rebond 66% (69/105) (MFE +2.42%)
   - −1.0% : fill 30min 58% · séance 76% (100/137) · gap 24% · délai 0.4min · rebond 70% (69/100) (MFE +2.46%)
   - −1.5% : fill 30min 50% · séance 69% (90/137) · gap 14% · délai 1.3min · rebond 65% (57/90) (MFE +1.75%)
   - −2.0% : fill 30min 42% · séance 59% (77/137) · gap 9% · délai 2.8min · rebond 64% (50/77) (MFE +1.64%)
   - −3.0% : fill 30min 30% · séance 52% (63/137) · gap 6% · délai 10.5min · rebond 79% (51/63) (MFE +2.33%)
   - −4.0% : fill 30min 23% · séance 44% (53/137) · gap 6% · délai 15.0min · rebond 75% (41/53) (MFE +2.75%)
   - −5.0% : fill 30min 21% · séance 40% (46/137) · gap 5% · délai 18.8min · rebond 88% (43/46) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −5.86%) → stop au-delà de −3.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −5.86%) → stop au-delà de −4.29% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.75% (p90 −5.86%) → stop au-delà de −4.33% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1300 jambes) : jambe baissière méd −1.23% (p90 −3.28%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (45/49) · rebond 66% (30/45)
      · −2.0% : fill 84% (38/49) · rebond 52% (23/38)
      · −3.0% : fill 81% (34/49) · rebond 74% (27/34)
      · −4.0% : fill 67% (29/49) · rebond 68% (23/29)
      · −5.0% : fill 63% (27/49) · rebond 77% (24/27)
   - **flat** (29 séances) :
      · −1.0% : fill 80% (22/29) · rebond 77% (17/22)
      · −2.0% : fill 60% (16/29) · rebond 84% (12/16)
      · −3.0% : fill 46% (11/29) · rebond 92% (10/11)
      · −4.0% : fill 46% (11/29) · rebond 94% (10/11)
      · −5.0% : fill 37% (9/29) · rebond 100% (9/9)
   - **gap-up** (59 séances) :
      · −1.0% : fill 57% (33/59) · rebond 71% (22/33)
      · −2.0% : fill 40% (23/59) · rebond 66% (15/23)
      · −3.0% : fill 32% (18/59) · rebond 80% (14/18)
      · −4.0% : fill 24% (13/59) · rebond 70% (8/13)
      · −5.0% : fill 22% (10/59) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 52% en base · 66% si les 15 1res min sont vertes (67 cas) · 40% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=138) : COUDE à **31min** → P(séance verte=clôture>ouverture) 77% si début vert vs 28% si rouge (base 52% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 209min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **77%** · continue >prix actuel 58% ; creux résiduel méd -2.06% (q20 -4.49%) → **SL/trailing à −4.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.64% / q75 +5.92% → **scale +3.64% / runner +5.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=69) : edge inversé — récupère vert seulement **28%** (continue à baisser 56%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.69%** (au-delà de la MAE q10 -8.69%), cible rebond +2.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-4.91% .. +6.58%] · haut q95 +8.48% · bas q05 -7.71%
   - 60min (n=138) : retour [-5.48% .. +9.3%] · haut q95 +9.89% · bas q05 -7.97%
   - 2h (n=138) : retour [-5.26% .. +9.72%] · haut q95 +10.08% · bas q05 -8.12%
   - 4h (n=138) : retour [-8.23% .. +10.24%] · haut q95 +12.49% · bas q05 -11.03%
   - 6h (n=138) : retour [-7.74% .. +14.37%] · haut q95 +16.44% · bas q05 -11.26%
   - session (n=138) : retour [-9.93% .. +16.28%] · haut q95 +17.69% · bas q05 -15.05%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.17%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.26 · part idiosyncratique 0.74
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.0  _(momentum baissier)_
- **ADX** : 28.7  _(tendance etablie)_
- **MACD** : hist -0.484  _(pas de croisement recent)_
- **BB** : %B 0.47 · largeur 121.1%
- **ATR** : 6.04 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.009  _(neutre)_
- **Vol ratio** : 1.48  _(volume normal)_
- **Choppiness** : 32.9  _(marche directionnel)_
- **MA** : MA20 38.78 · MA50 41.06 · MA200 22.75  _(prix < MA20)_
- **Dist MA** : MA20 -4.1% · MA50 -9.4% · MA200 +63.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93221 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
