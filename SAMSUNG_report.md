# 005930

**Generated** : 2026-07-14T00:14:46.161679+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩254500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩254500.00 (+7.4% vs entrée) · entrée ₩236921.66 · stop ₩227693.44 · T1 ₩255378.10 · R/R 2.0  
> ↳ P(T1 av. stop) 40 % · EV/risk 0.615 · ¼-Kelly 0.029 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -63 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩233230.37–₩240612.95 (mid ₩236921.66)
- Spot actuel : ₩254500.00 (+7.4% au-dessus de la zone — repli à attendre)
- Stop : ₩227693.44 (stop swing_plan-based (-10.53%))
- Targets : T1 ₩255378.10 · R/R 2.0 | T2 ₩273834.55 · R/R 4.0 | T3 ₩292290.99 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩227693.44


## Edge, scénarios & sizing

- EV/risk : 0.615 | EV/share : ₩5671.226 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 14 % | T3 3 %
- Kelly (position) : f* 0.116 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 52.5 | bear 9.6 | side 37.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.1  _(momentum baissier)_
- **ADX** : 19.4  _(pas de tendance nette)_
- **MACD** : hist -9164.894  _(pas de croisement recent)_
- **BB** : %B -0.01 · largeur 39.5%
- **ATR** : 27821.43 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.056  _(distribution)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 48.1  _(transition)_
- **MA** : MA20 319200.0 · MA50 303990.0 · MA200 181980.08  _(prix < MA20)_
- **Dist MA** : MA20 -20.3% · MA50 -16.3% · MA200 +39.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17375 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
