# MSTR

**Generated** : 2026-06-30T00:12:42.394474+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $92.68  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $92.68 (+11.7% vs entrée) · entrée $82.94 · stop $76.31 · T1 $85.73 · R/R 0.42  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.1 · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -24 % hors [0,100] (R² max 0.04). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $82.38–$83.50 (mid $82.94)
- Spot actuel : $92.68 (+11.7% au-dessus de la zone — repli à attendre)
- Stop : $76.31 (stop swing_plan-based (-24.17%))
- Targets : T1 $85.73 · R/R 0.42 | T2 $88.52 · R/R 0.84 | T3 $91.31 · R/R 1.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $76.31


## Edge, scénarios & sizing

- EV/risk : -0.1 | EV/share : $-0.666 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.077 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.9 | bear 80.2 | side 10.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→51% · +3.0%→31% · +5.0%→10% · +8.0%→4%
- Range intraday médian 5.18% (p90 9.24%) · excursion haute méd. +2.12% / basse méd. −2.89%
- Profil de vol intra : ouverture 3.148% vs midi 1.199% vs clôture 1.229% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.014)_ ; drift intra méd. -1.93% ; recovery-V 26%
- **σ réalisé intraday** 3.96% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 77% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 85.0756 (VA 84.0659–86.6624 ; dernier close 81.92)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 69% · **stop −5.24%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.27 (high win-rate)
- Gaps overnight (n=159) : méd. -0.32% · baisse 57% (gap-down >1% 41% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.95% (p90 −2.09%) · haut méd +0.57% · range méd 1.82%
- Excursion ouverture 15min (n=160) : bas méd −1.19% (p90 −3.03%) · haut méd +0.82% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.87%) · haut méd +1.06% · range méd 3.01%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −4.96%) · haut méd +1.45% · range méd 3.66%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 81.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 81% (127/159) · gap 48% · délai 0.0min · rebond 48% (63/127) (MFE +0.96%)
   - −1.0% : fill 30min 66% · séance 78% (122/159) · gap 41% · délai 0.0min · rebond 55% (68/122) (MFE +1.39%)
   - −1.5% : fill 30min 58% · séance 74% (114/159) · gap 29% · délai 0.0min · rebond 55% (67/114) (MFE +1.35%)
   - −2.0% : fill 30min 50% · séance 66% (102/159) · gap 24% · délai 1.3min · rebond 56% (64/102) (MFE +1.23%)
   - −3.0% : fill 30min 34% · séance 54% (78/159) · gap 14% · délai 9.4min · rebond 53% (47/78) (MFE +1.43%)
   - −4.0% : fill 30min 22% · séance 46% (64/159) · gap 6% · délai 38.8min · rebond 55% (39/64) (MFE +1.08%)
   - −5.0% : fill 30min 16% · séance 34% (49/159) · gap 3% · délai 58.2min · rebond 69% (35/49) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.89% (p90 −2.77%) → stop au-delà de −1.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −2.84%) → stop au-delà de −2.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.14% (p90 −2.8%) → stop au-delà de −2.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=970 jambes) : jambe baissière méd −1.22% (p90 −2.83%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 48% (36/73)
      · −2.0% : fill 89% (66/74) · rebond 50% (38/66)
      · −3.0% : fill 79% (57/74) · rebond 55% (35/57)
      · −4.0% : fill 67% (47/74) · rebond 58% (31/47)
      · −5.0% : fill 54% (38/74) · rebond 71% (28/38)
   - **flat** (17 séances) :
      · −1.0% : fill 86% (16/17) · rebond 77% (10/16)
      · −2.0% : fill 64% (13/17) · rebond 55% (9/13)
      · −3.0% : fill 44% (9/17) · rebond 36% (5/9)
      · −4.0% : fill 41% (7/17) · rebond 12% (2/7)
      · −5.0% : fill 32% (5/17) · rebond 15% (2/5)
   - **gap-up** (68 séances) :
      · −1.0% : fill 50% (33/68) · rebond 62% (22/33)
      · −2.0% : fill 38% (23/68) · rebond 71% (17/23)
      · −3.0% : fill 25% (12/68) · rebond 55% (7/12)
      · −4.0% : fill 22% (10/68) · rebond 67% (6/10)
      · −5.0% : fill 11% (6/68) · rebond 93% (5/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 46% si les 15 1res min sont vertes (73 cas) · 35% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 69% si début vert vs 19% si rouge (base 40% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **69%** · continue >prix actuel 48% ; creux résiduel méd -1.78% (q20 -3.6%) → **SL/trailing à −3.6%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.52% / q75 +2.74% → **scale +1.52% / runner +2.74%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **19%** (continue à baisser 65%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.36%** (au-delà de la MAE q10 -5.36%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +3.32%] · haut q95 +4.0% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.13% .. +3.4%] · haut q95 +4.83% · bas q05 -5.58%
   - 2h (n=160) : retour [-4.84% .. +5.2%] · haut q95 +5.79% · bas q05 -5.67%
   - 4h (n=160) : retour [-7.88% .. +4.92%] · haut q95 +7.71% · bas q05 -8.41%
   - 6h (n=160) : retour [-7.2% .. +4.94%] · haut q95 +7.83% · bas q05 -8.69%
   - session (n=160) : retour [-6.23% .. +5.21%] · haut q95 +7.83% · bas q05 -8.69%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0.6% / strong 4.4%) · base = 8 séances trend-up (n_eff 5.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 12% vs absente 0% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.43% (p75 2.0% / p90 3.04%) · ~3.0 replis/séance, durée méd 47.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 18.34 min, n=28)
   - −1.0% → **73%** (reprise méd 35.0 min, n=17)
   - −1.5% → **61%** (reprise méd 58.02 min, n=11)
   - −2.0% → **30%** (reprise méd None min, n=6)
   - −3.0% → **59%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−3.04%** (p90, défaut prudent ; serré/agressif −2.0%) ; extension open→close méd +5.97% (q75 +7.52% / q95 +15.37%), MFE méd +7.89% / q90 +14.64%
   - Échelle scale-out : +7.89% (33%) / +9.95% (33%) / +14.64% (34%)
- **DÉSARMER** : repli > **−3.04%** depuis le plus-haut = décay → P(retournement) **41%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.64% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +1.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.57 · part idiosyncratique 0.42
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.1  _(momentum baissier)_
- **ADX** : 32.1  _(tendance etablie)_
- **MACD** : hist -2.471  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 59.5%
- **ATR** : 9.74 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.336  _(distribution)_
- **Vol ratio** : 1.6  _(volume au-dessus de la moyenne)_
- **Choppiness** : 34.8  _(marche directionnel)_
- **MA** : MA20 115.83 · MA50 149.42 · MA200 184.78  _(prix < MA20)_
- **Dist MA** : MA20 -20.0% · MA50 -38.0% · MA200 -49.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89996 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
