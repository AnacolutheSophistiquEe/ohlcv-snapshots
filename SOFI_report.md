# SOFI

**Generated** : 2026-08-05T00:32:24.117265+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $18.70  

> 🟡 **WAIT-FOR-DIP** — spot +3.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $18.70 (+3.7% vs entrée) · entrée $18.04 · stop $17.69 · T1 $18.75 · R/R 2.03  
> ↳ P(T1 av. stop) 45 % · EV/risk 0.239 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.96% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -6108 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.95–$18.13 (mid $18.04)
- Spot actuel : $18.70 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $17.69 (stop swing_plan-based (-14.95%))
- Targets : T1 $18.75 · R/R 2.03 | T2 $19.05 · R/R 2.89 | T3 $19.34 · R/R 3.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.69


## Edge, scénarios & sizing

- EV/risk : -0.101 | EV/share : $-0.036 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 18 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.8 | bear 22.4 | side 60.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 280.0 (= 15 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.527% → cible +3.923% / stop −1.962%, p_fill 24%, n_eff≈9.2) : P(cible|rempli) **26%** · **EV/risk +0.140** (×p_fill ; si rempli +1.16% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→70% · +2.0%→49% · +3.0%→36% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.41% (p90 7.29%) · excursion haute méd. +1.9% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.073% vs midi 0.918% vs clôture 1.005% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 17% · trend ↑2%/↓0% ; spike-down 66% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.15 ; neutre — autocorr -0.021)_ ; drift intra méd. 0.419% ; recovery-V 22%
- **σ réalisé intraday** 3.008% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 59% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 17.7781 (VA 17.4159–17.9794 ; dernier close 18.03)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 51% · rebond 71% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.88% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 45% (gap-down >1% 27% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.76%) · haut méd +0.74% · range méd 1.68%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.98%) · haut méd +1.05% · range méd 2.37%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.33%) · haut méd +1.23% · range méd 2.85%
- Excursion ouverture 60min (n=160) : bas méd −1.48% (p90 −3.79%) · haut méd +1.33% · range méd 3.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.03 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (123/159) · gap 33% · délai 0.0min · rebond 51% (65/123) (MFE +1.07%)
   - −1.0% : fill 30min 54% · séance 67% (112/159) · gap 27% · délai 0.5min · rebond 61% (70/112) (MFE +1.23%)
   - −1.5% : fill 30min 49% · séance 63% (102/159) · gap 19% · délai 7.1min · rebond 66% (65/102) (MFE +1.58%)
   - −2.0% : fill 30min 39% · séance 51% (77/159) · gap 12% · délai 3.3min · rebond 71% (53/77) (MFE +1.88%)
   - −3.0% : fill 30min 18% · séance 39% (58/159) · gap 4% · délai 31.4min · rebond 66% (40/58) (MFE +1.57%)
   - −4.0% : fill 30min 11% · séance 23% (39/159) · gap 3% · délai 41.0min · rebond 57% (25/39) (MFE +1.46%)
   - −5.0% : fill 30min 5% · séance 9% (18/159) · gap 2% · délai 26.7min · rebond 40% (10/18) (MFE +0.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.05%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.71%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −1.81%) → stop au-delà de −1.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=660 jambes) : jambe baissière méd −1.12% (p90 −2.8%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 97% (65/66) · rebond 60% (41/65)
      · −2.0% : fill 85% (54/66) · rebond 71% (39/54)
      · −3.0% : fill 71% (44/66) · rebond 73% (33/44)
      · −4.0% : fill 42% (29/66) · rebond 65% (21/29)
      · −5.0% : fill 20% (14/66) · rebond 38% (8/14)
   - **flat** (24 séances) :
      · −1.0% : fill 54% (14/24) · rebond 46% (7/14)
      · −2.0% : fill 39% (8/24) · rebond 58% (4/8)
      · −3.0% : fill 34% (6/24) · rebond 57% (3/6)
      · −4.0% : fill 14% (3/24) · rebond 67% (1/3)
      · −5.0% : fill 1% (1/24) · rebond 0% (0/1)
   - **gap-up** (69 séances) :
      · −1.0% : fill 44% (33/69) · rebond 67% (22/33)
      · −2.0% : fill 24% (15/69) · rebond 78% (10/15)
      · −3.0% : fill 12% (8/69) · rebond 39% (4/8)
      · −4.0% : fill 9% (7/69) · rebond 20% (3/7)
      · −5.0% : fill 2% (3/69) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 56% si les 15 1res min sont vertes (73 cas) · 30% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 77% si début vert vs 13% si rouge (base 43% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **77%** · continue >prix actuel 56% ; creux résiduel méd -1.51% (q20 -3.3%) → **SL/trailing à −3.3%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.9% / q75 +2.95% → **scale +1.9% / runner +2.95%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **13%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.14%** (au-delà de la MAE q10 -3.14%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.91% .. +3.69%] · haut q95 +4.01% · bas q05 -3.56%
   - 60min (n=160) : retour [-3.13% .. +3.68%] · haut q95 +4.5% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.9%] · haut q95 +5.22% · bas q05 -4.62%
   - 4h (n=160) : retour [-3.84% .. +4.97%] · haut q95 +5.79% · bas q05 -5.06%
   - 6h (n=160) : retour [-4.61% .. +5.09%] · haut q95 +6.69% · bas q05 -5.08%
   - session (n=160) : retour [-4.54% .. +5.81%] · haut q95 +6.81% · bas q05 -5.18%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.9  _(neutre)_
- **ADX** : 16.0  _(pas de tendance nette)_
- **MACD** : hist 0.092  _(bullish_recent)_
- **BB** : %B 0.85 · largeur 21.7%
- **ATR** : 0.9 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.036  _(neutre)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 45.3  _(transition)_
- **MA** : MA20 17.37 · MA50 17.3 · MA200 21.22  _(prix > MA20)_
- **Dist MA** : MA20 +7.6% · MA50 +8.1% · MA200 -11.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85829 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
