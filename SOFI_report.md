# SOFI

**Generated** : 2026-07-27T00:30:24.925806+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.48  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $16.48 (+2.0% vs entrée) · entrée $16.16 · stop $15.85 · T1 $16.77 · R/R 1.97  
> ↳ P(T1 av. stop) 9 % _(réel 5 s)_ · EV/risk -0.003 _(réel 5 s)_ (GBM -0.086) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.89% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +5.1 % ≠ (strike 17.5 − spot 16.48)/spot = +6.2 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 125 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.11–$16.21 (mid $16.16)
- Spot actuel : $16.48 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $15.85 (stop swing_plan-based (-5.93%))
- Targets : T1 $16.77 · R/R 1.97 | T2 $16.84 · R/R 2.19 | T3 $16.91 · R/R 2.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.85


## Edge, scénarios & sizing

- EV/risk : -0.086 | EV/share : $-0.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 18 % | T2 15 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.0 | bear 18.0 | side 69.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.947% → cible +3.779% / stop −1.889%, p_fill 66%, n_eff≈25.2) : P(cible|rempli) **9%** · **EV/risk -0.003** (×p_fill ; si rempli -0.01% du capital)
  - **swing** (entrée dip −4.281% → cible +3.447% / stop −1.723%, p_fill 34%, n_eff≈12.3) : P(cible|rempli) **58%** · **EV/risk +0.236** (×p_fill ; si rempli +1.19% du capital)
  - **deep** (entrée dip −6.614% → cible +4.874% / stop −2.437%, p_fill 27%, n_eff≈8.3) : P(cible|rempli) **44%** · **EV/risk +0.080** (×p_fill ; si rempli +0.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→69% · +2.0%→48% · +3.0%→35% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.38% (p90 6.91%) · excursion haute méd. +1.89% / basse méd. −2.17%
- Profil de vol intra : ouverture 3.051% vs midi 0.909% vs clôture 0.993% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓0% ; spike-down 67% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; neutre — autocorr -0.016)_ ; drift intra méd. -0.3% ; recovery-V 21%
- **σ réalisé intraday** 2.912% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 62% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 16.5444 (VA 16.4341–16.6301 ; dernier close 16.48)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 51% · rebond 72% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.84% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 46% (gap-down >1% 26% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.7%) · haut méd +0.72% · range méd 1.68%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.93%) · haut méd +0.96% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.3%) · haut méd +1.15% · range méd 2.82%
- Excursion ouverture 60min (n=160) : bas méd −1.48% (p90 −3.72%) · haut méd +1.3% · range méd 3.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.48 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (122/159) · gap 33% · délai 0.0min · rebond 55% (66/122) (MFE +1.22%)
   - −1.0% : fill 30min 55% · séance 69% (111/159) · gap 26% · délai 1.0min · rebond 63% (70/111) (MFE +1.34%)
   - −1.5% : fill 30min 49% · séance 65% (101/159) · gap 17% · délai 9.0min · rebond 67% (65/101) (MFE +1.76%)
   - −2.0% : fill 30min 39% · séance 51% (75/159) · gap 11% · délai 4.6min · rebond 72% (51/75) (MFE +1.84%)
   - −3.0% : fill 30min 16% · séance 37% (56/159) · gap 2% · délai 36.8min · rebond 66% (39/56) (MFE +1.48%)
   - −4.0% : fill 30min 8% · séance 22% (38/159) · gap 1% · délai 56.0min · rebond 58% (24/38) (MFE +1.43%)
   - −5.0% : fill 30min 3% · séance 8% (18/159) · gap 1% · délai 58.2min · rebond 48% (10/18) (MFE +0.95%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.83%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −2.0%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −2.04%) → stop au-delà de −1.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=666 jambes) : jambe baissière méd −1.12% (p90 −2.78%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 97% (64/66) · rebond 66% (41/64)
      · −2.0% : fill 83% (52/66) · rebond 74% (38/52)
      · −3.0% : fill 68% (42/66) · rebond 76% (32/42)
      · −4.0% : fill 36% (27/66) · rebond 69% (20/27)
      · −5.0% : fill 18% (13/66) · rebond 47% (8/13)
   - **flat** (24 séances) :
      · −1.0% : fill 48% (14/24) · rebond 30% (7/14)
      · −2.0% : fill 31% (8/24) · rebond 36% (3/8)
      · −3.0% : fill 24% (6/24) · rebond 32% (3/6)
      · −4.0% : fill 17% (4/24) · rebond 64% (1/4)
      · −5.0% : fill 2% (2/24) · rebond 0% (0/2)
   - **gap-up** (69 séances) :
      · −1.0% : fill 50% (33/69) · rebond 67% (22/33)
      · −2.0% : fill 26% (15/69) · rebond 78% (10/15)
      · −3.0% : fill 13% (8/69) · rebond 39% (4/8)
      · −4.0% : fill 10% (7/69) · rebond 20% (3/7)
      · −5.0% : fill 2% (3/69) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 55% si les 15 1res min sont vertes (73 cas) · 29% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 79% si début vert vs 11% si rouge (base 42% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **79%** · continue >prix actuel 54% ; creux résiduel méd -1.52% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.87% / q75 +2.77% → **scale +1.87% / runner +2.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **11%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.38%** (au-delà de la MAE q10 -3.38%), cible rebond +1.09% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.93% .. +3.52%] · haut q95 +3.83% · bas q05 -3.54%
   - 60min (n=160) : retour [-3.18% .. +3.38%] · haut q95 +4.02% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.59% .. +3.63%] · haut q95 +4.59% · bas q05 -4.86%
   - 4h (n=160) : retour [-3.93% .. +4.3%] · haut q95 +5.63% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.63% .. +3.88%] · haut q95 +5.69% · bas q05 -5.11%
   - session (n=160) : retour [-4.56% .. +4.84%] · haut q95 +5.69% · bas q05 -5.35%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.2  _(momentum baissier)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist -0.218  _(pas de croisement recent)_
- **BB** : %B 0.0 · largeur 15.0%
- **ATR** : 0.83 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.093  _(distribution)_
- **Vol ratio** : 1.1  _(volume normal)_
- **Choppiness** : 46.4  _(transition)_
- **MA** : MA20 17.81 · MA50 17.12 · MA200 21.59  _(prix < MA20)_
- **Dist MA** : MA20 -7.5% · MA50 -3.7% · MA200 -23.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84046 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
