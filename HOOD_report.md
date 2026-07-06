# HOOD

**Generated** : 2026-07-06T00:21:07.358289+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $112.73  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $112.73 (+3.6% vs entrée) · entrée $108.80 · stop $105.53 · T1 $111.52 · R/R 0.83  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.023 _(réel 5 s)_ (GBM 0.063) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 157 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $108.25–$109.34 (mid $108.80)
- Spot actuel : $112.73 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : $105.53 (stop swing_plan-based (-10.25%))
- Targets : T1 $111.52 · R/R 0.83 | T2 $114.24 · R/R 1.66 | T3 $116.96 · R/R 2.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $105.53


## Edge, scénarios & sizing

- EV/risk : 0.063 | EV/share : $0.206 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 20 % | T3 20 %
- Kelly (position) : f* 0.05 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 64.2 | bear 12.1 | side 23.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 564.0 (= 5 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.484% → cible +2.501% / stop −3.0%, p_fill 29%, n_eff≈12.8) : P(cible|rempli) **27%** · **EV/risk -0.023** (×p_fill ; si rempli -0.24% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→54% · +3.0%→38% · +5.0%→20% · +8.0%→6%
- Range intraday médian 4.94% (p90 8.79%) · excursion haute méd. +2.11% / basse méd. −2.15%
- Profil de vol intra : ouverture 3.406% vs midi 1.072% vs clôture 1.035% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 19% · trend ↑1%/↓0% ; spike-down 65% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; momentum — autocorr 0.046)_ ; drift intra méd. 0.808% ; recovery-V 35%
- **σ réalisé intraday** 3.831% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 48% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 112.4111 (VA 111.2949–113.9739 ; dernier close 112.73)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 86% · **stop −4.75%** sous le fill (sous le bruit) · cible +2.38% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 50% (gap-down >1% 30% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −1.89%) · haut méd +0.85% · range méd 1.98%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.97%) · haut méd +1.04% · range méd 2.58%
- Excursion ouverture 30min (n=160) : bas méd −1.3% (p90 −3.66%) · haut méd +1.45% · range méd 3.26%
- Excursion ouverture 60min (n=160) : bas méd −1.56% (p90 −3.84%) · haut méd +1.68% · range méd 3.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 112.73 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 75% (120/159) · gap 38% · délai 0.0min · rebond 56% (61/120) (MFE +1.39%)
   - −1.0% : fill 30min 54% · séance 63% (105/159) · gap 30% · délai 0.0min · rebond 59% (59/105) (MFE +1.28%)
   - −1.5% : fill 30min 47% · séance 60% (98/159) · gap 22% · délai 0.3min · rebond 54% (53/98) (MFE +1.27%)
   - −2.0% : fill 30min 40% · séance 54% (88/159) · gap 16% · délai 1.0min · rebond 62% (52/88) (MFE +1.3%)
   - −3.0% : fill 30min 30% · séance 40% (66/159) · gap 8% · délai 10.7min · rebond 66% (42/66) (MFE +1.69%)
   - −4.0% : fill 30min 20% · séance 31% (51/159) · gap 4% · délai 12.3min · rebond 74% (33/51) (MFE +1.99%)
   - −5.0% : fill 30min 12% · séance 20% (33/159) · gap 2% · délai 21.4min · rebond 86% (27/33) (MFE +2.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −2.58%) → stop au-delà de −1.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −2.48%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.43%) → stop au-delà de −1.71% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=748 jambes) : jambe baissière méd −1.16% (p90 −2.71%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 95% (66/70) · rebond 52% (34/66)
      · −2.0% : fill 85% (57/70) · rebond 56% (32/57)
      · −3.0% : fill 71% (46/70) · rebond 61% (28/46)
      · −4.0% : fill 58% (38/70) · rebond 79% (27/38)
      · −5.0% : fill 42% (28/70) · rebond 84% (23/28)
   - **flat** (23 séances) :
      · −1.0% : fill 70% (17/23) · rebond 76% (12/17)
      · −2.0% : fill 54% (12/23) · rebond 59% (7/12)
      · −3.0% : fill 18% (6/23) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/23) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/23) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 31% (22/66) · rebond 64% (13/22)
      · −2.0% : fill 26% (19/66) · rebond 82% (13/19)
      · −3.0% : fill 20% (14/66) · rebond 95% (12/14)
      · −4.0% : fill 11% (8/66) · rebond 81% (5/8)
      · −5.0% : fill 4% (2/66) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 68% si les 15 1res min sont vertes (71 cas) · 38% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 84% si début vert vs 19% si rouge (base 51% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **84%** · continue >prix actuel 54% ; creux résiduel méd -1.39% (q20 -2.86%) → **SL/trailing à −2.86%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.95% / q75 +3.27% → **scale +0.95% / runner +3.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **19%** (continue à baisser 60%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.48% .. +4.84%] · haut q95 +5.3% · bas q05 -4.4%
   - 60min (n=160) : retour [-3.58% .. +4.93%] · haut q95 +6.39% · bas q05 -4.76%
   - 2h (n=160) : retour [-4.07% .. +6.62%] · haut q95 +7.63% · bas q05 -5.49%
   - 4h (n=160) : retour [-4.63% .. +7.7%] · haut q95 +8.58% · bas q05 -6.1%
   - 6h (n=160) : retour [-5.3% .. +7.68%] · haut q95 +8.58% · bas q05 -6.44%
   - session (n=160) : retour [-5.02% .. +7.72%] · haut q95 +8.78% · bas q05 -6.8%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **38%**. Lecture précoce 30 min : signature présente → 19% vs absente 5% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.42% / p90 2.29%) · ~3.81 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **84%** (reprise méd 20.0 min, n=49)
   - −1.0% → **67%** (reprise méd 30.0 min, n=22)
   - −1.5% → **32%** (reprise méd 35.94 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.29%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.1% (q75 +9.8% / q95 +13.38%), MFE méd +7.16% / q90 +15.08%
   - Échelle scale-out : +7.16% (33%) / +12.41% (33%) / +15.08% (34%)
- **DÉSARMER** : repli > **−2.29%** depuis le plus-haut = décay → P(retournement) **71%** (préavis méd 134.36 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +15.08% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 75% du temps (retour médian dernière heure +0.99%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 68.4  _(momentum haussier)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist 0.726  _(bullish_recent)_
- **BB** : %B 0.94 · largeur 36.6%
- **ATR** : 7.37 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.016  _(neutre)_
- **Vol ratio** : 1.2  _(volume normal)_
- **Choppiness** : 47.0  _(transition)_
- **MA** : MA20 97.07 · MA50 86.58 · MA200 102.37  _(prix > MA20)_
- **Dist MA** : MA20 +16.1% · MA50 +30.2% · MA200 +10.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94254 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
