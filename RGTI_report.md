# RGTI

**Generated** : 2026-08-19T00:27:25.358049+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.71  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $17.71 (+1.4% vs entrée) · entrée $17.46 · stop $15.60 · T1 $21.19 · R/R 2.01  
> ↳ P(T1 av. stop) 10 % _(réel 5 s)_ · EV/risk -0.056 _(réel 5 s)_ (GBM -0.037) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 19.3 < 20 (tendance pas encore confirmée) alors que Choppiness 37.0 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $17.22–$17.71 (mid $17.46)
- Spot actuel : $17.71 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $15.60 (stop swing_plan-based (-11.93%))
- Targets : T1 $21.19 · R/R 2.01 | T2 $21.20 · R/R 2.01 | T3 $21.21 · R/R 2.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.60


## Edge, scénarios & sizing

- EV/risk : -0.037 | EV/share : $-0.070 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 6.5 | bear 27.3 | side 66.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 390.0 (= 22 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.634% → cible +7.056% / stop −3.528%, p_fill 78%, n_eff≈35.8) : P(cible|rempli) **25%** · **EV/risk +0.082** (×p_fill ; si rempli +0.37% du capital)
  - **swing** (entrée dip −1.397% → cible +21.365% / stop −10.683%, p_fill 82%, n_eff≈35.0) : P(cible|rempli) **10%** · **EV/risk -0.056** (×p_fill ; si rempli -0.72% du capital)
  - **deep** (entrée dip −2.119% → cible +10.124% / stop −9.646%, p_fill 81%, n_eff≈34.7) : P(cible|rempli) **39%** · **EV/risk -0.197** (×p_fill ; si rempli -2.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→72% · +3.0%→57% · +5.0%→41% · +8.0%→14%
- Range intraday médian 7.89% (p90 13.36%) · excursion haute méd. +4.01% / basse méd. −2.46%
- Profil de vol intra : ouverture 5.412% vs midi 1.574% vs clôture 1.849% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.017)_ ; drift intra méd. 0.483% ; recovery-V 38%
- **σ réalisé intraday** 4.65% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 47% / whipsaw 7%
- POC intraday (dernière séance, temps-au-prix) : 18.9906 (VA 18.7624–19.0529 ; dernier close 18.815)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 42% · rebond 75% · **stop −6.39%** sous le fill (sous le bruit) · cible +2.32% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.45% · baisse 56% (gap-down >1% 41% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.21% (p90 −2.74%) · haut méd +1.27% · range méd 2.61%
- Excursion ouverture 15min (n=160) : bas méd −1.47% (p90 −4.01%) · haut méd +1.78% · range méd 3.78%
- Excursion ouverture 30min (n=160) : bas méd −1.79% (p90 −5.01%) · haut méd +2.1% · range méd 4.57%
- Excursion ouverture 60min (n=160) : bas méd −2.09% (p90 −6.02%) · haut méd +2.5% · range méd 5.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.815 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 83% (135/159) · gap 47% · délai 0.0min · rebond 68% (90/135) (MFE +2.56%)
   - −1.0% : fill 30min 67% · séance 75% (127/159) · gap 41% · délai 0.0min · rebond 69% (84/127) (MFE +2.47%)
   - −1.5% : fill 30min 58% · séance 68% (120/159) · gap 34% · délai 0.0min · rebond 67% (80/120) (MFE +2.4%)
   - −2.0% : fill 30min 54% · séance 61% (112/159) · gap 26% · délai 0.0min · rebond 68% (76/112) (MFE +2.38%)
   - −3.0% : fill 30min 47% · séance 54% (96/159) · gap 12% · délai 1.2min · rebond 73% (70/96) (MFE +2.47%)
   - −4.0% : fill 30min 34% · séance 42% (76/159) · gap 3% · délai 5.7min · rebond 75% (56/76) (MFE +2.32%)
   - −5.0% : fill 30min 18% · séance 32% (61/159) · gap 1% · délai 21.5min · rebond 67% (46/61) (MFE +1.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.22%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.96% (p90 −2.72%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.13% (p90 −2.95%) → stop au-delà de −2.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1177 jambes) : jambe baissière méd −1.28% (p90 −3.19%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 95% (83/85) · rebond 65% (52/83)
      · −2.0% : fill 84% (78/85) · rebond 67% (53/78)
      · −3.0% : fill 78% (70/85) · rebond 68% (49/70)
      · −4.0% : fill 62% (56/85) · rebond 72% (40/56)
      · −5.0% : fill 48% (46/85) · rebond 65% (35/46)
   - **flat** (15 séances) :
      · −1.0% : fill 95% (14/15) · rebond 94% (12/14)
      · −2.0% : fill 65% (11/15) · rebond 81% (9/11)
      · −3.0% : fill 39% (6/15) · rebond 84% (4/6)
      · −4.0% : fill 39% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 24% (5/15) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 43% (30/59) · rebond 67% (20/30)
      · −2.0% : fill 30% (23/59) · rebond 63% (14/23)
      · −3.0% : fill 25% (20/59) · rebond 89% (17/20)
      · −4.0% : fill 16% (14/59) · rebond 84% (12/14)
      · −5.0% : fill 13% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 74% si les 15 1res min sont vertes (80 cas) · 30% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 87% si début vert vs 17% si rouge (base 54% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **87%** · continue >prix actuel 54% ; creux résiduel méd -2.4% (q20 -3.73%) → **SL/trailing à −3.73%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.37% / q75 +5.21% → **scale +2.37% / runner +5.21%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **17%** (continue à baisser 58%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.72%** (au-delà de la MAE q10 -5.72%), cible rebond +2.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.36% .. +4.96%] · haut q95 +6.53% · bas q05 -6.45%
   - 60min (n=160) : retour [-5.59% .. +6.43%] · haut q95 +6.78% · bas q05 -6.9%
   - 2h (n=160) : retour [-6.13% .. +7.27%] · haut q95 +9.17% · bas q05 -7.65%
   - 4h (n=160) : retour [-7.39% .. +7.49%] · haut q95 +9.18% · bas q05 -7.96%
   - 6h (n=160) : retour [-7.57% .. +8.34%] · haut q95 +9.53% · bas q05 -8.7%
   - session (n=160) : retour [-7.49% .. +8.68%] · haut q95 +10.24% · bas q05 -8.7%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.8)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.69% / p90 2.67%) · ~4.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 13.25 min, n=41)
   - −1.0% → **77%** (reprise méd 55.8 min, n=26)
   - −1.5% → **78%** (reprise méd 94.96 min, n=15)
   - −2.0% → **79%** (reprise méd 109.11 min, n=8)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.67%** (p90, défaut prudent ; serré/agressif −1.69%) ; extension open→close méd +7.29% (q75 +9.11% / q95 +9.99%), MFE méd +9.12% / q90 +10.34%
   - Échelle scale-out : +9.12% (33%) / +10.23% (33%) / +10.34% (34%)
- **DÉSARMER** : repli > **−2.67%** depuis le plus-haut = décay → P(retournement) **33%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.34% : P(retournement après) 0% (mèche méd 1.02%)
- **CONTEXTE** : la dernière heure tient les gains 59% du temps (retour médian dernière heure +0.5%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 74.6  _(surachat)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist 0.356  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 42.1%
- **ATR** : 1.11 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.003  _(neutre)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 37.0  _(marche directionnel)_
- **MA** : MA20 16.51 · MA50 17.63 · MA200 20.42  _(prix > MA20)_
- **Dist MA** : MA20 +7.3% · MA50 +0.5% · MA200 -13.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91111 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
