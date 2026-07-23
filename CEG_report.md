# CEG

**Generated** : 2026-07-23T00:26:26.928493+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $274.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot $274.90 (+3.5% vs entrée) · entrée $265.49 · stop $261.50 · T1 $269.17 · R/R 0.92  
> ↳ P(T1 av. stop) 53 % · EV/risk -0.015 · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 79.2 > 70 (surachat) ; %B 1.00 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $264.75–$266.22 (mid $265.49)
- Spot actuel : $274.90 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : $261.50 (stop swing_plan-based (-8.97%))
- Targets : T1 $269.17 · R/R 0.92 | T2 $272.86 · R/R 1.85 | T3 $276.54 · R/R 2.77
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $261.50


## Edge, scénarios & sizing

- EV/risk : -0.015 | EV/share : $-0.059 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 21 % | T3 7 %
- Kelly (position) : f* 0.039 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.4 | bear 6.9 | side 9.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→65% · +2.0%→38% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.39% (p90 5.5%) · excursion haute méd. +1.51% / basse méd. −1.5%
- Profil de vol intra : ouverture 2.485% vs midi 0.709% vs clôture 0.743% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.054)_ ; drift intra méd. -0.081% ; recovery-V 10%
- **σ réalisé intraday** 2.235% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 60% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 262.5619 (VA 260.5744–263.3569 ; dernier close 262.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 43% · rebond 64% · **stop −3.08%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.14% · baisse 45% (gap-down >1% 20% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.68%) · haut méd +0.84% · range méd 1.68%
- Excursion ouverture 15min (n=160) : bas méd −0.65% (p90 −2.04%) · haut méd +1.0% · range méd 2.01%
- Excursion ouverture 30min (n=160) : bas méd −0.82% (p90 −2.58%) · haut méd +1.08% · range méd 2.26%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.96%) · haut méd +1.37% · range méd 2.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 262.27 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 68% (117/159) · gap 26% · délai 0.0min · rebond 45% (57/117) (MFE +0.93%)
   - −1.0% : fill 30min 49% · séance 59% (101/159) · gap 20% · délai 1.0min · rebond 51% (55/101) (MFE +1.05%)
   - −1.5% : fill 30min 38% · séance 50% (88/159) · gap 11% · délai 3.3min · rebond 51% (47/88) (MFE +1.05%)
   - −2.0% : fill 30min 29% · séance 43% (69/159) · gap 7% · délai 8.5min · rebond 64% (43/69) (MFE +1.15%)
   - −3.0% : fill 30min 11% · séance 26% (42/159) · gap 3% · délai 57.9min · rebond 33% (15/42) (MFE +0.77%)
   - −4.0% : fill 30min 5% · séance 14% (28/159) · gap 2% · délai 48.4min · rebond 37% (12/28) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 9% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.15%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.24% (p90 −0.99%) → stop au-delà de −0.75% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.59%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=479 jambes) : jambe baissière méd −1.07% (p90 −2.59%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 96% (56/57) · rebond 50% (33/56)
      · −2.0% : fill 78% (42/57) · rebond 62% (28/42)
      · −3.0% : fill 52% (28/57) · rebond 36% (11/28)
      · −4.0% : fill 31% (19/57) · rebond 34% (8/19)
      · −5.0% : fill 22% (15/57) · rebond 77% (11/15)
   - **flat** (33 séances) :
      · −1.0% : fill 60% (19/33) · rebond 38% (5/19)
      · −2.0% : fill 36% (10/33) · rebond 47% (3/10)
      · −3.0% : fill 24% (8/33) · rebond 24% (2/8)
      · −4.0% : fill 11% (5/33) · rebond 19% (1/5)
      · −5.0% : fill 4% (3/33) · rebond 50% (1/3)
   - **gap-up** (69 séances) :
      · −1.0% : fill 29% (26/69) · rebond 64% (17/26)
      · −2.0% : fill 19% (17/69) · rebond 79% (12/17)
      · −3.0% : fill 6% (6/69) · rebond 32% (2/6)
      · −4.0% : fill 3% (4/69) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/69) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 69% si les 15 1res min sont vertes (88 cas) · 26% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 76% si début vert vs 17% si rouge (base 50% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=88) : tient le vert **76%** · continue >prix actuel 50% ; creux résiduel méd -1.01% (q20 -2.5%) → **SL/trailing à −2.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +1.94% → **scale +1.18% / runner +1.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **17%** (continue à baisser 67%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.41%** (au-delà de la MAE q10 -3.41%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.99% .. +2.34%] · haut q95 +2.78% · bas q05 -3.44%
   - 60min (n=160) : retour [-3.64% .. +2.6%] · haut q95 +3.36% · bas q05 -4.2%
   - 2h (n=160) : retour [-3.81% .. +2.95%] · haut q95 +4.21% · bas q05 -4.84%
   - 4h (n=160) : retour [-3.88% .. +3.28%] · haut q95 +4.69% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.44% .. +3.08%] · haut q95 +4.98% · bas q05 -5.08%
   - session (n=160) : retour [-4.32% .. +3.26%] · haut q95 +4.98% · bas q05 -5.08%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.7% / strong 1.9%) · base = 9 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 13% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.33% / p90 1.7%) · ~1.3 replis/séance, durée méd 60.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 22.57 min, n=22)
   - −1.0% → **58%** (reprise méd 114.96 min, n=10)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.7%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.24% (q75 +3.91% / q95 +6.6%), MFE méd +3.42% / q90 +5.81%
   - Échelle scale-out : +3.42% (33%) / +5.29% (33%) / +5.81% (34%)
- **DÉSARMER** : repli > **−1.7%** depuis le plus-haut = décay → P(retournement) **63%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.81% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 89% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 79.2  _(surachat)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist 3.004  _(pas de croisement recent)_
- **BB** : %B 1.0 · largeur 16.2%
- **ATR** : 8.36 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.088  _(distribution)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 41.7  _(transition)_
- **MA** : MA20 254.16 · MA50 264.55 · MA200 310.93  _(prix > MA20)_
- **Dist MA** : MA20 +8.2% · MA50 +3.9% · MA200 -11.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90392 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
