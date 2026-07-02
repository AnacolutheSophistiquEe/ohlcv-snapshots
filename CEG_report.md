# CEG

**Generated** : 2026-07-02T21:56:08.184637+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $239.25  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $239.25 (+4.6% vs entrée) · entrée $228.83 · stop $225.40 · T1 $231.91 · R/R 0.9  
> ↳ P(T1 av. stop) 50 % · EV/risk -0.076 · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 19.0 < 20 (tendance pas encore confirmée) alors que Choppiness 37.6 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $228.21–$229.45 (mid $228.83)
- Spot actuel : $239.25 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : $225.40 (stop swing_plan-based (-10.08%))
- Targets : T1 $231.91 · R/R 0.9 | T2 $234.99 · R/R 1.8 | T3 $238.08 · R/R 2.7
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $225.40


## Edge, scénarios & sizing

- EV/risk : -0.076 | EV/share : $-0.260 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 23 % | T3 11 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 75.8 | bear 5.9 | side 18.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→65% · +2.0%→35% · +3.0%→24% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.55% (p90 5.51%) · excursion haute méd. +1.49% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.544% vs midi 0.729% vs clôture 0.787% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. -0.67% ; recovery-V 16%
- **σ réalisé intraday** 2.446% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 66% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 233.2685 (VA 232.3025–234.7175 ; dernier close 236.45)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 50% · rebond 63% · **stop −3.25%** sous le fill (sous le bruit) · cible +1.1% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.12% · baisse 44% (gap-down >1% 22% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.74% (p90 −1.79%) · haut méd +0.76% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −0.87% (p90 −2.27%) · haut méd +0.95% · range méd 2.11%
- Excursion ouverture 30min (n=160) : bas méd −1.0% (p90 −3.08%) · haut méd +1.06% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.17% (p90 −3.39%) · haut méd +1.29% · range méd 2.75%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 236.45 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 74% (120/159) · gap 28% · délai 0.0min · rebond 43% (58/120) (MFE +0.88%)
   - −1.0% : fill 30min 53% · séance 66% (105/159) · gap 22% · délai 1.9min · rebond 50% (57/105) (MFE +0.98%)
   - −1.5% : fill 30min 42% · séance 59% (92/159) · gap 12% · délai 4.1min · rebond 50% (50/92) (MFE +1.01%)
   - −2.0% : fill 30min 33% · séance 50% (72/159) · gap 9% · délai 9.2min · rebond 63% (46/72) (MFE +1.1%)
   - −3.0% : fill 30min 14% · séance 29% (44/159) · gap 3% · délai 36.7min · rebond 39% (19/44) (MFE +0.74%)
   - −4.0% : fill 30min 6% · séance 19% (30/159) · gap 2% · délai 48.3min · rebond 38% (14/30) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 11% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.41%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.27% (p90 −1.2%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=477 jambes) : jambe baissière méd −1.09% (p90 −2.66%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 100% (55/55) · rebond 47% (33/55)
      · −2.0% : fill 87% (41/55) · rebond 61% (28/41)
      · −3.0% : fill 58% (26/55) · rebond 43% (11/26)
      · −4.0% : fill 42% (19/55) · rebond 34% (8/19)
      · −5.0% : fill 30% (15/55) · rebond 77% (11/15)
   - **flat** (37 séances) :
      · −1.0% : fill 67% (23/37) · rebond 39% (7/23)
      · −2.0% : fill 41% (14/37) · rebond 49% (6/14)
      · −3.0% : fill 28% (12/37) · rebond 31% (6/12)
      · −4.0% : fill 13% (7/37) · rebond 27% (3/7)
      · −5.0% : fill 4% (3/37) · rebond 50% (1/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 39% (27/67) · rebond 63% (17/27)
      · −2.0% : fill 25% (17/67) · rebond 79% (12/17)
      · −3.0% : fill 8% (6/67) · rebond 32% (2/6)
      · −4.0% : fill 4% (4/67) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/67) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 70% si les 15 1res min sont vertes (87 cas) · 18% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 46% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 163min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **83%** · continue >prix actuel 40% ; creux résiduel méd -0.93% (q20 -1.95%) → **SL/trailing à −1.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.84% / q75 +1.7% → **scale +0.84% / runner +1.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **11%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.84%** (au-delà de la MAE q10 -2.84%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.33%] · haut q95 +3.06% · bas q05 -3.71%
   - 60min (n=160) : retour [-3.99% .. +2.91%] · haut q95 +3.49% · bas q05 -4.7%
   - 2h (n=160) : retour [-4.44% .. +3.14%] · haut q95 +4.24% · bas q05 -5.52%
   - 4h (n=160) : retour [-4.72% .. +3.35%] · haut q95 +5.28% · bas q05 -5.92%
   - 6h (n=160) : retour [-4.93% .. +3.51%] · haut q95 +5.28% · bas q05 -6.84%
   - session (n=160) : retour [-4.35% .. +3.51%] · haut q95 +5.28% · bas q05 -6.84%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.1% / strong 2.5%) · base = 9 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **19%**. Lecture précoce 30 min : signature présente → 12% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.29% / p90 1.8%) · ~2.0 replis/séance, durée méd 55.87 min. P(nouveau plus-haut après repli) :
   - −0.5% → **60%** (reprise méd 17.23 min, n=23)
   - −1.0% → **42%** (reprise méd 20.49 min, n=9)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.8%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +3.46% (q75 +4.43% / q95 +6.6%), MFE méd +3.74% / q90 +6.4%
   - Échelle scale-out : +3.74% (33%) / +5.32% (33%) / +6.4% (34%)
- **DÉSARMER** : repli > **−1.8%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.4% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 85% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.53
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.9  _(momentum baissier)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -1.862  _(bearish_recent)_
- **BB** : %B 0.09 · largeur 18.2%
- **ATR** : 10.42 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.239  _(distribution)_
- **Vol ratio** : 1.0  _(volume normal)_
- **Choppiness** : 37.6  _(marche directionnel)_
- **MA** : MA20 258.3 · MA50 278.67 · MA200 316.09  _(prix < MA20)_
- **Dist MA** : MA20 -7.4% · MA50 -14.1% · MA200 -24.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90005 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
