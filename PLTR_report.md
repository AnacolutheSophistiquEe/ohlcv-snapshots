# PLTR

**Generated** : 2026-06-23T00:15:20.715029+00:00  
**Santé technique** : 1/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $119.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $119.50 (+6.1% vs entrée) · entrée $112.68 · stop $110.64 · T1 $115.32 · R/R 1.29  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.01 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 16.5 < 20 (tendance pas encore confirmée) alors que Choppiness 32.6 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $112.15–$113.21 (mid $112.68)
- Spot actuel : $119.50 (+6.1% au-dessus de la zone — repli à attendre)
- Stop : $110.64 (stop swing-based (4.84%))
- Targets : T1 $115.32 · R/R 1.29 | T2 $117.96 · R/R 2.59 | T3 $120.60 · R/R 3.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $110.64


## Edge, scénarios & sizing

- EV/risk : 0.01 | EV/share : $0.020 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 19 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 22.4 | bear 44.8 | side 32.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 160 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (trop peu de remplissages (13))
  - **swing** : indisponible (trop peu de remplissages (4))
  - **deep** : indisponible (trop peu de remplissages (2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→67% · +2.0%→38% · +3.0%→21% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.91% (p90 6.93%) · excursion haute méd. +1.55% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.684% vs midi 0.757% vs clôture 0.873% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.45
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 14.7  _(survente)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist -1.602  _(pas de croisement recent)_
- **BB** : %B 0.06 · largeur 29.2%
- **ATR** : 6.82 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.017  _(neutre)_
- **Vol ratio** : 1.34  _(volume normal)_
- **Choppiness** : 32.6  _(marche directionnel)_
- **MA** : MA20 137.13 · MA50 138.21 · MA200 159.73  _(prix < MA20)_
- **Dist MA** : MA20 -12.9% · MA50 -13.5% · MA200 -25.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (22877 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
