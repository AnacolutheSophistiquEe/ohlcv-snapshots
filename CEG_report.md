# CEG

**Generated** : 2026-07-24T22:04:14.074843+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $274.35  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)  
> ↳ spot $274.35 (+6.4% vs entrée) · entrée $257.96 · stop $253.96 · T1 $265.95 · R/R 2.0  
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
- Entry (zone de repli) : $256.36–$259.56 (mid $257.96)
- Spot actuel : $274.35 (+6.4% au-dessus de la zone — repli à attendre)
- Stop : $253.96 (stop swing_plan-based (-7.43%))
- Targets : T1 $265.95 · R/R 2.0 | T2 $273.94 · R/R 4.0 | T3 $281.93 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $253.96


## Edge, scénarios & sizing

- EV/risk : 0.107 | EV/share : $0.429 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 22 % | T3 12 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 21.1 | bear 67.4 | side 11.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 274.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.985% → cible +1.385% / stop −1.5%, p_fill 18%, n_eff≈9.2) : P(cible|rempli) **13%** · **EV/risk -0.027** (×p_fill ; si rempli -0.23% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→65% · +2.0%→38% · +3.0%→20% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.4% (p90 5.5%) · excursion haute méd. +1.51% / basse méd. −1.5%
- Profil de vol intra : ouverture 2.494% vs midi 0.706% vs clôture 0.739% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.054)_ ; drift intra méd. 0.126% ; recovery-V 10%
- **σ réalisé intraday** 2.223% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 57% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 274.4124 (VA 271.6156–275.0339 ; dernier close 274.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 42% · rebond 63% · **stop −3.08%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 44% (gap-down >1% 20% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.64%) · haut méd +0.85% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −0.64% (p90 −1.98%) · haut méd +1.01% · range méd 2.02%
- Excursion ouverture 30min (n=160) : bas méd −0.81% (p90 −2.57%) · haut méd +1.08% · range méd 2.3%
- Excursion ouverture 60min (n=160) : bas méd −0.96% (p90 −2.95%) · haut méd +1.39% · range méd 2.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 274.78 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 67% (116/159) · gap 26% · délai 0.0min · rebond 45% (56/116) (MFE +0.93%)
   - −1.0% : fill 30min 48% · séance 58% (100/159) · gap 20% · délai 1.0min · rebond 51% (54/100) (MFE +1.05%)
   - −1.5% : fill 30min 37% · séance 49% (87/159) · gap 11% · délai 3.4min · rebond 51% (46/87) (MFE +1.04%)
   - −2.0% : fill 30min 28% · séance 42% (68/159) · gap 7% · délai 8.5min · rebond 63% (42/68) (MFE +1.15%)
   - −3.0% : fill 30min 11% · séance 25% (42/159) · gap 3% · délai 57.9min · rebond 33% (15/42) (MFE +0.77%)
   - −4.0% : fill 30min 4% · séance 14% (28/159) · gap 2% · délai 48.4min · rebond 37% (12/28) (MFE +0.6%)
   - −5.0% : fill 30min 3% · séance 9% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.14%) → stop au-delà de −0.85% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.26% (p90 −0.98%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.56%) → stop au-delà de −0.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=476 jambes) : jambe baissière méd −1.07% (p90 −2.59%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 95% (55/56) · rebond 50% (32/55)
      · −2.0% : fill 78% (41/56) · rebond 62% (27/41)
      · −3.0% : fill 52% (28/56) · rebond 36% (11/28)
      · −4.0% : fill 31% (19/56) · rebond 34% (8/19)
      · −5.0% : fill 22% (15/56) · rebond 77% (11/15)
   - **flat** (33 séances) :
      · −1.0% : fill 60% (19/33) · rebond 38% (5/19)
      · −2.0% : fill 36% (10/33) · rebond 47% (3/10)
      · −3.0% : fill 24% (8/33) · rebond 24% (2/8)
      · −4.0% : fill 11% (5/33) · rebond 19% (1/5)
      · −5.0% : fill 4% (3/33) · rebond 50% (1/3)
   - **gap-up** (70 séances) :
      · −1.0% : fill 28% (26/70) · rebond 64% (17/26)
      · −2.0% : fill 18% (17/70) · rebond 79% (12/17)
      · −3.0% : fill 6% (6/70) · rebond 32% (2/6)
      · −4.0% : fill 3% (4/70) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/70) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 70% si les 15 1res min sont vertes (89 cas) · 26% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 77% si début vert vs 17% si rouge (base 51% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=89) : tient le vert **77%** · continue >prix actuel 51% ; creux résiduel méd -0.99% (q20 -2.49%) → **SL/trailing à −2.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +1.92% → **scale +1.19% / runner +1.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **17%** (continue à baisser 67%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.42%** (au-delà de la MAE q10 -3.42%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.98% .. +2.33%] · haut q95 +2.77% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.55% .. +3.06%] · haut q95 +3.42% · bas q05 -4.17%
   - 2h (n=160) : retour [-3.78% .. +3.02%] · haut q95 +4.21% · bas q05 -4.78%
   - 4h (n=160) : retour [-3.84% .. +3.35%] · haut q95 +4.61% · bas q05 -5.03%
   - 6h (n=160) : retour [-4.33% .. +3.66%] · haut q95 +4.93% · bas q05 -5.04%
   - session (n=160) : retour [-4.3% .. +3.73%] · haut q95 +4.93% · bas q05 -5.03%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 3.7% / strong 2.5%) · base = 10 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 17% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.17% (p75 1.36% / p90 1.63%) · ~1.0 replis/séance, durée méd 85.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **70%** (reprise méd 32.71 min, n=23)
   - −1.0% → **68%** (reprise méd 169.64 min, n=11)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.63%** (p90, défaut prudent ; serré/agressif −1.36%) ; extension open→close méd +3.47% (q75 +4.43% / q95 +6.39%), MFE méd +3.74% / q90 +5.33%
   - Échelle scale-out : +3.74% (33%) / +5.11% (33%) / +5.33% (34%)
- **DÉSARMER** : repli > **−1.63%** depuis le plus-haut = décay → P(retournement) **63%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.33% : P(retournement après) 0% (mèche méd 0.26%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 74.4  _(surachat)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist 3.733  _(pas de croisement recent)_
- **BB** : %B 0.93 · largeur 17.9%
- **ATR** : 8.2 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.029  _(neutre)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 37.2  _(marche directionnel)_
- **MA** : MA20 254.83 · MA50 263.71 · MA200 310.07  _(prix > MA20)_
- **Dist MA** : MA20 +7.7% · MA50 +4.0% · MA200 -11.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92056 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
