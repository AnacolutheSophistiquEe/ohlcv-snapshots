# 298040

**Generated** : 2026-09-02T00:17:58.692931+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩2916000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2916000.00 (+7.7% vs entrée) · entrée ₩2706780.12 · stop ₩2541422.97 · T1 ₩2879602.26 · R/R 1.05  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.092 _(réel 5 s)_ (GBM 0.144) · ¼-Kelly 0.02 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2672215.69–₩2741344.54 (mid ₩2706780.12)
- Spot actuel : ₩2916000.00 (+7.7% au-dessus de la zone — repli à attendre)
- Stop : ₩2541422.97 (stop swing_plan-based (-12.85%))
- Targets : T1 ₩2879602.26 · R/R 1.05 | T2 ₩3052424.41 · R/R 2.09 | T3 ₩3225246.55 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2541422.97


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.12 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.85 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.85 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.45 % | p01 -4.607 % | pire -11.686 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0859** [0.0509 ; 0.1345] _(largeur 8.4 pt, n_eff 173.1)_
   - swing : **0.432** [0.3805 ; 0.4846] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.3561** [0.307 ; 0.4076] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : swing (44.2 pt), deep (40.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.95 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.60 % contre 5.93 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.91 % vs -12.61 % si l'on extrapolait par √5 _(rapport 0.944 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0756** (β de hausse 0.9866, asymétrie 1.0902) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.144 | EV/share : ₩23899.958 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 28 % | T3 13 %
- Kelly (position) : f* 0.08 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 78.2 | bear 16.4 | side 5.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.261% → cible +7.897% / stop −8.0%, p_fill 56%, n_eff≈26.5) : P(cible|rempli) **1%** · **EV/risk +0.018** (×p_fill ; si rempli +0.26% du capital)
  - **swing** (entrée dip −7.18% → cible +6.385% / stop −6.109%, p_fill 28%, n_eff≈16.0) : P(cible|rempli) **23%** · **EV/risk -0.092** (×p_fill ; si rempli -1.98% du capital)
  - **deep** (entrée dip −11.083% → cible +9.029% / stop −9.567%, p_fill 31%, n_eff≈19.5) : P(cible|rempli) **32%** · **EV/risk -0.107** (×p_fill ; si rempli -3.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→61% · +2.0%→50% · +3.0%→36% · +5.0%→20% · +8.0%→5%
- Range intraday médian 6.89% (p90 10.6%) · excursion haute méd. +2.05% / basse méd. −3.98%
- Profil de vol intra : ouverture 4.524% vs midi 1.171% vs clôture 1.239% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓1% ; spike-down 82% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.052)_ ; drift intra méd. -0.959% ; recovery-V 37%
- **σ réalisé intraday** 4.383% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 59% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 2952750.0 (VA 2938750.0–2973750.0 ; dernier close 2957000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 75% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.1% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.89% · baisse 34% (gap-down >1% 26% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.6% (p90 −3.33%) · haut méd +0.72% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.95% (p90 −4.21%) · haut méd +0.82% · range méd 3.34%
- Excursion ouverture 30min (n=160) : bas méd −2.32% (p90 −4.54%) · haut méd +0.87% · range méd 4.05%
- Excursion ouverture 60min (n=160) : bas méd −2.52% (p90 −5.3%) · haut méd +1.16% · range méd 4.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2963000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 69% (107/159) · gap 30% · délai 0.1min · rebond 56% (65/107) (MFE +1.16%)
   - −1.0% : fill 30min 55% · séance 63% (99/159) · gap 26% · délai 0.1min · rebond 56% (59/99) (MFE +1.34%)
   - −1.5% : fill 30min 49% · séance 56% (89/159) · gap 23% · délai 1.5min · rebond 53% (54/89) (MFE +1.17%)
   - −2.0% : fill 30min 45% · séance 53% (80/159) · gap 19% · délai 2.1min · rebond 52% (44/80) (MFE +1.24%)
   - −3.0% : fill 30min 33% · séance 46% (68/159) · gap 11% · délai 6.0min · rebond 64% (44/68) (MFE +1.46%)
   - −4.0% : fill 30min 24% · séance 40% (58/159) · gap 6% · délai 21.2min · rebond 70% (43/58) (MFE +2.23%)
   - −5.0% : fill 30min 19% · séance 36% (46/159) · gap 5% · délai 23.9min · rebond 75% (34/46) (MFE +2.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −3.5%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.02% (p90 −3.1%) → stop au-delà de −2.3% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.0% (p90 −2.67%) → stop au-delà de −2.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=861 jambes) : jambe baissière méd −1.38% (p90 −3.39%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 100% (53/53) · rebond 49% (31/53)
      · −2.0% : fill 91% (44/53) · rebond 40% (22/44)
      · −3.0% : fill 90% (43/53) · rebond 61% (27/43)
      · −4.0% : fill 88% (39/53) · rebond 71% (28/39)
      · −5.0% : fill 79% (33/53) · rebond 84% (26/33)
   - **flat** (17 séances) :
      · −1.0% : fill 77% (13/17) · rebond 70% (9/13)
      · −2.0% : fill 73% (12/17) · rebond 51% (6/12)
      · −3.0% : fill 50% (8/17) · rebond 59% (5/8)
      · −4.0% : fill 40% (7/17) · rebond 44% (5/7)
      · −5.0% : fill 30% (3/17) · rebond 24% (1/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 39% (33/89) · rebond 60% (19/33)
      · −2.0% : fill 28% (24/89) · rebond 76% (16/24)
      · −3.0% : fill 21% (17/89) · rebond 75% (12/17)
      · −4.0% : fill 13% (12/89) · rebond 79% (10/12)
      · −5.0% : fill 12% (10/89) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 55% si les 15 1res min sont vertes (62 cas) · 31% si rouges (98 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 76% si début vert vs 20% si rouge (base 39% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **76%** · continue >prix actuel 46% ; creux résiduel méd -1.83% (q20 -3.8%) → **SL/trailing à −3.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.77% / q75 +3.79% → **scale +1.77% / runner +3.79%**, sortie à la clôture
  - **si ROUGE au coude** (n=94) : edge inversé — récupère vert seulement **20%** (continue à baisser 60%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.83%** (au-delà de la MAE q10 -5.83%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.19% .. +4.37%] · haut q95 +6.12% · bas q05 -5.25%
   - 60min (n=160) : retour [-5.24% .. +4.02%] · haut q95 +6.36% · bas q05 -6.0%
   - 2h (n=160) : retour [-6.32% .. +3.89%] · haut q95 +6.48% · bas q05 -7.52%
   - 4h (n=160) : retour [-7.11% .. +5.1%] · haut q95 +6.5% · bas q05 -9.15%
   - 6h (n=160) : retour [-7.59% .. +5.24%] · haut q95 +6.81% · bas q05 -9.21%
   - session (n=160) : retour [-6.99% .. +5.44%] · haut q95 +6.81% · bas q05 -9.35%


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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 53.3  _(neutre)_
- **ADX** : 9.6  _(pas de tendance nette)_
- **MACD** : hist 25834.818  _(pas de croisement recent)_
- **BB** : %B 0.56 · largeur 17.8%
- **ATR** : 165357.14 (45.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.086  _(accumulation)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 2886650.0 · MA50 2892200.0 · MA200 2752840.67  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 +0.8% · MA200 +5.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (505285 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
