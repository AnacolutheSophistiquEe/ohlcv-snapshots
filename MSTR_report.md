# MSTR

**Generated** : 2026-06-24T00:12:26.712655+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $103.84  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $103.84 (+10.6% vs entrée) · entrée $93.86 · stop $90.86 · T1 $96.39 · R/R 0.84  
> ↳ P(T1 av. stop) 37 % · EV/risk -0.041 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -162 % hors [0,100] (R² max 0.04). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $93.35–$94.36 (mid $93.86)
- Spot actuel : $103.84 (+10.6% au-dessus de la zone — repli à attendre)
- Stop : $90.86 (stop swing_plan-based (-22.11%))
- Targets : T1 $96.39 · R/R 0.84 | T2 $98.92 · R/R 1.69 | T3 $101.46 · R/R 2.53
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $90.86


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : $-0.122 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 11 % | T3 2 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 7.7 | bear 81.5 | side 10.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→52% · +3.0%→31% · +5.0%→9% · +8.0%→4%
- Range intraday médian 5.12% (p90 8.46%) · excursion haute méd. +2.24% / basse méd. −2.89%
- Profil de vol intra : ouverture 3.011% vs midi 1.188% vs clôture 1.217% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.013)_ ; drift intra méd. -1.176% ; recovery-V 32%
- **σ réalisé intraday** 3.723% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 72% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 110.3259 (VA 107.5066–113.4584 ; dernier close 109.53)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 63% · **stop −4.62%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.17% · baisse 55% (gap-down >1% 38% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −2.06%) · haut méd +0.57% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −3.02%) · haut méd +0.81% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.48%) · haut méd +1.06% · range méd 2.98%
- Excursion ouverture 60min (n=160) : bas méd −1.8% (p90 −4.28%) · haut méd +1.46% · range méd 3.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 109.53 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 80% (127/159) · gap 46% · délai 0.0min · rebond 50% (64/127) (MFE +1.1%)
   - −1.0% : fill 30min 63% · séance 76% (122/159) · gap 38% · délai 0.0min · rebond 58% (70/122) (MFE +1.47%)
   - −1.5% : fill 30min 55% · séance 72% (114/159) · gap 28% · délai 0.0min · rebond 58% (69/114) (MFE +1.51%)
   - −2.0% : fill 30min 46% · séance 64% (102/159) · gap 22% · délai 1.6min · rebond 53% (64/102) (MFE +1.09%)
   - −3.0% : fill 30min 29% · séance 50% (78/159) · gap 15% · délai 12.6min · rebond 54% (48/78) (MFE +1.52%)
   - −4.0% : fill 30min 19% · séance 42% (64/159) · gap 6% · délai 39.8min · rebond 56% (40/64) (MFE +1.47%)
   - −5.0% : fill 30min 14% · séance 32% (49/159) · gap 3% · délai 71.3min · rebond 63% (34/49) (MFE +1.56%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −2.81%) → stop au-delà de −1.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.1% (p90 −2.84%) → stop au-delà de −2.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.19% (p90 −2.83%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=958 jambes) : jambe baissière méd −1.21% (p90 −2.76%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 50% (38/73)
      · −2.0% : fill 87% (66/74) · rebond 49% (39/66)
      · −3.0% : fill 76% (57/74) · rebond 53% (35/57)
      · −4.0% : fill 63% (47/74) · rebond 56% (31/47)
      · −5.0% : fill 52% (39/74) · rebond 66% (28/39)
   - **flat** (17 séances) :
      · −1.0% : fill 86% (16/17) · rebond 77% (10/16)
      · −2.0% : fill 64% (13/17) · rebond 55% (9/13)
      · −3.0% : fill 44% (9/17) · rebond 36% (5/9)
      · −4.0% : fill 41% (7/17) · rebond 12% (2/7)
      · −5.0% : fill 32% (5/17) · rebond 15% (2/5)
   - **gap-up** (68 séances) :
      · −1.0% : fill 47% (33/68) · rebond 68% (22/33)
      · −2.0% : fill 35% (23/68) · rebond 66% (16/23)
      · −3.0% : fill 22% (12/68) · rebond 68% (8/12)
      · −4.0% : fill 19% (10/68) · rebond 84% (7/10)
      · −5.0% : fill 7% (5/68) · rebond 88% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 49% si les 15 1res min sont vertes (71 cas) · 37% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.76% .. +2.76%] · haut q95 +3.74% · bas q05 -4.13%
   - 60min (n=160) : retour [-4.92% .. +3.33%] · haut q95 +4.1% · bas q05 -5.33%
   - session (n=160) : retour [-5.75% .. +5.22%] · haut q95 +7.95% · bas q05 -8.15%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.6 · part idiosyncratique 0.4
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.6  _(momentum baissier)_
- **ADX** : 27.3  _(tendance etablie)_
- **MACD** : hist -1.523  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 52.6%
- **ATR** : 9.98 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.249  _(distribution)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 52.8  _(transition)_
- **MA** : MA20 129.36 · MA50 153.58 · MA200 189.62  _(prix < MA20)_
- **Dist MA** : MA20 -19.7% · MA50 -32.4% · MA200 -45.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (40087 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
