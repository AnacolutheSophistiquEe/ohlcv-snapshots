# SOI

**Generated** : 2026-08-07T21:44:38.320425+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €122.50  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €122.50 (+1.0% vs entrée) · entrée €121.31 · stop €117.97 · T1 €128.00 · R/R 2.0  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk -0.109 _(réel 5 s)_ (GBM 0.116) · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.76% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -179 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 72.0 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €120.38–€122.25 (mid €121.31)
- Spot actuel : €122.50 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : €117.97 (stop swing_plan-based (-10.71%))
- Targets : T1 €128.00 · R/R 2.0 | T2 €131.65 · R/R 3.1 | T3 €135.31 · R/R 4.19
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €117.97


## Edge, scénarios & sizing

- EV/risk : 0.116 | EV/share : €0.388 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.131 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.4 | bear 73.1 | side 21.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 490.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.97% → cible +5.513% / stop −2.756%, p_fill 84%, n_eff≈34.9) : P(cible|rempli) **24%** · **EV/risk -0.109** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −2.128% → cible +13.523% / stop −8.768%, p_fill 70%, n_eff≈29.5) : P(cible|rempli) **30%** · **EV/risk -0.060** (×p_fill ; si rempli -0.75% du capital)
  - **deep** (entrée dip −3.298% → cible +12.162% / stop −13.311%, p_fill 85%, n_eff≈34.7) : P(cible|rempli) **25%** · **EV/risk -0.407** (×p_fill ; si rempli -6.38% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→70% · +3.0%→57% · +5.0%→41% · +8.0%→20%
- Range intraday médian 9.26% (p90 16.36%) · excursion haute méd. +3.69% / basse méd. −3.82%
- Profil de vol intra : ouverture 5.908% vs midi 1.685% vs clôture 2.563% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 76% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.106)_ ; drift intra méd. -0.191% ; recovery-V 39%
- **σ réalisé intraday** 5.616% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 64% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 117.2225 (VA 117.0575–118.8725 ; dernier close 120.48)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 64% · rebond 78% · **stop −8.34%** sous le fill (sous le bruit) · cible +2.87% · R/R 0.34 (high win-rate)
- Gaps overnight (n=148) : méd. 0.09% · baisse 47% (gap-down >1% 32% · >2% 22%)
- Excursion ouverture 5min (n=149) : bas méd −1.15% (p90 −3.75%) · haut méd +1.06% · range méd 2.92%
- Excursion ouverture 15min (n=149) : bas méd −1.36% (p90 −5.05%) · haut méd +1.58% · range méd 3.79%
- Excursion ouverture 30min (n=149) : bas méd −1.53% (p90 −5.37%) · haut méd +1.87% · range méd 4.26%
- Excursion ouverture 60min (n=149) : bas méd −1.71% (p90 −5.86%) · haut méd +1.91% · range méd 4.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 120.48 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 79% (117/148) · gap 38% · délai 0.0min · rebond 64% (76/117) (MFE +2.03%)
   - −1.0% : fill 30min 59% · séance 75% (111/148) · gap 32% · délai 0.2min · rebond 71% (80/111) (MFE +1.87%)
   - −1.5% : fill 30min 56% · séance 72% (102/148) · gap 28% · délai 0.2min · rebond 74% (75/102) (MFE +2.26%)
   - −2.0% : fill 30min 50% · séance 64% (93/148) · gap 22% · délai 0.4min · rebond 78% (74/93) (MFE +2.87%)
   - −3.0% : fill 30min 37% · séance 53% (76/148) · gap 16% · délai 0.8min · rebond 75% (60/76) (MFE +2.91%)
   - −4.0% : fill 30min 29% · séance 44% (61/148) · gap 7% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 22% · séance 40% (53/148) · gap 2% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −3.79%) → stop au-delà de −2.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.77% (p90 −3.37%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −2.95%) → stop au-delà de −2.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1305 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 98% (57/58) · rebond 63% (36/57)
      · −2.0% : fill 95% (55/58) · rebond 74% (43/55)
      · −3.0% : fill 82% (46/58) · rebond 74% (37/46)
      · −4.0% : fill 71% (40/58) · rebond 81% (33/40)
      · −5.0% : fill 64% (35/58) · rebond 87% (30/35)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (73 séances) :
      · −1.0% : fill 49% (37/73) · rebond 81% (30/37)
      · −2.0% : fill 30% (23/73) · rebond 87% (19/23)
      · −3.0% : fill 24% (19/73) · rebond 83% (15/19)
      · −4.0% : fill 18% (13/73) · rebond 55% (9/13)
      · −5.0% : fill 16% (10/73) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 52% en base · 69% si les 15 1res min sont vertes (71 cas) · 32% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=149) : COUDE à **38min** → P(séance verte=clôture>ouverture) 80% si début vert vs 24% si rouge (base 52% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **80%** · continue >prix actuel 61% ; creux résiduel méd -2.6% (q20 -5.4%) → **SL/trailing à −5.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.53% / q75 +4.75% → **scale +3.53% / runner +4.75%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **24%** (continue à baisser 66%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.82%** (au-delà de la MAE q10 -8.82%), cible rebond +2.73% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-5.23% .. +7.0%] · haut q95 +7.84% · bas q05 -6.55%
   - 60min (n=149) : retour [-5.93% .. +7.08%] · haut q95 +9.2% · bas q05 -6.97%
   - 2h (n=149) : retour [-6.03% .. +9.93%] · haut q95 +12.37% · bas q05 -7.59%
   - 4h (n=149) : retour [-6.85% .. +10.14%] · haut q95 +14.05% · bas q05 -8.14%
   - 6h (n=149) : retour [-7.69% .. +10.73%] · haut q95 +14.24% · bas q05 -9.62%
   - session (n=149) : retour [-11.18% .. +13.71%] · haut q95 +15.61% · bas q05 -12.85%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.0% des séances sont trend-up (mild 0% / strong 6.0%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 5% vs absente 5% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.08% (p75 1.67% / p90 2.95%) · ~6.0 replis/séance, durée méd 38.95 min. P(nouveau plus-haut après repli) :
   - −0.5% → **94%** (reprise méd 20.0 min, n=57)
   - −1.0% → **92%** (reprise méd 34.22 min, n=33)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.95%** (p90, défaut prudent ; serré/agressif −1.67%) ; extension open→close méd +10.12% (q75 +13.85% / q95 +17.31%), MFE méd +10.12% / q90 +18.28%
   - Échelle scale-out : +10.12% (33%) / +16.57% (33%) / +18.28% (34%)
- **DÉSARMER** : repli > **−2.95%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.28% : P(retournement après) 0% (mèche méd 1.42%)
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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 72.0  _(surachat)_
- **ADX** : 17.1  _(pas de tendance nette)_
- **MACD** : hist 3.639  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 44.6%
- **ATR** : 10.51 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.016  _(neutre)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 44.7  _(transition)_
- **MA** : MA20 104.14 · MA50 118.49 · MA200 72.63  _(prix > MA20)_
- **Dist MA** : MA20 +17.6% · MA50 +3.4% · MA200 +68.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (100265 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
