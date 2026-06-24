# PLTR

**Generated** : 2026-06-24T00:15:14.758505+00:00  
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
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑0%/↓1% ; spike-down 56% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr 0.019)_ ; drift intra méd. -0.391% ; recovery-V 27%
- **σ réalisé intraday** 2.604% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 50% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 120.7865 (VA 119.3405–122.7145 ; dernier close 119.48)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 55% · **stop −3.02%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 58% (gap-down >1% 31% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.87% (p90 −1.97%) · haut méd +0.83% · range méd 1.73%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −2.79%) · haut méd +1.0% · range méd 2.19%
- Excursion ouverture 30min (n=160) : bas méd −1.31% (p90 −3.49%) · haut méd +1.22% · range méd 2.61%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −3.83%) · haut méd +1.43% · range méd 3.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 119.48 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (118/159) · gap 43% · délai 0.0min · rebond 52% (63/118) (MFE +1.03%)
   - −1.0% : fill 30min 61% · séance 73% (110/159) · gap 31% · délai 0.0min · rebond 63% (65/110) (MFE +1.38%)
   - −1.5% : fill 30min 51% · séance 62% (92/159) · gap 20% · délai 1.4min · rebond 67% (58/92) (MFE +1.53%)
   - −2.0% : fill 30min 42% · séance 53% (77/159) · gap 15% · délai 4.6min · rebond 64% (49/77) (MFE +1.52%)
   - −3.0% : fill 30min 20% · séance 36% (57/159) · gap 5% · délai 21.0min · rebond 45% (28/57) (MFE +0.86%)
   - −4.0% : fill 30min 13% · séance 26% (41/159) · gap 4% · délai 30.4min · rebond 45% (20/41) (MFE +0.88%)
   - −5.0% : fill 30min 9% · séance 19% (28/159) · gap 3% · délai 31.5min · rebond 55% (15/28) (MFE +1.08%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.85%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.5%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −1.45%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=550 jambes) : jambe baissière méd −1.09% (p90 −2.69%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (65/68) · rebond 66% (41/65)
      · −2.0% : fill 80% (54/68) · rebond 63% (37/54)
      · −3.0% : fill 54% (39/68) · rebond 38% (20/39)
      · −4.0% : fill 42% (28/68) · rebond 41% (14/28)
      · −5.0% : fill 34% (20/68) · rebond 56% (10/20)
   - **flat** (34 séances) :
      · −1.0% : fill 83% (27/34) · rebond 41% (14/27)
      · −2.0% : fill 56% (14/34) · rebond 70% (8/14)
      · −3.0% : fill 43% (12/34) · rebond 76% (7/12)
      · −4.0% : fill 22% (9/34) · rebond 70% (5/9)
      · −5.0% : fill 6% (5/34) · rebond 67% (4/5)
   - **gap-up** (57 séances) :
      · −1.0% : fill 33% (18/57) · rebond 84% (10/18)
      · −2.0% : fill 12% (9/57) · rebond 61% (4/9)
      · −3.0% : fill 6% (6/57) · rebond 14% (1/6)
      · −4.0% : fill 4% (4/57) · rebond 18% (1/4)
      · −5.0% : fill 3% (3/57) · rebond 12% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 64% si les 15 1res min sont vertes (79 cas) · 33% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.07% .. +2.43%] · haut q95 +2.78% · bas q05 -4.33%
   - 60min (n=160) : retour [-3.54% .. +2.92%] · haut q95 +3.32% · bas q05 -4.46%
   - session (n=160) : retour [-4.99% .. +4.18%] · haut q95 +4.97% · bas q05 -5.92%


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (41500 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
