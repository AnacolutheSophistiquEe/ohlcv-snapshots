# PLTR

**Generated** : 2026-08-06T22:01:57.660892+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $155.92  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $155.92 (+3.2% vs entrée) · entrée $151.08 · stop $142.65 · T1 $163.21 · R/R 1.44  
> ↳ P(T1 av. stop) 21 % _(réel 5 s)_ · EV/risk 0.021 _(réel 5 s)_ (GBM -0.102) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 18.4 < 20 (tendance pas encore confirmée) alors que Choppiness 34.0 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 0.97 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $148.65–$153.51 (mid $151.08)
- Spot actuel : $155.92 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : $142.65 (stop swing_plan-based (-8.51%))
- Targets : T1 $163.21 · R/R 1.44 | T2 $175.35 · R/R 2.88 | T3 $187.48 · R/R 4.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $142.65


## Edge, scénarios & sizing

- EV/risk : -0.102 | EV/share : $-0.859 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 7 % | T3 2 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.4 | bear 13.6 | side 53.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 468.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.415% → cible +4.692% / stop −2.5%, p_fill 56%, n_eff≈22.4) : P(cible|rempli) **3%** · **EV/risk -0.040** (×p_fill ; si rempli -0.18% du capital)
  - **swing** (entrée dip −3.101% → cible +8.032% / stop −5.582%, p_fill 53%, n_eff≈21.7) : P(cible|rempli) **21%** · **EV/risk +0.021** (×p_fill ; si rempli +0.22% du capital)
  - **deep** (entrée dip −4.797% → cible +11.358% / stop −8.522%, p_fill 47%, n_eff≈16.9) : P(cible|rempli) **27%** · **EV/risk +0.016** (×p_fill ; si rempli +0.29% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→76% · +2.0%→48% · +3.0%→25% · +5.0%→8% · +8.0%→4%
- Range intraday médian 3.89% (p90 6.99%) · excursion haute méd. +1.9% / basse méd. −1.71%
- Profil de vol intra : ouverture 3.036% vs midi 0.74% vs clôture 0.86% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 21% · trend ↑2%/↓0% ; spike-down 56% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr 0.006)_ ; drift intra méd. 0.53% ; recovery-V 28%
- **σ réalisé intraday** 2.883% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 48% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 159.3388 (VA 158.7612–160.6863 ; dernier close 158.43)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 51% · **stop −3.07%** sous le fill (sous le bruit) · cible +1.01% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 56% (gap-down >1% 29% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.92% (p90 −2.11%) · haut méd +0.94% · range méd 1.96%
- Excursion ouverture 15min (n=160) : bas méd −1.06% (p90 −3.01%) · haut méd +1.17% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.16% (p90 −3.52%) · haut méd +1.22% · range méd 2.78%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −4.0%) · haut méd +1.38% · range méd 3.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 158.43 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 74% (118/159) · gap 38% · délai 0.0min · rebond 55% (64/118) (MFE +1.13%)
   - −1.0% : fill 30min 59% · séance 66% (109/159) · gap 29% · délai 0.0min · rebond 61% (63/109) (MFE +1.31%)
   - −1.5% : fill 30min 47% · séance 59% (95/159) · gap 23% · délai 0.2min · rebond 70% (60/95) (MFE +1.46%)
   - −2.0% : fill 30min 41% · séance 52% (80/159) · gap 15% · délai 1.5min · rebond 64% (50/80) (MFE +1.54%)
   - −3.0% : fill 30min 22% · séance 34% (55/159) · gap 8% · délai 5.2min · rebond 50% (25/55) (MFE +0.99%)
   - −4.0% : fill 30min 17% · séance 24% (40/159) · gap 5% · délai 12.5min · rebond 55% (20/40) (MFE +1.02%)
   - −5.0% : fill 30min 11% · séance 18% (28/159) · gap 2% · délai 25.3min · rebond 51% (13/28) (MFE +1.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.0%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.13%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.38%) → stop au-delà de −1.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=556 jambes) : jambe baissière méd −1.02% (p90 −2.53%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 93% (67/70) · rebond 63% (40/67)
      · −2.0% : fill 80% (57/70) · rebond 64% (37/57)
      · −3.0% : fill 54% (39/70) · rebond 47% (18/39)
      · −4.0% : fill 42% (30/70) · rebond 51% (14/30)
      · −5.0% : fill 35% (23/70) · rebond 58% (12/23)
   - **flat** (29 séances) :
      · −1.0% : fill 81% (24/29) · rebond 44% (12/24)
      · −2.0% : fill 62% (13/29) · rebond 65% (8/13)
      · −3.0% : fill 41% (10/29) · rebond 57% (5/10)
      · −4.0% : fill 25% (7/29) · rebond 84% (5/7)
      · −5.0% : fill 13% (3/29) · rebond 9% (1/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 30% (18/60) · rebond 72% (11/18)
      · −2.0% : fill 16% (10/60) · rebond 69% (5/10)
      · −3.0% : fill 7% (6/60) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/60) · rebond 20% (1/3)
      · −5.0% : fill 1% (2/60) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 67% si les 15 1res min sont vertes (78 cas) · 34% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 83% si début vert vs 23% si rouge (base 51% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **83%** · continue >prix actuel 62% ; creux résiduel méd -0.96% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.98% / q75 +2.67% → **scale +1.98% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **23%** (continue à baisser 48%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.29%** (au-delà de la MAE q10 -3.29%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.97% .. +3.8%] · haut q95 +4.05% · bas q05 -4.18%
   - 60min (n=160) : retour [-3.84% .. +3.91%] · haut q95 +4.78% · bas q05 -4.46%
   - 2h (n=160) : retour [-4.07% .. +5.65%] · haut q95 +5.81% · bas q05 -4.76%
   - 4h (n=160) : retour [-4.41% .. +5.64%] · haut q95 +6.44% · bas q05 -5.77%
   - 6h (n=160) : retour [-5.03% .. +5.78%] · haut q95 +6.82% · bas q05 -6.28%
   - session (n=160) : retour [-4.89% .. +4.9%] · haut q95 +6.82% · bas q05 -6.28%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 2.5% / strong 3.1%) · base = 9 séances trend-up (n_eff 6.3)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 18% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.79% (p75 1.05% / p90 1.52%) · ~3.91 replis/séance, durée méd 70.51 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 14.94 min, n=31)
   - −1.0% → **38%** (reprise méd 65.0 min, n=8)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.05%) ; extension open→close méd +4.69% (q75 +9.54% / q95 +12.13%), MFE méd +6.83% / q90 +13.49%
   - Échelle scale-out : +6.83% (33%) / +10.83% (33%) / +13.49% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.49% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 52% du temps (retour médian dernière heure +-0.0%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.8  _(momentum haussier)_
- **ADX** : 18.4  _(pas de tendance nette)_
- **MACD** : hist 3.7  _(bullish_recent)_
- **BB** : %B 0.97 · largeur 36.8%
- **ATR** : 8.43 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.187  _(accumulation)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 34.0  _(marche directionnel)_
- **MA** : MA20 132.78 · MA50 131.81 · MA200 152.33  _(prix > MA20)_
- **Dist MA** : MA20 +17.4% · MA50 +18.3% · MA200 +2.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93597 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
