# PLTR

**Generated** : 2026-08-06T00:24:23.019334+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $158.43  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $158.43 (+4.1% vs entrée) · entrée $152.21 · stop $135.35 · T1 $187.91 · R/R 2.12  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk 0.007 _(réel 5 s)_ (GBM -0.036) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 249 % hors [0,100] (R² max 0.40). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 17.2 < 20 (tendance pas encore confirmée) alors que Choppiness 34.0 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 1.12 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $149.75–$154.67 (mid $152.21)
- Spot actuel : $158.43 (+4.1% au-dessus de la zone — repli à attendre)
- Stop : $135.35 (stop swing_plan-based (-14.57%))
- Targets : T1 $187.91 · R/R 2.12 | T2 $188.45 · R/R 2.15 | T3 $188.99 · R/R 2.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $135.35


## Edge, scénarios & sizing

- EV/risk : -0.036 | EV/share : $-0.609 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 3 % | T2 2 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 14.0 | side 81.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 475.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.785% → cible +3.414% / stop −7.0%, p_fill 53%, n_eff≈20.3) : P(cible|rempli) **16%** · **EV/risk +0.030** (×p_fill ; si rempli +0.39% du capital)
  - **swing** (entrée dip −3.927% → cible +23.453% / stop −11.078%, p_fill 47%, n_eff≈17.0) : P(cible|rempli) **0%** · **EV/risk +0.007** (×p_fill ; si rempli +0.17% du capital)
  - **deep** (entrée dip −6.068% → cible +11.393% / stop −8.498%, p_fill 40%, n_eff≈15.0) : P(cible|rempli) **10%** · **EV/risk -0.072** (×p_fill ; si rempli -1.52% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→75% · +2.0%→46% · +3.0%→24% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.85% (p90 6.93%) · excursion haute méd. +1.88% / basse méd. −1.71%
- Profil de vol intra : ouverture 2.983% vs midi 0.73% vs clôture 0.856% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓1% ; spike-down 56% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr 0.004)_ ; drift intra méd. 0.102% ; recovery-V 30%
- **σ réalisé intraday** 2.728% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 48% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 125.6771 (VA 125.0511–125.9119 ; dernier close 125.89)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 51% · **stop −3.07%** sous le fill (sous le bruit) · cible +1.01% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 57% (gap-down >1% 30% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.92% (p90 −2.11%) · haut méd +0.9% · range méd 1.91%
- Excursion ouverture 15min (n=160) : bas méd −1.06% (p90 −3.01%) · haut méd +1.08% · range méd 2.32%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.54%) · haut méd +1.17% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.38% (p90 −4.01%) · haut méd +1.33% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 125.89 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (119/159) · gap 40% · délai 0.0min · rebond 54% (65/119) (MFE +1.07%)
   - −1.0% : fill 30min 59% · séance 67% (108/159) · gap 30% · délai 0.0min · rebond 60% (62/108) (MFE +1.3%)
   - −1.5% : fill 30min 48% · séance 59% (94/159) · gap 24% · délai 0.1min · rebond 69% (59/94) (MFE +1.57%)
   - −2.0% : fill 30min 42% · séance 52% (79/159) · gap 16% · délai 1.3min · rebond 63% (49/79) (MFE +1.57%)
   - −3.0% : fill 30min 23% · séance 35% (55/159) · gap 9% · délai 5.2min · rebond 50% (25/55) (MFE +0.99%)
   - −4.0% : fill 30min 18% · séance 25% (40/159) · gap 5% · délai 12.5min · rebond 55% (20/40) (MFE +1.02%)
   - −5.0% : fill 30min 11% · séance 19% (28/159) · gap 2% · délai 25.3min · rebond 51% (13/28) (MFE +1.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −2.02%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −2.14%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.49% (p90 −1.38%) → stop au-delà de −1.01% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=549 jambes) : jambe baissière méd −1.02% (p90 −2.53%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 92% (66/71) · rebond 61% (39/66)
      · −2.0% : fill 79% (56/71) · rebond 62% (36/56)
      · −3.0% : fill 56% (39/71) · rebond 47% (18/39)
      · −4.0% : fill 44% (30/71) · rebond 51% (14/30)
      · −5.0% : fill 36% (23/71) · rebond 58% (12/23)
   - **flat** (29 séances) :
      · −1.0% : fill 81% (24/29) · rebond 44% (12/24)
      · −2.0% : fill 62% (13/29) · rebond 65% (8/13)
      · −3.0% : fill 41% (10/29) · rebond 57% (5/10)
      · −4.0% : fill 25% (7/29) · rebond 84% (5/7)
      · −5.0% : fill 13% (3/29) · rebond 9% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 31% (18/59) · rebond 72% (11/18)
      · −2.0% : fill 17% (10/59) · rebond 69% (5/10)
      · −3.0% : fill 7% (6/59) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 69% si les 15 1res min sont vertes (78 cas) · 34% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **24min** → P(séance verte=clôture>ouverture) 76% si début vert vs 27% si rouge (base 51% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -1.55% (q20 -2.39%) → **SL/trailing à −2.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.42% / q75 +2.58% → **scale +1.42% / runner +2.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **27%** (continue à baisser 46%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.2%** (au-delà de la MAE q10 -3.2%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.01% .. +3.45%] · haut q95 +3.78% · bas q05 -4.22%
   - 60min (n=160) : retour [-3.87% .. +3.61%] · haut q95 +4.5% · bas q05 -4.46%
   - 2h (n=160) : retour [-4.1% .. +4.46%] · haut q95 +4.76% · bas q05 -4.79%
   - 4h (n=160) : retour [-4.44% .. +4.92%] · haut q95 +5.6% · bas q05 -5.83%
   - 6h (n=160) : retour [-5.05% .. +4.64%] · haut q95 +5.61% · bas q05 -6.3%
   - session (n=160) : retour [-4.96% .. +4.48%] · haut q95 +5.61% · bas q05 -6.3%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 2.5% / strong 2.5%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 12% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.61%) · ~3.0 replis/séance, durée méd 72.55 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 21.18 min, n=27)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.61%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.43% (q75 +5.23% / q95 +7.65%), MFE méd +5.49% / q90 +8.71%
   - Échelle scale-out : +5.49% (33%) / +7.2% (33%) / +8.71% (34%)
- **DÉSARMER** : repli > **−1.61%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.71% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : extreme
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

- **RSI** : 65.2  _(momentum haussier)_
- **ADX** : 17.2  _(pas de tendance nette)_
- **MACD** : hist 3.273  _(bullish_recent)_
- **BB** : %B 1.12 · largeur 33.3%
- **ATR** : 8.43 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.219  _(accumulation)_
- **Vol ratio** : 1.42  _(volume normal)_
- **Choppiness** : 34.0  _(marche directionnel)_
- **MA** : MA20 131.43 · MA50 131.42 · MA200 152.44  _(prix > MA20)_
- **Dist MA** : MA20 +20.5% · MA50 +20.5% · MA200 +3.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93754 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
