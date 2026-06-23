# PLTR

**Generated** : 2026-06-23T21:50:30.944610+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $116.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $116.70 (+5.8% vs entrée) · entrée $110.32 · stop $108.40 · T1 $112.91 · R/R 1.35  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.032 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -22 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 17.7 < 20 (tendance pas encore confirmée) alors que Choppiness 35.0 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $109.80–$110.84 (mid $110.32)
- Spot actuel : $116.70 (+5.8% au-dessus de la zone — repli à attendre)
- Stop : $108.40 (stop swing_plan-based (-13.28%))
- Targets : T1 $112.91 · R/R 1.35 | T2 $115.50 · R/R 2.7 | T3 $118.10 · R/R 4.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $108.40


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : $-0.061 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 5 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 18.7 | bear 70.4 | side 10.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→72% · +2.0%→39% · +3.0%→20% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.86% (p90 7.17%) · excursion haute méd. +1.79% / basse méd. −1.71%
- Profil de vol intra : ouverture 2.82% vs midi 0.732% vs clôture 0.812% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr 0.019)_ ; drift intra méd. -0.391% ; recovery-V 27%
- **σ réalisé intraday** 2.604% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 50% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 120.7865 (VA 119.3405–122.7145 ; dernier close 119.48)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 16.2  _(survente)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -2.011  _(pas de croisement recent)_
- **BB** : %B 0.06 · largeur 32.4%
- **ATR** : 6.38 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.059  _(distribution)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 35.0  _(marche directionnel)_
- **MA** : MA20 136.12 · MA50 137.99 · MA200 159.54  _(prix < MA20)_
- **Dist MA** : MA20 -14.3% · MA50 -15.4% · MA200 -26.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (25448 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
