# AL2SI

**Generated** : 2026-06-24T00:08:29.296108+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €27.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €27.70 (+15.3% vs entrée) · entrée €24.02 · stop €22.10 · T1 €25.99 · R/R 1.03  
> ↳ P(T1 av. stop) 21 % · EV/risk -0.014 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €23.72–€24.32 (mid €24.02)
- Spot actuel : €27.70 (+15.3% au-dessus de la zone — repli à attendre)
- Stop : €22.10 (stop swing_plan-based (-36.19%))
- Targets : T1 €25.99 · R/R 1.03 | T2 €27.97 · R/R 2.06 | T3 €29.94 · R/R 3.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.10


## Edge, scénarios & sizing

- EV/risk : -0.014 | EV/share : €-0.027 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 3 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 25.0 | bear 46.6 | side 28.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 138.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→79% · +2.0%→75% · +3.0%→64% · +5.0%→40% · +8.0%→20%
- Range intraday médian 7.78% (p90 13.46%) · excursion haute méd. +3.92% / basse méd. −3.43%
- Profil de vol intra : ouverture 5.218% vs midi 1.539% vs clôture 1.821% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (132 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.167 ; neutre — autocorr -0.028)_ ; drift intra méd. 0.038% ; recovery-V 34%
- **σ réalisé intraday** 7.447% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 65% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 20.2904 (VA 16.5149–22.1781 ; dernier close 22.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 86% · **stop −5.48%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.46 (high win-rate)
- Gaps overnight (n=131) : méd. 0.12% · baisse 44% (gap-down >1% 27% · >2% 10%)
- Excursion ouverture 5min (n=132) : bas méd −0.86% (p90 −4.34%) · haut méd +0.9% · range méd 2.51%
- Excursion ouverture 15min (n=132) : bas méd −1.32% (p90 −5.16%) · haut méd +1.4% · range méd 3.21%
- Excursion ouverture 30min (n=132) : bas méd −1.39% (p90 −5.65%) · haut méd +1.57% · range méd 3.95%
- Excursion ouverture 60min (n=132) : bas méd −1.93% (p90 −6.62%) · haut méd +2.25% · range méd 4.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 22.56 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 78% (100/131) · gap 33% · délai 0.1min · rebond 64% (65/100) (MFE +2.65%)
   - −1.0% : fill 30min 61% · séance 75% (95/131) · gap 27% · délai 0.3min · rebond 66% (64/95) (MFE +2.49%)
   - −1.5% : fill 30min 52% · séance 70% (86/131) · gap 16% · délai 1.3min · rebond 66% (55/86) (MFE +1.75%)
   - −2.0% : fill 30min 43% · séance 58% (73/131) · gap 10% · délai 2.8min · rebond 66% (48/73) (MFE +1.64%)
   - −3.0% : fill 30min 29% · séance 52% (60/131) · gap 7% · délai 10.9min · rebond 80% (49/60) (MFE +2.22%)
   - −4.0% : fill 30min 22% · séance 43% (50/131) · gap 7% · délai 20.5min · rebond 76% (39/50) (MFE +2.67%)
   - −5.0% : fill 30min 19% · séance 38% (43/131) · gap 6% · délai 27.7min · rebond 86% (40/43) (MFE +2.53%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −4.87%) → stop au-delà de −2.35% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −4.82%) → stop au-delà de −2.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −4.72%) → stop au-delà de −2.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1228 jambes) : jambe baissière méd −1.19% (p90 −2.91%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (45/49) · rebond 66% (30/45)
      · −2.0% : fill 84% (38/49) · rebond 52% (23/38)
      · −3.0% : fill 81% (34/49) · rebond 74% (27/34)
      · −4.0% : fill 67% (29/49) · rebond 68% (23/29)
      · −5.0% : fill 63% (27/49) · rebond 77% (24/27)
   - **flat** (27 séances) :
      · −1.0% : fill 76% (20/27) · rebond 71% (15/20)
      · −2.0% : fill 53% (14/27) · rebond 79% (10/14)
      · −3.0% : fill 35% (9/27) · rebond 87% (8/9)
      · −4.0% : fill 35% (9/27) · rebond 91% (8/9)
      · −5.0% : fill 25% (7/27) · rebond 100% (7/7)
   - **gap-up** (55 séances) :
      · −1.0% : fill 53% (30/55) · rebond 62% (19/30)
      · −2.0% : fill 38% (21/55) · rebond 83% (15/21)
      · −3.0% : fill 33% (17/55) · rebond 92% (14/17)
      · −4.0% : fill 23% (12/55) · rebond 85% (8/12)
      · −5.0% : fill 22% (9/55) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=132) : 52% en base · 69% si les 15 1res min sont vertes (63 cas) · 39% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=132) : retour [-4.01% .. +6.19%] · haut q95 +8.23% · bas q05 -6.92%
   - 60min (n=132) : retour [-5.9% .. +9.04%] · haut q95 +9.61% · bas q05 -7.83%
   - session (n=132) : retour [-7.81% .. +10.97%] · haut q95 +14.7% · bas q05 -11.18%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.12 · part idiosyncratique 0.89
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.5  _(survente)_
- **ADX** : 30.5  _(tendance etablie)_
- **MACD** : hist -3.631  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 98.1%
- **ATR** : 6.44 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.027  _(neutre)_
- **Vol ratio** : 2.62  _(volume au-dessus de la moyenne)_
- **Choppiness** : 29.4  _(marche directionnel)_
- **MA** : MA20 45.89 · MA50 42.24 · MA200 22.11  _(prix < MA20)_
- **Dist MA** : MA20 -39.6% · MA50 -34.4% · MA200 +25.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (42571 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
