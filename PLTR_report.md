# PLTR

**Generated** : 2026-06-29T21:51:04.722560+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $115.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $115.70 (+5.7% vs entrée) · entrée $109.43 · stop $100.68 · T1 $111.56 · R/R 0.24  
> ↳ P(T1 av. stop) 38 % · EV/risk -0.041 · ¼-Kelly 0.048 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $109.00–$109.86 (mid $109.43)
- Spot actuel : $115.70 (+5.7% au-dessus de la zone — repli à attendre)
- Stop : $100.68 (stop swing_plan-based (-12.78%))
- Targets : T1 $111.56 · R/R 0.24 | T2 $113.69 · R/R 0.49 | T3 $115.82 · R/R 0.73
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $100.68


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : $-0.361 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 9 % | T3 5 %
- Kelly (position) : f* 0.193 | ¼-Kelly 0.048 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.6 | bear 71.1 | side 10.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→36% · +3.0%→19% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.89% (p90 6.99%) · excursion haute méd. +1.69% / basse méd. −1.73%
- Profil de vol intra : ouverture 2.827% vs midi 0.73% vs clôture 0.813% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑0%/↓1% ; spike-down 58% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.484% ; recovery-V 22%
- **σ réalisé intraday** 2.684% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 54% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 113.1514 (VA 112.3219–113.8426 ; dernier close 112.79)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 49% · **stop −2.89%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.23% · baisse 57% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.87% (p90 −1.97%) · haut méd +0.83% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.79%) · haut méd +1.0% · range méd 2.2%
- Excursion ouverture 30min (n=160) : bas méd −1.26% (p90 −3.59%) · haut méd +1.22% · range méd 2.61%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −3.93%) · haut méd +1.44% · range méd 3.07%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 112.79 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (117/159) · gap 43% · délai 0.0min · rebond 53% (64/117) (MFE +1.06%)
   - −1.0% : fill 30min 60% · séance 73% (109/159) · gap 32% · délai 0.0min · rebond 61% (64/109) (MFE +1.32%)
   - −1.5% : fill 30min 50% · séance 63% (91/159) · gap 22% · délai 1.0min · rebond 64% (57/91) (MFE +1.37%)
   - −2.0% : fill 30min 42% · séance 54% (76/159) · gap 16% · délai 4.3min · rebond 61% (48/76) (MFE +1.43%)
   - −3.0% : fill 30min 20% · séance 37% (55/159) · gap 4% · délai 21.3min · rebond 45% (26/55) (MFE +0.85%)
   - −4.0% : fill 30min 14% · séance 26% (39/159) · gap 3% · délai 28.5min · rebond 41% (18/39) (MFE +0.83%)
   - −5.0% : fill 30min 10% · séance 19% (27/159) · gap 2% · délai 26.4min · rebond 49% (14/27) (MFE +0.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.8%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −1.4%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.38%) → stop au-delà de −1.34% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=548 jambes) : jambe baissière méd −1.09% (p90 −2.7%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 97% (64/67) · rebond 64% (40/64)
      · −2.0% : fill 81% (53/67) · rebond 61% (36/53)
      · −3.0% : fill 57% (38/67) · rebond 39% (19/38)
      · −4.0% : fill 42% (27/67) · rebond 37% (12/27)
      · −5.0% : fill 36% (20/67) · rebond 51% (10/20)
   - **flat** (33 séances) :
      · −1.0% : fill 83% (26/33) · rebond 42% (14/26)
      · −2.0% : fill 55% (13/33) · rebond 70% (8/13)
      · −3.0% : fill 43% (11/33) · rebond 75% (6/11)
      · −4.0% : fill 22% (8/33) · rebond 71% (5/8)
      · −5.0% : fill 5% (4/33) · rebond 63% (3/4)
   - **gap-up** (59 séances) :
      · −1.0% : fill 35% (19/59) · rebond 72% (10/19)
      · −2.0% : fill 16% (10/59) · rebond 42% (4/10)
      · −3.0% : fill 5% (6/59) · rebond 14% (1/6)
      · −4.0% : fill 4% (4/59) · rebond 18% (1/4)
      · −5.0% : fill 3% (3/59) · rebond 12% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 63% si les 15 1res min sont vertes (79 cas) · 31% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:45** → P(séance verte=clôture>ouverture) 84% si début vert vs 14% si rouge (base 47% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **84%** · continue >prix actuel 52% ; creux résiduel méd -0.84% (q20 -1.64%) → **SL/trailing à −1.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.95% / q75 +1.77% → **scale +0.95% / runner +1.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **14%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.1%** (au-delà de la MAE q10 -3.1%), cible rebond +0.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.04% .. +2.48%] · haut q95 +3.13% · bas q05 -4.25%
   - 60min (n=160) : retour [-3.52% .. +2.89%] · haut q95 +3.48% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.76% .. +3.29%] · haut q95 +4.08% · bas q05 -4.5%
   - 4h (n=160) : retour [-4.47% .. +3.58%] · haut q95 +4.57% · bas q05 -5.56%
   - 6h (n=160) : retour [-5.07% .. +3.9%] · haut q95 +4.71% · bas q05 -5.64%
   - session (n=160) : retour [-4.98% .. +3.87%] · haut q95 +4.57% · bas q05 -5.73%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 3.1% / strong 1.9%) · base = 8 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **31%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.84% / p90 1.43%) · ~3.0 replis/séance, durée méd 76.74 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 30.0 min, n=25)
   - −1.0% → **39%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−1.43%** (p90, défaut prudent ; serré/agressif −0.84%) ; extension open→close méd +3.81% (q75 +4.61% / q95 +7.65%), MFE méd +4.14% / q90 +8.89%
   - Échelle scale-out : +4.14% (33%) / +6.64% (33%) / +8.89% (34%)
- **DÉSARMER** : repli > **−1.43%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.89% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.66 · part idiosyncratique 0.34
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.3  _(momentum baissier)_
- **ADX** : 22.8  _(pas de tendance nette)_
- **MACD** : hist -2.026  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 41.2%
- **ATR** : 6.27 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.243  _(distribution)_
- **Vol ratio** : 1.02  _(volume normal)_
- **Choppiness** : 39.9  _(transition)_
- **MA** : MA20 130.14 · MA50 135.92 · MA200 158.59  _(prix < MA20)_
- **Dist MA** : MA20 -11.1% · MA50 -14.9% · MA200 -27.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89310 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
