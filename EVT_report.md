# EVT

**Generated** : 2026-08-06T21:38:57.520700+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.43  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €3.43 (+4.3% vs entrée) · entrée €3.29 · stop €3.16 · T1 €3.55 · R/R 2.0  
> ↳ P(T1 av. stop) 20 % · EV/risk -0.204 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €3.24–€3.34 (mid €3.29)
- Spot actuel : €3.43 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : €3.16 (stop swing_plan-based (-7.98%))
- Targets : T1 €3.55 · R/R 2.0 | T2 €3.81 · R/R 4.0 | T3 €4.07 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.16


## Edge, scénarios & sizing

- EV/risk : -0.06 | EV/share : €-0.008 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 4 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 72.3 | bear 22.7 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.865% → cible +3.507% / stop −3.501%, p_fill 51%, n_eff≈19.3) : P(cible|rempli) **11%** · **EV/risk -0.007** (×p_fill ; si rempli -0.05% du capital)
  - **swing** (entrée dip −4.105% → cible +7.839% / stop −4.041%, p_fill 22%, n_eff≈10.3) : P(cible|rempli) **3%** · **EV/risk -0.120** (×p_fill ; si rempli -2.23% du capital)
  - **deep** (entrée dip −6.337% → cible +11.088% / stop −6.206%, p_fill 33%, n_eff≈14.1) : P(cible|rempli) **3%** · **EV/risk -0.155** (×p_fill ; si rempli -2.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→45% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 4.03% (p90 6.25%) · excursion haute méd. +1.74% / basse méd. −1.8%
- Profil de vol intra : ouverture 2.702% vs midi 1.213% vs clôture 1.209% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.075 ; mean-reverting — autocorr -0.141)_ ; drift intra méd. -0.435% ; recovery-V 30%
- **σ réalisé intraday** 3.327% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 69% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 3.4946 (VA 3.4811–3.5013 ; dernier close 3.452)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 71% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.59% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.06% · baisse 45% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −2.4%) · haut méd +0.56% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.84% (p90 −2.67%) · haut méd +0.83% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −2.77%) · haut méd +0.94% · range méd 2.08%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −3.01%) · haut méd +0.95% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.452 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 82% (132/159) · gap 28% · délai 0.2min · rebond 67% (86/132) (MFE +1.49%)
   - −1.0% : fill 30min 50% · séance 71% (117/159) · gap 20% · délai 0.6min · rebond 67% (75/117) (MFE +1.59%)
   - −1.5% : fill 30min 35% · séance 57% (98/159) · gap 14% · délai 2.7min · rebond 60% (62/98) (MFE +1.33%)
   - −2.0% : fill 30min 26% · séance 45% (78/159) · gap 9% · délai 14.8min · rebond 64% (51/78) (MFE +1.43%)
   - −3.0% : fill 30min 14% · séance 29% (54/159) · gap 5% · délai 31.1min · rebond 68% (40/54) (MFE +1.65%)
   - −4.0% : fill 30min 7% · séance 16% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 5% · séance 8% (17/159) · gap 1% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −2.45%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −1.89%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.63% (p90 −1.95%) → stop au-delà de −1.35% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=815 jambes) : jambe baissière méd −1.08% (p90 −2.32%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 95% (57/60) · rebond 71% (34/57)
      · −2.0% : fill 64% (42/60) · rebond 60% (26/42)
      · −3.0% : fill 38% (30/60) · rebond 68% (22/30)
      · −4.0% : fill 26% (20/60) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/60) · rebond 57% (9/13)
   - **flat** (41 séances) :
      · −1.0% : fill 79% (32/41) · rebond 68% (24/32)
      · −2.0% : fill 53% (19/41) · rebond 68% (13/19)
      · −3.0% : fill 40% (12/41) · rebond 73% (9/12)
      · −4.0% : fill 17% (5/41) · rebond 20% (1/5)
      · −5.0% : fill 8% (3/41) · rebond 27% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 43% (28/58) · rebond 59% (17/28)
      · −2.0% : fill 21% (17/58) · rebond 70% (12/17)
      · −3.0% : fill 12% (12/58) · rebond 57% (9/12)
      · −4.0% : fill 5% (5/58) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/58) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 63% si les 15 1res min sont vertes (75 cas) · 40% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 64% si début vert vs 39% si rouge (base 51% · écart 25 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **64%** · continue >prix actuel 46% ; creux résiduel méd -1.87% (q20 -3.05%) → **SL/trailing à −3.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +2.13% → **scale +1.31% / runner +2.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **39%** (continue à baisser 43%) → **RÉDUIRE ~61%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.5%** (au-delà de la MAE q10 -4.5%), cible rebond +2.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.44% .. +2.42%] · haut q95 +3.51% · bas q05 -3.42%
   - 60min (n=160) : retour [-3.08% .. +2.87%] · haut q95 +4.31% · bas q05 -3.51%
   - 2h (n=160) : retour [-3.48% .. +3.19%] · haut q95 +4.41% · bas q05 -4.24%
   - 4h (n=160) : retour [-2.88% .. +2.87%] · haut q95 +4.41% · bas q05 -4.3%
   - 6h (n=160) : retour [-3.33% .. +3.23%] · haut q95 +4.57% · bas q05 -5.21%
   - session (n=160) : retour [-4.16% .. +4.07%] · haut q95 +5.62% · bas q05 -5.64%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.0  _(neutre)_
- **ADX** : 41.1  _(tendance tres forte)_
- **MACD** : hist 0.022  _(bullish_recent)_
- **BB** : %B 0.37 · largeur 58.7%
- **ATR** : 0.13 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.029  _(neutre)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 70.5  _(marche en range (choppy))_
- **MA** : MA20 3.71 · MA50 4.43 · MA200 5.24  _(prix < MA20)_
- **Dist MA** : MA20 -7.4% · MA50 -22.5% · MA200 -34.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89474 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
