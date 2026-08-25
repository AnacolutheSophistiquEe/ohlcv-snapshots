# 298040

**Generated** : 2026-08-25T21:54:43.290628+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · ₩2736000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2736000.00 (+1.7% vs entrée) · entrée ₩2689721.22 · stop ₩2502935.51 · T1 ₩2971794.14 · R/R 1.51  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.061 _(réel 5 s)_ (GBM 0.2) · ¼-Kelly 0.014 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2643442.44–₩2736000.00 (mid ₩2689721.22)
- Spot actuel : ₩2736000.00 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : ₩2502935.51 (stop swing_plan-based (-8.52%))
- Targets : T1 ₩2971794.14 · R/R 1.51 | T2 ₩3253867.06 · R/R 3.02 | T3 ₩3535939.99 · R/R 4.53
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2502935.51


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.04 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.52 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **3.166 pt plus bas** dans le cas TYPIQUE (médiane), 3.166 au p90, **3.166 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 8.52 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0026 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.44 % | p01 -4.603 % | pire -11.686 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.091** [0.0549 ; 0.1406] _(largeur 8.6 pt, n_eff 173.1)_
   - swing : **0.399** [0.3484 ; 0.4513] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.3826** [0.3325 ; 0.4346] _(largeur 10.2 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : swing (30.3 pt), deep (30.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.91 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 3.72 % contre 6.03 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.9 % vs -12.54 % si l'on extrapolait par √5 _(rapport 0.949 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0759** (β de hausse 0.9726, asymétrie 1.1063) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.2 | EV/share : ₩37258.481 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 8 % | T3 2 %
- Kelly (position) : f* 0.058 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 7.3 | bear 76.6 | side 16.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.761% → cible +12.103% / stop −8.0%, p_fill 96%, n_eff≈38.6) : P(cible|rempli) **3%** · **EV/risk -0.152** (×p_fill ; si rempli -1.27% du capital)
  - **swing** (entrée dip −1.693% → cible +10.487% / stop −6.944%, p_fill 97%, n_eff≈38.9) : P(cible|rempli) **25%** · **EV/risk -0.061** (×p_fill ; si rempli -0.44% du capital)
  - **deep** (entrée dip −2.47% → cible +14.831% / stop −10.499%, p_fill 98%, n_eff≈38.6) : P(cible|rempli) **26%** · **EV/risk -0.254** (×p_fill ; si rempli -2.72% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→60% · +2.0%→51% · +3.0%→39% · +5.0%→22% · +8.0%→6%
- Range intraday médian 7.04% (p90 10.6%) · excursion haute méd. +2.13% / basse méd. −4.19%
- Profil de vol intra : ouverture 4.528% vs midi 1.157% vs clôture 1.222% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 24% · trend ↑0%/↓1% ; spike-down 82% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. -1.572% ; recovery-V 25%
- **σ réalisé intraday** 4.595% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 38% / bas 62% / whipsaw 6%
- POC intraday (dernière séance, temps-au-prix) : 2720562.5 (VA 2711937.5–2734937.5 ; dernier close 2720000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 41% · rebond 72% · **stop −5.54%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.4 (high win-rate)
- Gaps overnight (n=158) : méd. 0.92% · baisse 34% (gap-down >1% 24% · >2% 17%)
- Excursion ouverture 5min (n=159) : bas méd −1.48% (p90 −3.44%) · haut méd +0.74% · range méd 2.63%
- Excursion ouverture 15min (n=159) : bas méd −1.94% (p90 −4.32%) · haut méd +0.87% · range méd 3.36%
- Excursion ouverture 30min (n=159) : bas méd −2.46% (p90 −4.91%) · haut méd +0.94% · range méd 4.13%
- Excursion ouverture 60min (n=159) : bas méd −2.58% (p90 −5.32%) · haut méd +1.36% · range méd 4.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2721000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 67% (105/158) · gap 30% · délai 0.1min · rebond 56% (65/105) (MFE +1.13%)
   - −1.0% : fill 30min 55% · séance 62% (97/158) · gap 24% · délai 0.1min · rebond 57% (59/97) (MFE +1.35%)
   - −1.5% : fill 30min 50% · séance 58% (89/158) · gap 21% · délai 2.3min · rebond 57% (56/89) (MFE +1.28%)
   - −2.0% : fill 30min 46% · séance 55% (79/158) · gap 17% · délai 3.6min · rebond 56% (45/79) (MFE +1.47%)
   - −3.0% : fill 30min 32% · séance 48% (66/158) · gap 8% · délai 10.1min · rebond 66% (43/66) (MFE +1.46%)
   - −4.0% : fill 30min 23% · séance 41% (56/158) · gap 6% · délai 25.4min · rebond 72% (42/56) (MFE +2.23%)
   - −5.0% : fill 30min 17% · séance 36% (44/158) · gap 6% · délai 59.5min · rebond 72% (32/44) (MFE +1.96%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −3.16%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −3.28%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −3.47%) → stop au-delà de −2.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=858 jambes) : jambe baissière méd −1.41% (p90 −3.47%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 100% (51/51) · rebond 55% (31/51)
      · −2.0% : fill 90% (42/51) · rebond 46% (22/42)
      · −3.0% : fill 89% (41/51) · rebond 63% (26/41)
      · −4.0% : fill 87% (37/51) · rebond 74% (27/37)
      · −5.0% : fill 76% (31/51) · rebond 81% (24/31)
   - **flat** (17 séances) :
      · −1.0% : fill 91% (13/17) · rebond 70% (9/13)
      · −2.0% : fill 87% (12/17) · rebond 51% (6/12)
      · −3.0% : fill 60% (8/17) · rebond 59% (5/8)
      · −4.0% : fill 48% (7/17) · rebond 44% (5/7)
      · −5.0% : fill 35% (3/17) · rebond 24% (1/3)
   - **gap-up** (90 séances) :
      · −1.0% : fill 36% (33/90) · rebond 53% (19/33)
      · −2.0% : fill 31% (25/90) · rebond 76% (17/25)
      · −3.0% : fill 23% (17/90) · rebond 75% (12/17)
      · −4.0% : fill 14% (12/90) · rebond 79% (10/12)
      · −5.0% : fill 13% (10/90) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 34% en base · 53% si les 15 1res min sont vertes (63 cas) · 24% si rouges (96 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=159) : COUDE à **46min** → P(séance verte=clôture>ouverture) 74% si début vert vs 13% si rouge (base 34% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **74%** · continue >prix actuel 46% ; creux résiduel méd -1.83% (q20 -3.92%) → **SL/trailing à −3.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +3.91% → **scale +1.78% / runner +3.91%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **13%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.94%** (au-delà de la MAE q10 -5.94%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-4.28% .. +4.24%] · haut q95 +6.12% · bas q05 -5.34%
   - 60min (n=159) : retour [-5.25% .. +4.8%] · haut q95 +6.57% · bas q05 -6.06%
   - 2h (n=159) : retour [-6.98% .. +4.45%] · haut q95 +6.76% · bas q05 -8.03%
   - 4h (n=159) : retour [-7.56% .. +5.3%] · haut q95 +7.39% · bas q05 -9.25%
   - 6h (n=159) : retour [-7.6% .. +5.24%] · haut q95 +8.33% · bas q05 -9.3%
   - session (n=159) : retour [-7.47% .. +5.56%] · haut q95 +8.33% · bas q05 -9.39%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **54%**. Lecture précoce 30 min : signature présente → 20% vs absente 0% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 52.5  _(neutre)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist 15117.206  _(pas de croisement recent)_
- **BB** : %B 0.53 · largeur 47.2%
- **ATR** : 186785.71 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.06  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 65.9  _(marche en range (choppy))_
- **MA** : MA20 2697100.0 · MA50 2974600.0 · MA200 2734086.12  _(prix > MA20)_
- **Dist MA** : MA20 +1.4% · MA50 -8.0% · MA200 +0.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (540028 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
