# CEG

**Generated** : 2026-07-27T00:26:47.308586+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $274.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $274.40 (+6.4% vs entrée) · entrée $258.01 · stop $254.01 · T1 $266.00 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.107 · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 17.0 < 20 (tendance pas encore confirmée) alors que Choppiness 37.1 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $256.41–$259.61 (mid $258.01)
- Spot actuel : $274.40 (+6.4% au-dessus de la zone — repli à attendre)
- Stop : $254.01 (stop swing_plan-based (-7.43%))
- Targets : T1 $266.00 · R/R 2.0 | T2 $273.99 · R/R 4.0 | T3 $281.98 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $254.01


## Edge, scénarios & sizing

- EV/risk : 0.107 | EV/share : $0.429 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 22 % | T3 12 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 21.1 | bear 67.5 | side 11.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 274.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.985% → cible +1.385% / stop −1.5%, p_fill 16%, n_eff≈9.2) : P(cible|rempli) **13%** · **EV/risk -0.025** (×p_fill ; si rempli -0.23% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→65% · +2.0%→39% · +3.0%→20% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.38% (p90 5.5%) · excursion haute méd. +1.5% / basse méd. −1.43%
- Profil de vol intra : ouverture 2.451% vs midi 0.708% vs clôture 0.739% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 45% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.051)_ ; drift intra méd. 0.138% ; recovery-V 8%
- **σ réalisé intraday** 2.166% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 277.6479 (VA 275.6109–279.5151 ; dernier close 274.36)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 41% · rebond 64% · **stop −3.08%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 45% (gap-down >1% 19% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.59% (p90 −1.6%) · haut méd +0.85% · range méd 1.63%
- Excursion ouverture 15min (n=160) : bas méd −0.63% (p90 −1.97%) · haut méd +1.01% · range méd 2.0%
- Excursion ouverture 30min (n=160) : bas méd −0.79% (p90 −2.53%) · haut méd +1.08% · range méd 2.25%
- Excursion ouverture 60min (n=160) : bas méd −0.88% (p90 −2.87%) · haut méd +1.32% · range méd 2.6%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 274.36 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 68% (117/159) · gap 27% · délai 0.0min · rebond 45% (57/117) (MFE +0.93%)
   - −1.0% : fill 30min 48% · séance 59% (101/159) · gap 19% · délai 1.0min · rebond 51% (55/101) (MFE +1.05%)
   - −1.5% : fill 30min 36% · séance 48% (86/159) · gap 10% · délai 3.3min · rebond 51% (46/86) (MFE +1.05%)
   - −2.0% : fill 30min 28% · séance 41% (67/159) · gap 7% · délai 8.4min · rebond 64% (42/67) (MFE +1.15%)
   - −3.0% : fill 30min 10% · séance 24% (41/159) · gap 3% · délai 60.6min · rebond 33% (14/41) (MFE +0.77%)
   - −4.0% : fill 30min 4% · séance 14% (27/159) · gap 2% · délai 47.1min · rebond 38% (12/27) (MFE +0.6%)
   - −5.0% : fill 30min 3% · séance 8% (18/159) · gap 1% · délai 45.4min · rebond 75% (12/18) (MFE +1.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.14%) → stop au-delà de −0.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.24% (p90 −0.98%) → stop au-delà de −0.66% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.38% (p90 −1.53%) → stop au-delà de −0.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=469 jambes) : jambe baissière méd −1.06% (p90 −2.59%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 96% (56/57) · rebond 52% (33/56)
      · −2.0% : fill 74% (41/57) · rebond 62% (27/41)
      · −3.0% : fill 50% (28/57) · rebond 36% (11/28)
      · −4.0% : fill 30% (19/57) · rebond 34% (8/19)
      · −5.0% : fill 21% (15/57) · rebond 77% (11/15)
   - **flat** (33 séances) :
      · −1.0% : fill 64% (19/33) · rebond 33% (5/19)
      · −2.0% : fill 32% (9/33) · rebond 48% (3/9)
      · −3.0% : fill 21% (7/33) · rebond 21% (1/7)
      · −4.0% : fill 9% (4/33) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/33) · rebond 61% (1/2)
   - **gap-up** (69 séances) :
      · −1.0% : fill 28% (26/69) · rebond 64% (17/26)
      · −2.0% : fill 18% (17/69) · rebond 79% (12/17)
      · −3.0% : fill 6% (6/69) · rebond 32% (2/6)
      · −4.0% : fill 3% (4/69) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/69) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 69% si les 15 1res min sont vertes (91 cas) · 26% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **32min** → P(séance verte=clôture>ouverture) 76% si début vert vs 15% si rouge (base 51% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=94) : tient le vert **76%** · continue >prix actuel 53% ; creux résiduel méd -1.07% (q20 -2.23%) → **SL/trailing à −2.23%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.14% / q75 +2.09% → **scale +1.14% / runner +2.09%**, sortie à la clôture
  - **si ROUGE au coude** (n=66) : edge inversé — récupère vert seulement **15%** (continue à baisser 72%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.52%** (au-delà de la MAE q10 -3.52%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.9% .. +2.32%] · haut q95 +2.76% · bas q05 -3.29%
   - 60min (n=160) : retour [-3.33% .. +3.05%] · haut q95 +3.41% · bas q05 -4.12%
   - 2h (n=160) : retour [-3.71% .. +3.02%] · haut q95 +4.21% · bas q05 -4.61%
   - 4h (n=160) : retour [-3.73% .. +3.35%] · haut q95 +4.47% · bas q05 -4.85%
   - 6h (n=160) : retour [-4.29% .. +3.54%] · haut q95 +4.78% · bas q05 -4.91%
   - session (n=160) : retour [-4.15% .. +3.58%] · haut q95 +4.76% · bas q05 -4.92%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.7% / strong 1.9%) · base = 9 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 16% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.18% (p75 1.36% / p90 1.68%) · ~1.0 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **71%** (reprise méd 32.71 min, n=20)
   - −1.0% → **67%** (reprise méd 175.01 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.68%** (p90, défaut prudent ; serré/agressif −1.36%) ; extension open→close méd +3.46% (q75 +4.38% / q95 +6.41%), MFE méd +3.74% / q90 +5.85%
   - Échelle scale-out : +3.74% (33%) / +5.06% (33%) / +5.85% (34%)
- **DÉSARMER** : repli > **−1.68%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.85% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 74.5  _(surachat)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist 3.736  _(pas de croisement recent)_
- **BB** : %B 0.93 · largeur 17.9%
- **ATR** : 8.2 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.025  _(neutre)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 37.2  _(marche directionnel)_
- **MA** : MA20 254.83 · MA50 263.71 · MA200 310.07  _(prix > MA20)_
- **Dist MA** : MA20 +7.7% · MA50 +4.1% · MA200 -11.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91859 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
