# SOI

**Generated** : 2026-07-22T21:44:16.877567+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €96.02  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €96.02 (+8.7% vs entrée) · entrée €88.31 · stop €85.75 · T1 €91.27 · R/R 1.16  
> ↳ P(T1 av. stop) 45 % · EV/risk 0.037 · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.89% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -30 % hors [0,100] (R² max 0.12). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €87.71–€88.90 (mid €88.31)
- Spot actuel : €96.02 (+8.7% au-dessus de la zone — repli à attendre)
- Stop : €85.75 (stop swing_plan-based (-20.77%))
- Targets : T1 €91.27 · R/R 1.16 | T2 €94.23 · R/R 2.31 | T3 €97.20 · R/R 3.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €85.75


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : €0.095 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 38 % | T3 38 %
- Kelly (position) : f* 0.086 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.8 | bear 31.4 | side 59.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 96.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→68% · +3.0%→56% · +5.0%→44% · +8.0%→21%
- Range intraday médian 9.09% (p90 17.62%) · excursion haute méd. +3.68% / basse méd. −3.47%
- Profil de vol intra : ouverture 5.775% vs midi 1.688% vs clôture 2.578% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.086)_ ; drift intra méd. -0.417% ; recovery-V 38%
- **σ réalisé intraday** 5.452% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 65% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 90.1718 (VA 88.7678–93.1553 ; dernier close 95.48)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 44% · rebond 79% · **stop −7.26%** sous le fill (sous le bruit) · cible +2.85% · R/R 0.39 (high win-rate)
- Gaps overnight (n=136) : méd. 0.08% · baisse 48% (gap-down >1% 32% · >2% 24%)
- Excursion ouverture 5min (n=137) : bas méd −1.24% (p90 −3.53%) · haut méd +1.02% · range méd 3.12%
- Excursion ouverture 15min (n=137) : bas méd −1.53% (p90 −4.89%) · haut méd +1.39% · range méd 3.81%
- Excursion ouverture 30min (n=137) : bas méd −1.71% (p90 −5.32%) · haut méd +1.83% · range méd 4.36%
- Excursion ouverture 60min (n=137) : bas méd −1.91% (p90 −5.87%) · haut méd +1.95% · range méd 4.83%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 95.48 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (107/136) · gap 40% · délai 0.0min · rebond 62% (69/107) (MFE +1.9%)
   - −1.0% : fill 30min 62% · séance 75% (102/136) · gap 32% · délai 0.1min · rebond 69% (73/102) (MFE +1.83%)
   - −1.5% : fill 30min 58% · séance 71% (93/136) · gap 29% · délai 0.2min · rebond 73% (68/93) (MFE +2.18%)
   - −2.0% : fill 30min 53% · séance 66% (86/136) · gap 24% · délai 0.2min · rebond 76% (68/86) (MFE +2.67%)
   - −3.0% : fill 30min 41% · séance 56% (71/136) · gap 18% · délai 1.0min · rebond 74% (56/71) (MFE +2.81%)
   - −4.0% : fill 30min 31% · séance 47% (57/136) · gap 7% · délai 4.5min · rebond 74% (45/57) (MFE +2.45%)
   - −5.0% : fill 30min 24% · séance 44% (50/136) · gap 2% · délai 18.3min · rebond 79% (42/50) (MFE +2.85%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −3.79%) → stop au-delà de −2.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −3.17%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −3.2%) → stop au-delà de −2.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1200 jambes) : jambe baissière méd −1.32% (p90 −3.15%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 97% (52/53) · rebond 58% (32/52)
      · −2.0% : fill 93% (50/53) · rebond 72% (39/50)
      · −3.0% : fill 83% (42/53) · rebond 74% (34/42)
      · −4.0% : fill 74% (37/53) · rebond 77% (30/37)
      · −5.0% : fill 70% (33/53) · rebond 85% (28/33)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (66 séances) :
      · −1.0% : fill 46% (33/66) · rebond 84% (27/33)
      · −2.0% : fill 31% (21/66) · rebond 82% (17/21)
      · −3.0% : fill 28% (18/66) · rebond 80% (14/18)
      · −4.0% : fill 19% (12/66) · rebond 68% (9/12)
      · −5.0% : fill 17% (9/66) · rebond 59% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 52% en base · 71% si les 15 1res min sont vertes (63 cas) · 32% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=137) : COUDE à **36min** → P(séance verte=clôture>ouverture) 79% si début vert vs 25% si rouge (base 52% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **79%** · continue >prix actuel 58% ; creux résiduel méd -2.55% (q20 -5.52%) → **SL/trailing à −5.52%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.67% / q75 +5.91% → **scale +2.67% / runner +5.91%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **25%** (continue à baisser 61%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.63%** (au-delà de la MAE q10 -8.63%), cible rebond +2.09% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-5.34% .. +6.82%] · haut q95 +7.22% · bas q05 -6.37%
   - 60min (n=137) : retour [-6.11% .. +7.41%] · haut q95 +8.65% · bas q05 -6.77%
   - 2h (n=137) : retour [-6.78% .. +10.18%] · haut q95 +12.06% · bas q05 -8.2%
   - 4h (n=137) : retour [-7.21% .. +11.29%] · haut q95 +13.2% · bas q05 -8.51%
   - 6h (n=137) : retour [-8.69% .. +12.08%] · haut q95 +14.18% · bas q05 -10.47%
   - session (n=137) : retour [-12.03% .. +13.89%] · haut q95 +16.49% · bas q05 -13.98%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.6% des séances sont trend-up (mild 0% / strong 6.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 6% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.08% (p75 1.67% / p90 2.95%) · ~6.0 replis/séance, durée méd 38.95 min. P(nouveau plus-haut après repli) :
   - −0.5% → **94%** (reprise méd 20.0 min, n=57)
   - −1.0% → **92%** (reprise méd 34.22 min, n=33)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.95%** (p90, défaut prudent ; serré/agressif −1.67%) ; extension open→close méd +10.12% (q75 +13.85% / q95 +17.31%), MFE méd +10.12% / q90 +18.28%
   - Échelle scale-out : +10.12% (33%) / +16.57% (33%) / +18.28% (34%)
- **DÉSARMER** : repli > **−2.95%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.28% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +3.01%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 38.8  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist 0.035  _(bullish_recent)_
- **BB** : %B 0.32 · largeur 41.1%
- **ATR** : 8.51 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.024  _(neutre)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 44.2  _(transition)_
- **MA** : MA20 103.73 · MA50 129.36 · MA200 68.74  _(prix < MA20)_
- **Dist MA** : MA20 -7.4% · MA50 -25.8% · MA200 +39.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98181 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
