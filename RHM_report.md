# RHM

**Generated** : 2026-07-21T21:35:42.466339+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €995.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €995.40 (+1.7% vs entrée) · entrée €978.75 · stop €959.17 · T1 €1008.08 · R/R 1.5  
> ↳ P(T1 av. stop) 17 % _(réel 5 s)_ · EV/risk -0.161 _(réel 5 s)_ (GBM 0.023) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €972.88–€984.62 (mid €978.75)
- Spot actuel : €995.40 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : €959.17 (stop swing_plan-based (-6.91%))
- Targets : T1 €1008.08 · R/R 1.5 | T2 €1037.41 · R/R 3.0 | T3 €1066.74 · R/R 4.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €959.17


## Edge, scénarios & sizing

- EV/risk : 0.023 | EV/share : €0.451 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 2 % | T3 2 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.7 | bear 5.0 | side 77.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.673% → cible +2.997% / stop −2.0%, p_fill 54%, n_eff≈21.3) : P(cible|rempli) **17%** · **EV/risk -0.161** (×p_fill ; si rempli -0.60% du capital)
  - **swing** (entrée dip −3.683% → cible +6.701% / stop −3.35%, p_fill 44%, n_eff≈15.0) : P(cible|rempli) **7%** · **EV/risk -0.201** (×p_fill ; si rempli -1.54% du capital)
  - **deep** (entrée dip −5.692% → cible +9.476% / stop −4.738%, p_fill 39%, n_eff≈14.2) : P(cible|rempli) **5%** · **EV/risk -0.275** (×p_fill ; si rempli -3.33% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→64% · +2.0%→48% · +3.0%→30% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.86%) · excursion haute méd. +1.85% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.551% vs midi 0.842% vs clôture 1.085% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.106 ; neutre — autocorr -0.013)_ ; drift intra méd. -0.339% ; recovery-V 45%
- **σ réalisé intraday** 2.831% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 68% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 986.1537 (VA 983.5412–988.2437 ; dernier close 991.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 61% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 46% (gap-down >1% 13% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −1.76%) · haut méd +0.5% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.02%) · haut méd +0.67% · range méd 1.97%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −2.75%) · haut méd +0.81% · range méd 2.21%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −3.03%) · haut méd +1.0% · range méd 2.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 991.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 80% (123/159) · gap 30% · délai 0.2min · rebond 57% (64/123) (MFE +1.24%)
   - −1.0% : fill 30min 51% · séance 73% (111/159) · gap 13% · délai 4.2min · rebond 61% (64/111) (MFE +1.39%)
   - −1.5% : fill 30min 33% · séance 58% (83/159) · gap 7% · délai 17.7min · rebond 51% (42/83) (MFE +1.14%)
   - −2.0% : fill 30min 23% · séance 48% (72/159) · gap 5% · délai 29.9min · rebond 61% (42/72) (MFE +1.31%)
   - −3.0% : fill 30min 11% · séance 32% (48/159) · gap 3% · délai 118.8min · rebond 60% (30/48) (MFE +1.31%)
   - −4.0% : fill 30min 5% · séance 23% (29/159) · gap 2% · délai 152.5min · rebond 61% (17/29) (MFE +1.45%)
   - −5.0% : fill 30min 2% · séance 11% (16/159) · gap 1% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −1.71%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −1.77%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.77%) → stop au-delà de −1.59% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.07% (p90 −2.57%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 94% (51/53) · rebond 62% (28/51)
      · −2.0% : fill 77% (40/53) · rebond 63% (25/40)
      · −3.0% : fill 50% (28/53) · rebond 59% (18/28)
      · −4.0% : fill 36% (16/53) · rebond 71% (11/16)
      · −5.0% : fill 17% (9/53) · rebond 77% (7/9)
   - **flat** (51 séances) :
      · −1.0% : fill 75% (37/51) · rebond 69% (24/37)
      · −2.0% : fill 32% (18/51) · rebond 71% (10/18)
      · −3.0% : fill 21% (11/51) · rebond 56% (6/11)
      · −4.0% : fill 19% (9/51) · rebond 38% (3/9)
      · −5.0% : fill 12% (6/51) · rebond 22% (1/6)
   - **gap-up** (55 séances) :
      · −1.0% : fill 48% (23/55) · rebond 49% (12/23)
      · −2.0% : fill 29% (14/55) · rebond 46% (7/14)
      · −3.0% : fill 23% (9/55) · rebond 66% (6/9)
      · −4.0% : fill 12% (4/55) · rebond 61% (3/4)
      · −5.0% : fill 5% (1/55) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 67% si les 15 1res min sont vertes (83 cas) · 33% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 75% si début vert vs 27% si rouge (base 50% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **75%** · continue >prix actuel 48% ; creux résiduel méd -1.25% (q20 -2.46%) → **SL/trailing à −2.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.25% / q75 +1.88% → **scale +1.25% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **27%** (continue à baisser 53%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.97%** (au-delà de la MAE q10 -4.97%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.65% .. +3.1%] · haut q95 +3.78% · bas q05 -3.21%
   - 60min (n=160) : retour [-3.46% .. +3.09%] · haut q95 +3.99% · bas q05 -4.03%
   - 2h (n=160) : retour [-3.6% .. +2.81%] · haut q95 +4.1% · bas q05 -4.69%
   - 4h (n=160) : retour [-3.83% .. +2.98%] · haut q95 +4.49% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.72% .. +3.26%] · haut q95 +4.53% · bas q05 -5.75%
   - session (n=160) : retour [-6.18% .. +4.18%] · haut q95 +4.74% · bas q05 -6.74%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.29%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.4  _(momentum baissier)_
- **ADX** : 28.4  _(tendance etablie)_
- **MACD** : hist 1.945  _(bullish_recent)_
- **BB** : %B 0.43 · largeur 23.4%
- **ATR** : 46.67 (6.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.041  _(neutre)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 43.0  _(transition)_
- **MA** : MA20 1011.98 · MA50 1123.9 · MA200 1490.83  _(prix < MA20)_
- **Dist MA** : MA20 -1.6% · MA50 -11.4% · MA200 -33.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90610 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
