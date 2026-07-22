# SOFI

**Generated** : 2026-07-22T00:31:59.367692+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.64  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $17.64 (+2.3% vs entrée) · entrée $17.24 · stop $16.64 · T1 $17.50 · R/R 0.43  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.03 _(réel 5 s)_ (GBM 0.009) · ¼-Kelly 0.036 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -240 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.19–$17.30 (mid $17.24)
- Spot actuel : $17.64 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : $16.64 (stop swing_plan-based (-6.51%))
- Targets : T1 $17.50 · R/R 0.43 | T2 $17.75 · R/R 0.85 | T3 $18.00 · R/R 1.27
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.64


## Edge, scénarios & sizing

- EV/risk : 0.009 | EV/share : $0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 59 % | T2 39 % | T3 17 %
- Kelly (position) : f* 0.144 | ¼-Kelly 0.036 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.7 | bear 19.4 | side 67.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.239% → cible +1.457% / stop −3.5%, p_fill 53%, n_eff≈20.4) : P(cible|rempli) **40%** · **EV/risk -0.030** (×p_fill ; si rempli -0.20% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=15, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→70% · +2.0%→50% · +3.0%→38% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.55% (p90 6.91%) · excursion haute méd. +1.97% / basse méd. −2.15%
- Profil de vol intra : ouverture 3.075% vs midi 0.95% vs clôture 0.987% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑0%/↓0% ; spike-down 67% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr -0.007)_ ; drift intra méd. -0.247% ; recovery-V 26%
- **σ réalisé intraday** 3.07% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 59% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 17.0955 (VA 17.0405–17.2825 ; dernier close 17.03)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 51% · rebond 73% · **stop −2.97%** sous le fill (sous le bruit) · cible +2.03% · R/R 0.68 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 46% (gap-down >1% 24% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.76%) · haut méd +0.74% · range méd 1.72%
- Excursion ouverture 15min (n=160) : bas méd −1.02% (p90 −3.03%) · haut méd +1.11% · range méd 2.41%
- Excursion ouverture 30min (n=160) : bas méd −1.18% (p90 −3.33%) · haut méd +1.25% · range méd 2.87%
- Excursion ouverture 60min (n=160) : bas méd −1.47% (p90 −3.77%) · haut méd +1.44% · range méd 3.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.03 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (123/159) · gap 32% · délai 0.0min · rebond 57% (68/123) (MFE +1.27%)
   - −1.0% : fill 30min 53% · séance 69% (112/159) · gap 24% · délai 1.0min · rebond 66% (72/112) (MFE +1.37%)
   - −1.5% : fill 30min 47% · séance 64% (101/159) · gap 18% · délai 9.8min · rebond 66% (65/101) (MFE +1.8%)
   - −2.0% : fill 30min 39% · séance 51% (76/159) · gap 12% · délai 5.2min · rebond 73% (52/76) (MFE +2.03%)
   - −3.0% : fill 30min 18% · séance 36% (56/159) · gap 2% · délai 30.8min · rebond 63% (39/56) (MFE +1.49%)
   - −4.0% : fill 30min 9% · séance 24% (39/159) · gap 2% · délai 57.4min · rebond 58% (24/39) (MFE +1.41%)
   - −5.0% : fill 30min 3% · séance 9% (19/159) · gap 1% · délai 60.7min · rebond 47% (10/19) (MFE +0.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.9%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −2.05%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −2.08%) → stop au-delà de −1.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=671 jambes) : jambe baissière méd −1.1% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 96% (64/66) · rebond 72% (43/64)
      · −2.0% : fill 81% (51/66) · rebond 76% (38/51)
      · −3.0% : fill 64% (40/66) · rebond 73% (30/40)
      · −4.0% : fill 40% (27/66) · rebond 69% (20/27)
      · −5.0% : fill 19% (13/66) · rebond 47% (8/13)
   - **flat** (24 séances) :
      · −1.0% : fill 55% (15/24) · rebond 31% (8/15)
      · −2.0% : fill 36% (9/24) · rebond 37% (4/9)
      · −3.0% : fill 28% (7/24) · rebond 34% (4/7)
      · −4.0% : fill 20% (4/24) · rebond 64% (1/4)
      · −5.0% : fill 2% (2/24) · rebond 0% (0/2)
   - **gap-up** (69 séances) :
      · −1.0% : fill 48% (33/69) · rebond 64% (21/33)
      · −2.0% : fill 28% (16/69) · rebond 77% (10/16)
      · −3.0% : fill 14% (9/69) · rebond 40% (5/9)
      · −4.0% : fill 11% (8/69) · rebond 20% (3/8)
      · −5.0% : fill 2% (4/69) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 56% si les 15 1res min sont vertes (72 cas) · 32% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 78% si début vert vs 13% si rouge (base 43% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -1.55% (q20 -3.64%) → **SL/trailing à −3.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.78% → **scale +1.69% / runner +2.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **13%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.89%** (au-delà de la MAE q10 -3.89%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.94% .. +3.58%] · haut q95 +3.91% · bas q05 -3.58%
   - 60min (n=160) : retour [-3.21% .. +3.4%] · haut q95 +4.03% · bas q05 -4.01%
   - 2h (n=160) : retour [-3.7% .. +3.67%] · haut q95 +4.75% · bas q05 -4.97%
   - 4h (n=160) : retour [-4.01% .. +4.41%] · haut q95 +5.66% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.64% .. +3.94%] · haut q95 +5.69% · bas q05 -5.14%
   - session (n=160) : retour [-4.57% .. +4.92%] · haut q95 +5.69% · bas q05 -5.41%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.7  _(neutre)_
- **ADX** : 20.1  _(pas de tendance nette)_
- **MACD** : hist -0.149  _(pas de croisement recent)_
- **BB** : %B 0.38 · largeur 12.0%
- **ATR** : 0.93 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.05  _(neutre)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 52.4  _(transition)_
- **MA** : MA20 17.89 · MA50 17.07 · MA200 21.73  _(prix < MA20)_
- **Dist MA** : MA20 -1.4% · MA50 +3.3% · MA200 -18.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83845 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
