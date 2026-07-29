# AL2SI

**Generated** : 2026-07-29T00:10:16.815767+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €25.74  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €25.74 (+7.2% vs entrée) · entrée €24.01 · stop €22.93 · T1 €26.18 · R/R 2.01  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.224 _(réel 5 s)_ (GBM 0.287) · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €23.58–€24.45 (mid €24.01)
- Spot actuel : €25.74 (+7.2% au-dessus de la zone — repli à attendre)
- Stop : €22.93 (stop swing_plan-based (-10.91%))
- Targets : T1 €26.18 · R/R 2.01 | T2 €28.34 · R/R 4.01 | T3 €30.50 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.93


## Edge, scénarios & sizing

- EV/risk : 0.287 | EV/share : €0.310 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 18 % | T3 12 %
- Kelly (position) : f* 0.05 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 24.9 | bear 69.7 | side 5.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.045% → cible +4.028% / stop −3.986%, p_fill 77%, n_eff≈28.9) : P(cible|rempli) **34%** · **EV/risk -0.081** (×p_fill ; si rempli -0.42% du capital)
  - **swing** (entrée dip −6.709% → cible +9.006% / stop −4.503%, p_fill 54%, n_eff≈21.2) : P(cible|rempli) **23%** · **EV/risk -0.224** (×p_fill ; si rempli -1.86% du capital)
  - **deep** (entrée dip −10.372% → cible +12.736% / stop −6.368%, p_fill 60%, n_eff≈19.8) : P(cible|rempli) **5%** · **EV/risk -0.552** (×p_fill ; si rempli -5.88% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→74% · +3.0%→64% · +5.0%→46% · +8.0%→24%
- Range intraday médian 8.95% (p90 22.19%) · excursion haute méd. +4.37% / basse méd. −3.94%
- Profil de vol intra : ouverture 5.893% vs midi 1.751% vs clôture 2.012% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 8% · trend ↑0%/↓1% ; spike-down 79% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.054)_ ; drift intra méd. -0.208% ; recovery-V 32%
- **σ réalisé intraday** 8.252% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 66% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 29.0207 (VA 28.0532–29.4078 ; dernier close 27.14)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 45% · rebond 89% · **stop −5.51%** sous le fill (sous le bruit) · cible +3.1% · R/R 0.56 (high win-rate)
- Gaps overnight (n=156) : méd. 0.23% · baisse 38% (gap-down >1% 21% · >2% 10%)
- Excursion ouverture 5min (n=157) : bas méd −1.25% (p90 −5.11%) · haut méd +1.08% · range méd 3.13%
- Excursion ouverture 15min (n=157) : bas méd −1.67% (p90 −5.79%) · haut méd +1.6% · range méd 4.48%
- Excursion ouverture 30min (n=157) : bas méd −1.75% (p90 −5.86%) · haut méd +2.37% · range méd 4.97%
- Excursion ouverture 60min (n=157) : bas méd −2.34% (p90 −6.92%) · haut méd +2.83% · range méd 6.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.14 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 84% (123/156) · gap 28% · délai 0.3min · rebond 70% (83/123) (MFE +3.36%)
   - −1.0% : fill 30min 61% · séance 82% (118/156) · gap 21% · délai 0.4min · rebond 73% (83/118) (MFE +2.82%)
   - −1.5% : fill 30min 54% · séance 77% (108/156) · gap 15% · délai 1.1min · rebond 74% (73/108) (MFE +2.58%)
   - −2.0% : fill 30min 47% · séance 70% (95/156) · gap 10% · délai 3.4min · rebond 66% (63/95) (MFE +1.9%)
   - −3.0% : fill 30min 35% · séance 59% (77/156) · gap 6% · délai 8.1min · rebond 87% (65/77) (MFE +2.34%)
   - −4.0% : fill 30min 27% · séance 49% (65/156) · gap 4% · délai 22.1min · rebond 75% (50/65) (MFE +2.72%)
   - −5.0% : fill 30min 19% · séance 45% (57/156) · gap 4% · délai 64.4min · rebond 89% (53/57) (MFE +3.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −5.52%) → stop au-delà de −3.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.32% (p90 −5.53%) → stop au-delà de −3.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.25% (p90 −5.56%) → stop au-delà de −3.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1533 jambes) : jambe baissière méd −1.29% (p90 −3.61%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 98% (50/54) · rebond 70% (34/50)
      · −2.0% : fill 88% (43/54) · rebond 60% (27/43)
      · −3.0% : fill 80% (38/54) · rebond 80% (31/38)
      · −4.0% : fill 70% (33/54) · rebond 77% (27/33)
      · −5.0% : fill 63% (30/54) · rebond 83% (27/30)
   - **flat** (33 séances) :
      · −1.0% : fill 85% (26/33) · rebond 84% (21/26)
      · −2.0% : fill 71% (20/33) · rebond 81% (15/20)
      · −3.0% : fill 55% (14/33) · rebond 95% (13/14)
      · −4.0% : fill 47% (13/33) · rebond 81% (11/13)
      · −5.0% : fill 41% (11/33) · rebond 100% (11/11)
   - **gap-up** (69 séances) :
      · −1.0% : fill 69% (42/69) · rebond 69% (28/42)
      · −2.0% : fill 57% (32/69) · rebond 64% (21/32)
      · −3.0% : fill 45% (25/69) · rebond 91% (21/25)
      · −4.0% : fill 36% (19/69) · rebond 68% (12/19)
      · −5.0% : fill 35% (16/69) · rebond 89% (15/16)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 46% en base · 55% si les 15 1res min sont vertes (76 cas) · 38% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=157) : COUDE à **44min** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 46% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **72%** · continue >prix actuel 53% ; creux résiduel méd -2.63% (q20 -5.6%) → **SL/trailing à −5.6%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.24% / q75 +5.03% → **scale +3.24% / runner +5.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **21%** (continue à baisser 49%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.47%** (au-delà de la MAE q10 -10.47%), cible rebond +2.81% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-5.21% .. +6.42%] · haut q95 +8.33% · bas q05 -7.71%
   - 60min (n=157) : retour [-5.96% .. +9.2%] · haut q95 +9.84% · bas q05 -7.93%
   - 2h (n=157) : retour [-5.99% .. +9.98%] · haut q95 +11.07% · bas q05 -8.09%
   - 4h (n=157) : retour [-8.52% .. +10.1%] · haut q95 +12.37% · bas q05 -11.2%
   - 6h (n=157) : retour [-7.68% .. +14.25%] · haut q95 +15.63% · bas q05 -11.26%
   - session (n=157) : retour [-9.92% .. +14.99%] · haut q95 +16.95% · bas q05 -14.93%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.49%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.8  _(momentum baissier)_
- **ADX** : 24.5  _(pas de tendance nette)_
- **MACD** : hist 0.168  _(bullish_recent)_
- **BB** : %B 0.26 · largeur 62.5%
- **ATR** : 3.32 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.114  _(distribution)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 30.26 · MA50 37.9 · MA200 24.55  _(prix < MA20)_
- **Dist MA** : MA20 -14.9% · MA50 -32.1% · MA200 +4.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90761 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
