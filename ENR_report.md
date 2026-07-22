# ENR

**Generated** : 2026-07-22T21:40:09.245675+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €152.32  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €152.32 (+0.6% vs entrée) · entrée €151.43 · stop €148.14 · T1 €158.02 · R/R 2.0  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.297 _(réel 5 s)_ (GBM 0.062) · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €150.54–€152.32 (mid €151.43)
- Spot actuel : €152.32 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €148.14 (stop swing_plan-based (-2.75%))
- Targets : T1 €158.02 · R/R 2.0 | T2 €164.60 · R/R 4.0 | T3 €171.19 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €148.14


## Edge, scénarios & sizing

- EV/risk : 0.062 | EV/share : €0.205 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 16 % | T3 5 %
- Kelly (position) : f* 0.024 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 7.7 | bear 15.5 | side 76.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.345% → cible +1.945% / stop −1.5%, p_fill 89%, n_eff≈35.6) : P(cible|rempli) **38%** · **EV/risk -0.037** (×p_fill ; si rempli -0.06% du capital)
  - **swing** (entrée dip −0.588% → cible +4.35% / stop −2.175%, p_fill 81%, n_eff≈34.2) : P(cible|rempli) **22%** · **EV/risk -0.297** (×p_fill ; si rempli -0.80% du capital)
  - **deep** (entrée dip −0.778% → cible +6.151% / stop −3.076%, p_fill 92%, n_eff≈35.7) : P(cible|rempli) **19%** · **EV/risk -0.448** (×p_fill ; si rempli -1.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→61% · +2.0%→48% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 4.01% (p90 6.03%) · excursion haute méd. +1.66% / basse méd. −1.73%
- Profil de vol intra : ouverture 2.058% vs midi 0.901% vs clôture 1.143% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.049% ; recovery-V 23%
- **σ réalisé intraday** 2.479% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 60% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 157.12 (VA 155.968–158.656 ; dernier close 158.58)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 34% · rebond 67% · **stop −3.28%** sous le fill (sous le bruit) · cible +1.65% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 40% (gap-down >1% 22% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.57% (p90 −1.83%) · haut méd +0.44% · range méd 1.17%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.6% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.86% (p90 −2.36%) · haut méd +0.6% · range méd 1.85%
- Excursion ouverture 60min (n=160) : bas méd −0.96% (p90 −2.6%) · haut méd +0.67% · range méd 1.98%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 158.58 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 72% (117/159) · gap 30% · délai 0.3min · rebond 52% (61/117) (MFE +1.12%)
   - −1.0% : fill 30min 51% · séance 68% (107/159) · gap 22% · délai 1.2min · rebond 56% (63/107) (MFE +1.34%)
   - −1.5% : fill 30min 41% · séance 60% (92/159) · gap 20% · délai 8.0min · rebond 62% (59/92) (MFE +1.48%)
   - −2.0% : fill 30min 26% · séance 45% (67/159) · gap 14% · délai 3.8min · rebond 59% (40/67) (MFE +1.38%)
   - −3.0% : fill 30min 16% · séance 34% (50/159) · gap 5% · délai 53.5min · rebond 67% (36/50) (MFE +1.65%)
   - −4.0% : fill 30min 8% · séance 22% (37/159) · gap 3% · délai 285.2min · rebond 60% (25/37) (MFE +1.23%)
   - −5.0% : fill 30min 3% · séance 14% (21/159) · gap 1% · délai 203.6min · rebond 67% (14/21) (MFE +1.36%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −1.67%) → stop au-delà de −1.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.55% (p90 −1.79%) → stop au-delà de −1.02% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.36%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=492 jambes) : jambe baissière méd −1.02% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (48/49) · rebond 53% (27/48)
      · −2.0% : fill 73% (35/49) · rebond 64% (23/35)
      · −3.0% : fill 59% (29/49) · rebond 59% (20/29)
      · −4.0% : fill 42% (23/49) · rebond 55% (16/23)
      · −5.0% : fill 31% (15/49) · rebond 63% (10/15)
   - **flat** (27 séances) :
      · −1.0% : fill 75% (21/27) · rebond 74% (15/21)
      · −2.0% : fill 32% (9/27) · rebond 56% (4/9)
      · −3.0% : fill 16% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 14% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 8% (2/27) · rebond 74% (1/2)
   - **gap-up** (83 séances) :
      · −1.0% : fill 47% (38/83) · rebond 51% (21/38)
      · −2.0% : fill 30% (23/83) · rebond 54% (13/23)
      · −3.0% : fill 21% (16/83) · rebond 78% (13/16)
      · −4.0% : fill 11% (10/83) · rebond 67% (7/10)
      · −5.0% : fill 6% (4/83) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 89% si les 15 1res min sont vertes (75 cas) · 25% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 89% si début vert vs 25% si rouge (base 52% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **89%** · continue >prix actuel 74% ; creux résiduel méd -1.09% (q20 -1.97%) → **SL/trailing à −1.97%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.33% / q75 +3.33% → **scale +2.33% / runner +3.33%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **25%** (continue à baisser 64%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.73%** (au-delà de la MAE q10 -4.73%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.27% .. +2.22%] · haut q95 +2.63% · bas q05 -2.8%
   - 60min (n=160) : retour [-2.47% .. +2.34%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.62%] · haut q95 +3.03% · bas q05 -3.8%
   - 4h (n=160) : retour [-2.71% .. +2.68%] · haut q95 +3.91% · bas q05 -3.92%
   - 6h (n=160) : retour [-3.27% .. +3.6%] · haut q95 +4.48% · bas q05 -4.42%
   - session (n=160) : retour [-5.1% .. +4.34%] · haut q95 +5.44% · bas q05 -5.7%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 1.3% / strong 3.7%) · base = 8 séances trend-up (n_eff 6.1)
- **ARMER** : fenêtre la + prédictive = **30 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 21% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.14% / p90 1.33%) · ~3.0 replis/séance, durée méd 68.37 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 40.0 min, n=24)
   - −1.0% → **100%** (reprise méd 77.51 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.33%** (p90, défaut prudent ; serré/agressif −1.14%) ; extension open→close méd +4.34% (q75 +4.76% / q95 +6.23%), MFE méd +4.72% / q90 +6.39%
   - Échelle scale-out : +4.72% (33%) / +5.59% (33%) / +6.39% (34%)
- **DÉSARMER** : repli > **−1.33%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.39% : P(retournement après) 0% (mèche méd 0.4%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.53%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.6  _(momentum baissier)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -0.136  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 17.3%
- **ATR** : 7.57 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.016  _(neutre)_
- **Vol ratio** : 1.86  _(volume au-dessus de la moyenne)_
- **Choppiness** : 51.4  _(transition)_
- **MA** : MA20 157.0 · MA50 161.19 · MA200 143.17  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -5.5% · MA200 +6.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94901 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
