# PLTR

**Generated** : 2026-06-30T21:51:12.418439+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $116.67  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $116.67 (+5.3% vs entrée) · entrée $110.79 · stop $101.93 · T1 $112.90 · R/R 0.24  
> ↳ P(T1 av. stop) 41 % · EV/risk -0.04 · ¼-Kelly 0.052 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $110.37–$111.22 (mid $110.79)
- Spot actuel : $116.67 (+5.3% au-dessus de la zone — repli à attendre)
- Stop : $101.93 (stop swing_plan-based (-11.98%))
- Targets : T1 $112.90 · R/R 0.24 | T2 $115.01 · R/R 0.48 | T3 $117.11 · R/R 0.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $101.93


## Edge, scénarios & sizing

- EV/risk : -0.04 | EV/share : $-0.357 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 10 % | T3 5 %
- Kelly (position) : f* 0.209 | ¼-Kelly 0.052 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.2 | bear 10.0 | side 71.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→38% · +3.0%→19% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.89% (p90 6.99%) · excursion haute méd. +1.69% / basse méd. −1.71%
- Profil de vol intra : ouverture 2.831% vs midi 0.732% vs clôture 0.807% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑0%/↓1% ; spike-down 56% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr 0.001)_ ; drift intra méd. -0.486% ; recovery-V 21%
- **σ réalisé intraday** 2.679% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 56% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 116.3914 (VA 115.4441–116.8124 ; dernier close 115.66)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 49% · **stop −2.89%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 56% (gap-down >1% 31% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.84% (p90 −1.97%) · haut méd +0.85% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.79%) · haut méd +1.05% · range méd 2.22%
- Excursion ouverture 30min (n=160) : bas méd −1.25% (p90 −3.56%) · haut méd +1.23% · range méd 2.62%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −3.91%) · haut méd +1.48% · range méd 3.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 115.66 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (116/159) · gap 42% · délai 0.0min · rebond 53% (63/116) (MFE +1.06%)
   - −1.0% : fill 30min 59% · séance 72% (108/159) · gap 31% · délai 0.0min · rebond 61% (63/108) (MFE +1.32%)
   - −1.5% : fill 30min 49% · séance 62% (90/159) · gap 22% · délai 1.1min · rebond 64% (56/90) (MFE +1.37%)
   - −2.0% : fill 30min 42% · séance 53% (75/159) · gap 15% · délai 4.2min · rebond 61% (47/75) (MFE +1.43%)
   - −3.0% : fill 30min 20% · séance 36% (54/159) · gap 4% · délai 21.1min · rebond 45% (25/54) (MFE +0.85%)
   - −4.0% : fill 30min 13% · séance 25% (39/159) · gap 3% · délai 28.5min · rebond 41% (18/39) (MFE +0.83%)
   - −5.0% : fill 30min 10% · séance 19% (27/159) · gap 2% · délai 26.4min · rebond 49% (14/27) (MFE +0.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.33% (p90 −1.77%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.39%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.38%) → stop au-delà de −1.34% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=544 jambes) : jambe baissière méd −1.09% (p90 −2.72%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 97% (63/66) · rebond 64% (39/63)
      · −2.0% : fill 81% (52/66) · rebond 61% (35/52)
      · −3.0% : fill 57% (37/66) · rebond 38% (18/37)
      · −4.0% : fill 43% (27/66) · rebond 37% (12/27)
      · −5.0% : fill 36% (20/66) · rebond 51% (10/20)
   - **flat** (33 séances) :
      · −1.0% : fill 83% (26/33) · rebond 42% (14/26)
      · −2.0% : fill 55% (13/33) · rebond 70% (8/13)
      · −3.0% : fill 43% (11/33) · rebond 75% (6/11)
      · −4.0% : fill 22% (8/33) · rebond 71% (5/8)
      · −5.0% : fill 5% (4/33) · rebond 63% (3/4)
   - **gap-up** (60 séances) :
      · −1.0% : fill 33% (19/60) · rebond 72% (10/19)
      · −2.0% : fill 15% (10/60) · rebond 42% (4/10)
      · −3.0% : fill 5% (6/60) · rebond 14% (1/6)
      · −4.0% : fill 3% (4/60) · rebond 18% (1/4)
      · −5.0% : fill 3% (3/60) · rebond 12% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 60% si les 15 1res min sont vertes (79 cas) · 31% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:30** → P(séance verte=clôture>ouverture) 90% si début vert vs 11% si rouge (base 46% · écart 79 pts) ; prédictivité sature ensuite (plafond brut 149min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **90%** · continue >prix actuel 51% ; creux résiduel méd -0.73% (q20 -1.66%) → **SL/trailing à −1.66%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.83% / q75 +1.41% → **scale +0.83% / runner +1.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **11%** (continue à baisser 50%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.44%** (au-delà de la MAE q10 -2.44%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.02% .. +2.48%] · haut q95 +3.1% · bas q05 -4.23%
   - 60min (n=160) : retour [-3.49% .. +2.86%] · haut q95 +3.46% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.74% .. +3.29%] · haut q95 +4.04% · bas q05 -4.5%
   - 4h (n=160) : retour [-4.47% .. +3.57%] · haut q95 +4.56% · bas q05 -5.55%
   - 6h (n=160) : retour [-5.07% .. +3.88%] · haut q95 +4.69% · bas q05 -5.62%
   - session (n=160) : retour [-4.98% .. +3.83%] · haut q95 +4.57% · bas q05 -5.69%


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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.67 · part idiosyncratique 0.33
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.4  _(momentum baissier)_
- **ADX** : 23.1  _(pas de tendance nette)_
- **MACD** : hist -1.492  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 36.3%
- **ATR** : 5.88 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.264  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 38.6  _(transition)_
- **MA** : MA20 127.94 · MA50 135.32 · MA200 158.35  _(prix < MA20)_
- **Dist MA** : MA20 -8.8% · MA50 -13.8% · MA200 -26.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89712 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
