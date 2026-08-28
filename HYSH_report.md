# 298040

**Generated** : 2026-08-28T21:54:28.923463+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩3140000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩3140000.00 (+0.8% vs entrée) · entrée ₩3115770.22 · stop ₩2866508.60 · T1 ₩3237291.86 · R/R 0.49  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.041 _(réel 5 s)_ (GBM -0.151) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 151 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩3091540.44–₩3140000.00 (mid ₩3115770.22)
- Spot actuel : ₩3140000.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : ₩2866508.60 (stop swing_plan-based (-7.04%))
- Targets : T1 ₩3237291.86 · R/R 0.49 | T2 ₩3358813.49 · R/R 0.98 | T3 ₩3480335.13 · R/R 1.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2866508.60


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.04 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.04 %)** : le gap seul le franchit 0.164 % des séances (2 fois sur 1218).
   - exécution **2.543 pt plus bas** dans le cas TYPIQUE (médiane), 4.226 au p90, **4.646 au pire**
   - perte réelle **9.583 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 7.04 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0042 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.44 % | p01 -4.603 % | pire -11.686 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0845** [0.0499 ; 0.1329] _(largeur 8.3 pt, n_eff 173.1)_
   - swing : **0.5108** [0.4582 ; 0.5632] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4423** [0.3906 ; 0.495] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (28.0 pt), swing (29.6 pt), deep (30.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.94 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.61 % contre 5.90 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.9 % vs -12.54 % si l'on extrapolait par √5 _(rapport 0.949 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0771** (β de hausse 0.9851, asymétrie 1.0934) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.151 | EV/share : ₩-37594.481 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 19 % | T3 19 %
- Kelly (position) : f* 0.058 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 47.8 | bear 26.7 | side 25.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.772% → cible +3.9% / stop −8.0%, p_fill 97%, n_eff≈39.2) : P(cible|rempli) **25%** · **EV/risk -0.041** (×p_fill ; si rempli -0.34% du capital)
  - **swing** (entrée dip −1.701% → cible +8.721% / stop −5.431%, p_fill 98%, n_eff≈39.4) : P(cible|rempli) **26%** · **EV/risk -0.179** (×p_fill ; si rempli -1.00% du capital)
  - **deep** (entrée dip −2.612% → cible +12.334% / stop −8.223%, p_fill 91%, n_eff≈38.1) : P(cible|rempli) **20%** · **EV/risk -0.314** (×p_fill ; si rempli -2.83% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→61% · +2.0%→50% · +3.0%→36% · +5.0%→19% · +8.0%→5%
- Range intraday médian 6.99% (p90 10.6%) · excursion haute méd. +2.05% / basse méd. −4.19%
- Profil de vol intra : ouverture 4.526% vs midi 1.172% vs clôture 1.235% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 23% · trend ↑0%/↓1% ; spike-down 83% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. -1.037% ; recovery-V 39%
- **σ réalisé intraday** 4.405% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 60% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 3060912.5 (VA 2972362.5–3072987.5 ; dernier close 3071000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 74% · **stop −4.79%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.92% · baisse 33% (gap-down >1% 24% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.6% (p90 −3.38%) · haut méd +0.72% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.95% (p90 −4.25%) · haut méd +0.83% · range méd 3.34%
- Excursion ouverture 30min (n=160) : bas méd −2.37% (p90 −4.78%) · haut méd +0.87% · range méd 4.05%
- Excursion ouverture 60min (n=160) : bas méd −2.58% (p90 −5.31%) · haut méd +1.16% · range méd 4.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3079000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 67% (106/159) · gap 29% · délai 0.3min · rebond 56% (65/106) (MFE +1.16%)
   - −1.0% : fill 30min 55% · séance 63% (99/159) · gap 24% · délai 0.2min · rebond 57% (60/99) (MFE +1.38%)
   - −1.5% : fill 30min 48% · séance 56% (89/159) · gap 22% · délai 1.7min · rebond 55% (55/89) (MFE +1.2%)
   - −2.0% : fill 30min 44% · séance 53% (79/159) · gap 18% · délai 2.7min · rebond 54% (44/79) (MFE +1.44%)
   - −3.0% : fill 30min 32% · séance 46% (67/159) · gap 9% · délai 7.2min · rebond 67% (44/67) (MFE +1.5%)
   - −4.0% : fill 30min 24% · séance 40% (57/159) · gap 6% · délai 23.5min · rebond 73% (43/57) (MFE +2.27%)
   - −5.0% : fill 30min 18% · séance 35% (45/159) · gap 5% · délai 39.5min · rebond 74% (33/45) (MFE +2.24%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.85% (p90 −3.57%) → stop au-delà de −2.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.2% (p90 −3.16%) → stop au-delà de −2.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.09% (p90 −3.18%) → stop au-delà de −2.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=865 jambes) : jambe baissière méd −1.37% (p90 −3.37%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 100% (52/52) · rebond 52% (31/52)
      · −2.0% : fill 90% (43/52) · rebond 43% (22/43)
      · −3.0% : fill 90% (42/52) · rebond 65% (27/42)
      · −4.0% : fill 87% (38/52) · rebond 76% (28/38)
      · −5.0% : fill 78% (32/52) · rebond 82% (25/32)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (13/16) · rebond 70% (9/13)
      · −2.0% : fill 88% (12/16) · rebond 51% (6/12)
      · −3.0% : fill 60% (8/16) · rebond 59% (5/8)
      · −4.0% : fill 48% (7/16) · rebond 44% (5/7)
      · −5.0% : fill 36% (3/16) · rebond 24% (1/3)
   - **gap-up** (91 séances) :
      · −1.0% : fill 39% (34/91) · rebond 60% (20/34)
      · −2.0% : fill 28% (24/91) · rebond 76% (16/24)
      · −3.0% : fill 21% (17/91) · rebond 75% (12/17)
      · −4.0% : fill 13% (12/91) · rebond 79% (10/12)
      · −5.0% : fill 12% (10/91) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 52% si les 15 1res min sont vertes (62 cas) · 32% si rouges (98 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 75% si début vert vs 20% si rouge (base 38% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **75%** · continue >prix actuel 49% ; creux résiduel méd -1.78% (q20 -3.88%) → **SL/trailing à −3.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.9% / q75 +3.8% → **scale +1.9% / runner +3.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=94) : edge inversé — récupère vert seulement **20%** (continue à baisser 58%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.86%** (au-delà de la MAE q10 -5.86%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.19% .. +4.05%] · haut q95 +6.12% · bas q05 -5.28%
   - 60min (n=160) : retour [-5.24% .. +4.38%] · haut q95 +6.4% · bas q05 -6.02%
   - 2h (n=160) : retour [-6.59% .. +3.95%] · haut q95 +6.49% · bas q05 -7.73%
   - 4h (n=160) : retour [-7.26% .. +5.16%] · haut q95 +6.51% · bas q05 -9.19%
   - 6h (n=160) : retour [-7.59% .. +5.24%] · haut q95 +6.94% · bas q05 -9.25%
   - session (n=160) : retour [-7.0% .. +5.45%] · haut q95 +6.94% · bas q05 -9.37%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **55%**. Lecture précoce 30 min : signature présente → 21% vs absente 0% (base 5%)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 62.4  _(momentum haussier)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist 39852.113  _(pas de croisement recent)_
- **BB** : %B 0.92 · largeur 25.6%
- **ATR** : 167642.86 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.143  _(accumulation)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 47.7  _(transition)_
- **MA** : MA20 2837650.0 · MA50 2925320.0 · MA200 2745655.18  _(prix > MA20)_
- **Dist MA** : MA20 +10.7% · MA50 +7.3% · MA200 +14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (623590 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
