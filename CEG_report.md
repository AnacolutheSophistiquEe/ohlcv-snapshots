# CEG

**Generated** : 2026-07-01T21:57:14.048889+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $236.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $236.50 (+4.6% vs entrée) · entrée $226.20 · stop $222.80 · T1 $229.22 · R/R 0.89  
> ↳ P(T1 av. stop) 50 % · EV/risk -0.076 · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 17.4 < 20 (tendance pas encore confirmée) alors que Choppiness 37.1 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $225.59–$226.80 (mid $226.20)
- Spot actuel : $236.50 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : $222.80 (stop swing_plan-based (-10.08%))
- Targets : T1 $229.22 · R/R 0.89 | T2 $232.25 · R/R 1.78 | T3 $235.28 · R/R 2.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $222.80


## Edge, scénarios & sizing

- EV/risk : -0.076 | EV/share : $-0.258 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 23 % | T3 11 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 80.5 | bear 5.8 | side 13.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→65% · +2.0%→35% · +3.0%→24% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.55% (p90 5.51%) · excursion haute méd. +1.49% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.559% vs midi 0.736% vs clôture 0.772% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. -0.498% ; recovery-V 17%
- **σ réalisé intraday** 2.4% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 65% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 253.9025 (VA 250.3725–254.9615 ; dernier close 248.36)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 49% · rebond 66% · **stop −3.03%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 43% (gap-down >1% 22% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.82%) · haut méd +0.78% · range méd 1.71%
- Excursion ouverture 15min (n=160) : bas méd −0.84% (p90 −2.25%) · haut méd +1.0% · range méd 2.07%
- Excursion ouverture 30min (n=160) : bas méd −0.97% (p90 −2.72%) · haut méd +1.07% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.14% (p90 −3.05%) · haut méd +1.29% · range méd 2.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 248.36 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (120/159) · gap 28% · délai 0.0min · rebond 44% (59/120) (MFE +0.89%)
   - −1.0% : fill 30min 52% · séance 65% (105/159) · gap 22% · délai 1.9min · rebond 51% (58/105) (MFE +1.06%)
   - −1.5% : fill 30min 41% · séance 58% (92/159) · gap 12% · délai 4.0min · rebond 52% (51/92) (MFE +1.05%)
   - −2.0% : fill 30min 32% · séance 49% (72/159) · gap 9% · délai 9.9min · rebond 66% (47/72) (MFE +1.15%)
   - −3.0% : fill 30min 13% · séance 28% (44/159) · gap 4% · délai 42.2min · rebond 42% (19/44) (MFE +0.79%)
   - −4.0% : fill 30min 6% · séance 17% (29/159) · gap 2% · délai 66.1min · rebond 42% (14/29) (MFE +0.74%)
   - −5.0% : fill 30min 4% · séance 10% (18/159) · gap 1% · délai 45.0min · rebond 69% (11/18) (MFE +1.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.41%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.27% (p90 −1.2%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.62%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=477 jambes) : jambe baissière méd −1.09% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 100% (54/54) · rebond 50% (33/54)
      · −2.0% : fill 86% (40/54) · rebond 65% (28/40)
      · −3.0% : fill 56% (25/54) · rebond 48% (11/25)
      · −4.0% : fill 38% (18/54) · rebond 39% (8/18)
      · −5.0% : fill 26% (14/54) · rebond 72% (10/14)
   - **flat** (37 séances) :
      · −1.0% : fill 67% (23/37) · rebond 39% (7/23)
      · −2.0% : fill 41% (14/37) · rebond 49% (6/14)
      · −3.0% : fill 28% (12/37) · rebond 31% (6/12)
      · −4.0% : fill 13% (7/37) · rebond 27% (3/7)
      · −5.0% : fill 4% (3/37) · rebond 50% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 39% (28/68) · rebond 63% (18/28)
      · −2.0% : fill 25% (18/68) · rebond 79% (13/18)
      · −3.0% : fill 8% (7/68) · rebond 31% (2/7)
      · −4.0% : fill 4% (4/68) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/68) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 70% si les 15 1res min sont vertes (88 cas) · 19% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 47% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 163min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **83%** · continue >prix actuel 40% ; creux résiduel méd -0.93% (q20 -1.95%) → **SL/trailing à −1.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.85% / q75 +1.69% → **scale +0.85% / runner +1.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **11%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.9%** (au-delà de la MAE q10 -2.9%), cible rebond +0.79% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.01% .. +2.33%] · haut q95 +3.1% · bas q05 -3.73%
   - 60min (n=160) : retour [-3.38% .. +3.0%] · haut q95 +3.5% · bas q05 -4.11%
   - 2h (n=160) : retour [-3.72% .. +3.14%] · haut q95 +4.26% · bas q05 -4.67%
   - 4h (n=160) : retour [-3.78% .. +3.35%] · haut q95 +5.28% · bas q05 -4.96%
   - 6h (n=160) : retour [-4.32% .. +3.53%] · haut q95 +5.28% · bas q05 -4.98%
   - session (n=160) : retour [-4.25% .. +3.54%] · haut q95 +5.28% · bas q05 -4.96%


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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.53
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.2  _(neutre)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist -1.257  _(bearish_recent)_
- **BB** : %B -0.03 · largeur 16.9%
- **ATR** : 10.3 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.253  _(distribution)_
- **Vol ratio** : 2.07  _(volume au-dessus de la moyenne)_
- **Choppiness** : 37.2  _(marche directionnel)_
- **MA** : MA20 259.7 · MA50 279.43 · MA200 316.54  _(prix < MA20)_
- **Dist MA** : MA20 -8.9% · MA50 -15.4% · MA200 -25.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90742 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
