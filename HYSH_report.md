# 298040

**Generated** : 2026-09-01T00:18:26.673147+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩2940000.00  

> 🟡 **WAIT-FOR-DIP** — spot +5.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩2940000.00 (+5.3% vs entrée) · entrée ₩2792050.00 · stop ₩2619835.71 · T1 ₩2972174.58 · R/R 1.05  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.025 _(réel 5 s)_ (GBM 0.133) · ¼-Kelly 0.018 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2756025.08–₩2828074.92 (mid ₩2792050.00)
- Spot actuel : ₩2940000.00 (+5.3% au-dessus de la zone — repli à attendre)
- Stop : ₩2619835.71 (stop swing_plan-based (-10.89%))
- Targets : T1 ₩2972174.58 · R/R 1.05 | T2 ₩3152299.16 · R/R 2.09 | T3 ₩3332423.74 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2619835.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.12 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.89 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1217).
   - exécution **0.796 pt plus bas** dans le cas TYPIQUE (médiane), 0.796 au p90, **0.796 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 10.89 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0007 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.45 % | p01 -4.607 % | pire -11.686 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0869** [0.0517 ; 0.1357] _(largeur 8.4 pt, n_eff 173.1)_
   - swing : **0.4365** [0.3849 ; 0.4891] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.3526** [0.3036 ; 0.404] _(largeur 10.0 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : swing (37.8 pt), deep (38.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.96 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.60 % contre 5.94 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.91 % vs -12.61 % si l'on extrapolait par √5 _(rapport 0.944 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0751** (β de hausse 0.983, asymétrie 1.0937) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.133 | EV/share : ₩22958.421 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 27 % | T3 12 %
- Kelly (position) : f* 0.073 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 53.8 | bear 29.3 | side 17.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.283% → cible +5.95% / stop −8.0%, p_fill 63%, n_eff≈31.0) : P(cible|rempli) **8%** · **EV/risk -0.017** (×p_fill ; si rempli -0.21% du capital)
  - **swing** (entrée dip −5.032% → cible +6.451% / stop −6.168%, p_fill 56%, n_eff≈24.4) : P(cible|rempli) **50%** · **EV/risk +0.025** (×p_fill ; si rempli +0.27% du capital)
  - **deep** (entrée dip −7.773% → cible +9.124% / stop −9.527%, p_fill 48%, n_eff≈23.5) : P(cible|rempli) **46%** · **EV/risk -0.054** (×p_fill ; si rempli -1.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→61% · +2.0%→50% · +3.0%→36% · +5.0%→20% · +8.0%→5%
- Range intraday médian 6.89% (p90 10.6%) · excursion haute méd. +2.05% / basse méd. −4.1%
- Profil de vol intra : ouverture 4.517% vs midi 1.176% vs clôture 1.237% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓1% ; spike-down 82% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.053)_ ; drift intra méd. -0.886% ; recovery-V 39%
- **σ réalisé intraday** 4.434% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 57% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 3139612.5 (VA 3115487.5–3163737.5 ; dernier close 3153000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 74% · **stop −4.79%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.91% · baisse 32% (gap-down >1% 24% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −1.57% (p90 −3.36%) · haut méd +0.73% · range méd 2.61%
- Excursion ouverture 15min (n=160) : bas méd −1.91% (p90 −4.23%) · haut méd +0.86% · range méd 3.36%
- Excursion ouverture 30min (n=160) : bas méd −2.28% (p90 −4.66%) · haut méd +0.91% · range méd 4.11%
- Excursion ouverture 60min (n=160) : bas méd −2.54% (p90 −5.3%) · haut méd +1.18% · range méd 4.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3153000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 68% (106/159) · gap 29% · délai 0.2min · rebond 57% (65/106) (MFE +1.18%)
   - −1.0% : fill 30min 54% · séance 62% (98/159) · gap 24% · délai 0.2min · rebond 57% (59/98) (MFE +1.38%)
   - −1.5% : fill 30min 48% · séance 55% (88/159) · gap 21% · délai 1.7min · rebond 55% (54/88) (MFE +1.2%)
   - −2.0% : fill 30min 44% · séance 52% (79/159) · gap 17% · délai 2.7min · rebond 54% (44/79) (MFE +1.44%)
   - −3.0% : fill 30min 32% · séance 45% (67/159) · gap 9% · délai 7.2min · rebond 67% (44/67) (MFE +1.5%)
   - −4.0% : fill 30min 23% · séance 39% (57/159) · gap 6% · délai 23.5min · rebond 73% (43/57) (MFE +2.27%)
   - −5.0% : fill 30min 17% · séance 34% (45/159) · gap 5% · délai 39.5min · rebond 74% (33/45) (MFE +2.24%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.92% (p90 −3.5%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −3.1%) → stop au-delà de −2.32% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.01% (p90 −2.79%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=864 jambes) : jambe baissière méd −1.38% (p90 −3.41%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 100% (52/52) · rebond 52% (31/52)
      · −2.0% : fill 90% (43/52) · rebond 43% (22/43)
      · −3.0% : fill 90% (42/52) · rebond 65% (27/42)
      · −4.0% : fill 87% (38/52) · rebond 76% (28/38)
      · −5.0% : fill 78% (32/52) · rebond 82% (25/32)
   - **flat** (17 séances) :
      · −1.0% : fill 77% (13/17) · rebond 70% (9/13)
      · −2.0% : fill 73% (12/17) · rebond 51% (6/12)
      · −3.0% : fill 50% (8/17) · rebond 59% (5/8)
      · −4.0% : fill 40% (7/17) · rebond 44% (5/7)
      · −5.0% : fill 30% (3/17) · rebond 24% (1/3)
   - **gap-up** (90 séances) :
      · −1.0% : fill 39% (33/90) · rebond 60% (19/33)
      · −2.0% : fill 28% (24/90) · rebond 76% (16/24)
      · −3.0% : fill 21% (17/90) · rebond 75% (12/17)
      · −4.0% : fill 13% (12/90) · rebond 79% (10/12)
      · −5.0% : fill 12% (10/90) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 55% si les 15 1res min sont vertes (62 cas) · 32% si rouges (98 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 76% si début vert vs 20% si rouge (base 39% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **76%** · continue >prix actuel 46% ; creux résiduel méd -1.83% (q20 -3.8%) → **SL/trailing à −3.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.77% / q75 +3.79% → **scale +1.77% / runner +3.79%**, sortie à la clôture
  - **si ROUGE au coude** (n=94) : edge inversé — récupère vert seulement **20%** (continue à baisser 58%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.86%** (au-delà de la MAE q10 -5.86%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.19% .. +4.38%] · haut q95 +6.12% · bas q05 -5.26%
   - 60min (n=160) : retour [-5.24% .. +4.18%] · haut q95 +6.38% · bas q05 -6.01%
   - 2h (n=160) : retour [-6.46% .. +3.89%] · haut q95 +6.49% · bas q05 -7.65%
   - 4h (n=160) : retour [-7.18% .. +5.13%] · haut q95 +6.5% · bas q05 -9.17%
   - 6h (n=160) : retour [-7.59% .. +5.24%] · haut q95 +6.87% · bas q05 -9.23%
   - session (n=160) : retour [-7.0% .. +5.44%] · haut q95 +6.87% · bas q05 -9.36%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **55%**. Lecture précoce 30 min : signature présente → 19% vs absente 0% (base 5%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 50.2  _(neutre)_
- **ADX** : 10.1  _(pas de tendance nette)_
- **MACD** : hist 33074.246  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 21.5%
- **ATR** : 172214.29 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.056  _(accumulation)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 48.7  _(transition)_
- **MA** : MA20 2864450.0 · MA50 2910520.0 · MA200 2749372.54  _(prix > MA20)_
- **Dist MA** : MA20 +2.6% · MA50 +1.0% · MA200 +6.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (510054 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
