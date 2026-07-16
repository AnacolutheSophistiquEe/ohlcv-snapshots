# HOOD

**Generated** : 2026-07-16T00:33:11.881719+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $115.54  

> 🟡 **WAIT-FOR-DIP** — spot +4.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $115.54 (+4.2% vs entrée) · entrée $110.91 · stop $107.58 · T1 $113.36 · R/R 0.74  
> ↳ P(T1 av. stop) 48 % · EV/risk 0.064 · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $110.41–$111.40 (mid $110.91)
- Spot actuel : $115.54 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : $107.58 (stop swing_plan-based (-11.08%))
- Targets : T1 $113.36 · R/R 0.74 | T2 $115.82 · R/R 1.47 | T3 $118.28 · R/R 2.21
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $107.58


## Edge, scénarios & sizing

- EV/risk : 0.064 | EV/share : $0.214 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 26 % | T3 21 %
- Kelly (position) : f* 0.079 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.7 | bear 5.4 | side 83.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 578.0 (= 5 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.01% → cible +2.216% / stop −3.0%, p_fill 20%, n_eff≈8.5) : P(cible|rempli) **25%** · **EV/risk -0.064** (×p_fill ; si rempli -0.94% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→55% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.05% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.528% vs midi 1.073% vs clôture 1.051% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑1%/↓0% ; spike-down 65% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; momentum — autocorr 0.037)_ ; drift intra méd. 0.688% ; recovery-V 35%
- **σ réalisé intraday** 3.816% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 46% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 112.3017 (VA 111.8407–113.4543 ; dernier close 111.99)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 87% · **stop −4.57%** sous le fill (sous le bruit) · cible +2.72% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 34% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.75% (p90 −1.99%) · haut méd +0.89% · range méd 1.98%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.04%) · haut méd +1.07% · range méd 2.59%
- Excursion ouverture 30min (n=160) : bas méd −1.29% (p90 −3.84%) · haut méd +1.68% · range méd 3.34%
- Excursion ouverture 60min (n=160) : bas méd −1.63% (p90 −3.88%) · haut méd +1.71% · range méd 3.75%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 111.99 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (121/159) · gap 41% · délai 0.0min · rebond 56% (61/121) (MFE +1.41%)
   - −1.0% : fill 30min 58% · séance 66% (107/159) · gap 34% · délai 0.0min · rebond 61% (61/107) (MFE +1.32%)
   - −1.5% : fill 30min 50% · séance 62% (99/159) · gap 23% · délai 0.3min · rebond 56% (54/99) (MFE +1.54%)
   - −2.0% : fill 30min 42% · séance 55% (88/159) · gap 15% · délai 0.6min · rebond 66% (53/88) (MFE +1.4%)
   - −3.0% : fill 30min 31% · séance 42% (66/159) · gap 7% · délai 10.8min · rebond 70% (43/66) (MFE +1.91%)
   - −4.0% : fill 30min 18% · séance 32% (50/159) · gap 3% · délai 22.3min · rebond 77% (32/50) (MFE +2.21%)
   - −5.0% : fill 30min 10% · séance 20% (31/159) · gap 1% · délai 29.8min · rebond 87% (25/31) (MFE +2.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.5%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.44%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.43%) → stop au-delà de −1.64% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=751 jambes) : jambe baissière méd −1.15% (p90 −2.66%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 95% (67/71) · rebond 60% (36/67)
      · −2.0% : fill 79% (56/71) · rebond 61% (32/56)
      · −3.0% : fill 67% (45/71) · rebond 66% (28/45)
      · −4.0% : fill 53% (36/71) · rebond 80% (25/36)
      · −5.0% : fill 35% (25/71) · rebond 84% (20/25)
   - **flat** (22 séances) :
      · −1.0% : fill 71% (17/22) · rebond 76% (12/17)
      · −2.0% : fill 54% (12/22) · rebond 59% (7/12)
      · −3.0% : fill 18% (6/22) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/22) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/22) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 34% (23/66) · rebond 56% (13/23)
      · −2.0% : fill 29% (20/66) · rebond 85% (14/20)
      · −3.0% : fill 23% (15/66) · rebond 96% (13/15)
      · −4.0% : fill 15% (9/66) · rebond 87% (6/9)
      · −5.0% : fill 8% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 68% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 84% si début vert vs 20% si rouge (base 52% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 193min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **84%** · continue >prix actuel 59% ; creux résiduel méd -1.17% (q20 -2.45%) → **SL/trailing à −2.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +3.19% → **scale +1.8% / runner +3.19%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.22%** (au-delà de la MAE q10 -4.22%), cible rebond +1.55% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.01% .. +4.7%] · haut q95 +5.19% · bas q05 -4.95%
   - 60min (n=160) : retour [-3.66% .. +4.88%] · haut q95 +6.37% · bas q05 -5.19%
   - 2h (n=160) : retour [-4.51% .. +6.6%] · haut q95 +7.61% · bas q05 -5.95%
   - 4h (n=160) : retour [-4.73% .. +7.44%] · haut q95 +8.49% · bas q05 -6.56%
   - 6h (n=160) : retour [-5.68% .. +7.16%] · haut q95 +8.5% · bas q05 -7.65%
   - session (n=160) : retour [-5.2% .. +7.37%] · haut q95 +8.74% · bas q05 -7.77%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 10.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **40%**. Lecture précoce 30 min : signature présente → 22% vs absente 4% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.42% / p90 2.11%) · ~4.0 replis/séance, durée méd 37.3 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=50)
   - −1.0% → **70%** (reprise méd 32.75 min, n=22)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.11%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.07% (q75 +9.68% / q95 +13.38%), MFE méd +6.49% / q90 +14.82%
   - Échelle scale-out : +6.49% (33%) / +11.14% (33%) / +14.82% (34%)
- **DÉSARMER** : repli > **−2.11%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.82% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +0.61%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 68.8  _(momentum haussier)_
- **ADX** : 29.3  _(tendance etablie)_
- **MACD** : hist -0.011  _(bearish_recent)_
- **BB** : %B 0.79 · largeur 26.9%
- **ATR** : 6.43 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.022  _(neutre)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 45.3  _(transition)_
- **MA** : MA20 107.09 · MA50 91.97 · MA200 102.01  _(prix > MA20)_
- **Dist MA** : MA20 +7.9% · MA50 +25.6% · MA200 +13.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90718 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
