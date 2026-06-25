# PLTR

**Generated** : 2026-06-25T00:15:28.139229+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $113.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot $113.50 (+5.6% vs entrée) · entrée $107.49 · stop $105.68 · T1 $110.02 · R/R 1.4  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.028 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -34 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 19.2 < 20 (tendance pas encore confirmée) alors que Choppiness 34.2 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $106.98–$107.99 (mid $107.49)
- Spot actuel : $113.50 (+5.6% au-dessus de la zone — repli à attendre)
- Stop : $105.68 (stop swing_plan-based (-12.96%))
- Targets : T1 $110.02 · R/R 1.4 | T2 $112.56 · R/R 2.8 | T3 $115.10 · R/R 4.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $105.68


## Edge, scénarios & sizing

- EV/risk : -0.028 | EV/share : $-0.051 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 5 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 18.9 | bear 70.9 | side 10.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→71% · +2.0%→38% · +3.0%→19% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.86% (p90 7.17%) · excursion haute méd. +1.75% / basse méd. −1.71%
- Profil de vol intra : ouverture 2.797% vs midi 0.727% vs clôture 0.804% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑0%/↓1% ; spike-down 57% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr 0.007)_ ; drift intra méd. -0.51% ; recovery-V 25%
- **σ réalisé intraday** 2.604% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 52% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 118.9219 (VA 117.5269–119.7356 ; dernier close 116.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 54% · **stop −3.03%** sous le fill (sous le bruit) · cible +1.07% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 57% (gap-down >1% 30% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.88% (p90 −1.97%) · haut méd +0.76% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.79%) · haut méd +0.97% · range méd 2.18%
- Excursion ouverture 30min (n=160) : bas méd −1.27% (p90 −3.42%) · haut méd +1.22% · range méd 2.56%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −3.83%) · haut méd +1.41% · range méd 3.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 116.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (118/159) · gap 42% · délai 0.0min · rebond 53% (64/118) (MFE +1.06%)
   - −1.0% : fill 30min 60% · séance 74% (110/159) · gap 30% · délai 0.0min · rebond 62% (65/110) (MFE +1.32%)
   - −1.5% : fill 30min 50% · séance 63% (92/159) · gap 20% · délai 1.5min · rebond 66% (58/92) (MFE +1.37%)
   - −2.0% : fill 30min 41% · séance 54% (77/159) · gap 15% · délai 5.4min · rebond 62% (49/77) (MFE +1.43%)
   - −3.0% : fill 30min 20% · séance 35% (56/159) · gap 5% · délai 21.2min · rebond 45% (27/56) (MFE +0.86%)
   - −4.0% : fill 30min 13% · séance 25% (40/159) · gap 4% · délai 29.9min · rebond 45% (20/40) (MFE +0.88%)
   - −5.0% : fill 30min 9% · séance 18% (27/159) · gap 3% · délai 30.4min · rebond 54% (14/27) (MFE +1.07%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.86%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.5%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −1.45%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=550 jambes) : jambe baissière méd −1.09% (p90 −2.68%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (65/68) · rebond 66% (41/65)
      · −2.0% : fill 80% (54/68) · rebond 63% (37/54)
      · −3.0% : fill 54% (39/68) · rebond 38% (20/39)
      · −4.0% : fill 42% (28/68) · rebond 41% (14/28)
      · −5.0% : fill 34% (20/68) · rebond 56% (10/20)
   - **flat** (33 séances) :
      · −1.0% : fill 83% (26/33) · rebond 42% (14/26)
      · −2.0% : fill 55% (13/33) · rebond 70% (8/13)
      · −3.0% : fill 43% (11/33) · rebond 75% (6/11)
      · −4.0% : fill 22% (8/33) · rebond 71% (5/8)
      · −5.0% : fill 5% (4/33) · rebond 63% (3/4)
   - **gap-up** (58 séances) :
      · −1.0% : fill 37% (19/58) · rebond 72% (10/19)
      · −2.0% : fill 17% (10/58) · rebond 42% (4/10)
      · −3.0% : fill 6% (6/58) · rebond 14% (1/6)
      · −4.0% : fill 4% (4/58) · rebond 18% (1/4)
      · −5.0% : fill 3% (3/58) · rebond 12% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 64% si les 15 1res min sont vertes (78 cas) · 32% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.07% .. +2.42%] · haut q95 +2.77% · bas q05 -4.31%
   - 60min (n=160) : retour [-3.53% .. +2.91%] · haut q95 +3.25% · bas q05 -4.46%
   - session (n=160) : retour [-4.99% .. +4.12%] · haut q95 +4.83% · bas q05 -5.88%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.63 · part idiosyncratique 0.37
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 18.6  _(survente)_
- **ADX** : 19.2  _(pas de tendance nette)_
- **MACD** : hist -2.343  _(pas de croisement recent)_
- **BB** : %B 0.06 · largeur 35.9%
- **ATR** : 6.01 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.098  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 34.2  _(marche directionnel)_
- **MA** : MA20 134.96 · MA50 137.61 · MA200 159.34  _(prix < MA20)_
- **Dist MA** : MA20 -15.9% · MA50 -17.5% · MA200 -28.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (41447 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
