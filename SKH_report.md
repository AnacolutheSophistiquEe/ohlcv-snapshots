# 000660

**Generated** : 2026-09-30T00:17:45.526859+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1765000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩1765000.00 (+2.7% vs entrée) · entrée ₩1718164.39 · stop ₩1636735.81 · T1 ₩1793783.48 · R/R 0.93  
> ↳ ¼-Kelly 0.065 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1703040.57–₩1733288.21 (mid ₩1718164.39)
- Spot actuel : ₩1765000.00 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : ₩1636735.81 (plancher anti-bruit (R/R<2) ; -4.74 % depuis l'entree)
- Targets : T1 ₩1793783.48 · R/R 0.93 | T2 ₩1869402.58 · R/R 1.86 | T3 ₩1945021.68 · R/R 2.79
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1636735.81


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.49 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.27 %)** : le gap seul le franchit 0.903 % des séances (11 fois sur 1218).
   - exécution **1.376 pt plus bas** dans le cas TYPIQUE (médiane), 3.068 au p90, **3.59 au pire**
   - perte réelle **8.937 %** en moyenne _(tirée par la queue)_, jusqu'à **10.86 %** — au lieu des 7.27 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0151 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.444 % | p01 -6.997 % | pire -10.86 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4067** [0.3356 ; 0.4809] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.3827** [0.3326 ; 0.4347] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.3446** [0.296 ; 0.3958] _(largeur 10.0 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 70.4 observations effectives », dont la borne haute a 95 % vaut environ 4.3 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 63.8 observations effectives », dont la borne haute a 95 % vaut environ 4.7 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.74 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.10 % contre 6.65 % aujourd'hui, rapport 0.47)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.74 % si l'on extrapolait par √5 _(rapport 0.875 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4152** (β de hausse 1.6211, asymétrie 0.873) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.32 | EV/share : ₩26065.641 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 45 % | T3 31 %
- Kelly (position) : f* 0.258 | ¼-Kelly 0.065 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.0 | bear 6.6 | side 8.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.209% → cible +5.671% / stop −2.836%, p_fill 71%, n_eff≈75.2) : P(cible|rempli) **13%** · **EV/risk -0.226** (×p_fill ; si rempli -0.91% du capital)
  - **swing** (entrée dip −2.657% → cible +4.401% / stop −4.739%, p_fill 62%, n_eff≈70.4) : P(cible|rempli) **42%** · **EV/risk -0.159** (×p_fill ; si rempli -1.22% du capital)
  - **deep** (entrée dip −4.1% → cible +6.224% / stop −7.216%, p_fill 60%, n_eff≈63.8) : P(cible|rempli) **46%** · **EV/risk -0.131** (×p_fill ; si rempli -1.57% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→56% · +3.0%→41% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.84% (p90 10.55%) · excursion haute méd. +2.36% / basse méd. −2.61%
- Profil de vol intra : ouverture 2.965% vs midi 1.26% vs clôture 1.433% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑1%/↓0% ; spike-down 68% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.016)_ ; drift intra méd. -0.761% ; recovery-V 28%
- **σ réalisé intraday** 4.039% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 62% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1643750.0 (VA 1628750.0–1654250.0 ; dernier close 1649000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 68% · **stop −7.63%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.28 (high win-rate)
- Gaps overnight (n=153) : méd. 0.55% · baisse 46% (gap-down >1% 37% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.0%) · haut méd +0.75% · range méd 1.6%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.6%) · haut méd +0.95% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.32% (p90 −3.49%) · haut méd +1.26% · range méd 2.93%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −4.54%) · haut méd +1.52% · range méd 3.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1647000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 67% (97/153) · gap 42% · délai 0.0min · rebond 57% (54/97) (MFE +1.21%)
   - −1.0% : fill 30min 53% · séance 63% (89/153) · gap 37% · délai 0.0min · rebond 60% (56/89) (MFE +1.6%)
   - −1.5% : fill 30min 43% · séance 57% (80/153) · gap 28% · délai 0.0min · rebond 68% (52/80) (MFE +1.64%)
   - −2.0% : fill 30min 38% · séance 52% (73/153) · gap 27% · délai 0.0min · rebond 64% (48/73) (MFE +1.79%)
   - −3.0% : fill 30min 32% · séance 48% (62/153) · gap 21% · délai 1.9min · rebond 70% (42/62) (MFE +2.09%)
   - −4.0% : fill 30min 24% · séance 38% (50/153) · gap 13% · délai 3.0min · rebond 66% (36/50) (MFE +2.18%)
   - −5.0% : fill 30min 16% · séance 30% (39/153) · gap 7% · délai 22.4min · rebond 68% (26/39) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.52%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.74%) → stop au-delà de −2.29% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −3.31%) → stop au-delà de −2.34% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=870 jambes) : jambe baissière méd −1.25% (p90 −3.41%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 96% (61/63) · rebond 56% (34/61)
      · −2.0% : fill 82% (52/63) · rebond 55% (29/52)
      · −3.0% : fill 78% (46/63) · rebond 63% (28/46)
      · −4.0% : fill 67% (41/63) · rebond 61% (28/41)
      · −5.0% : fill 52% (32/63) · rebond 59% (19/32)
   - **flat** (10 séances) :
      · −1.0% : fill 86% (8/10) · rebond 95% (7/8)
      · −2.0% : fill 44% (4/10) · rebond 100% (4/4)
      · −3.0% : fill 32% (3/10) · rebond 100% (3/3)
      · −4.0% : fill 0% (0/10) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/10) · rebond 0% (0/0)
   - **gap-up** (80 séances) :
      · −1.0% : fill 33% (20/80) · rebond 66% (15/20)
      · −2.0% : fill 28% (17/80) · rebond 85% (15/17)
      · −3.0% : fill 24% (13/80) · rebond 86% (11/13)
      · −4.0% : fill 15% (9/80) · rebond 83% (8/9)
      · −5.0% : fill 13% (7/80) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (80 cas) · 34% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 79% si début vert vs 13% si rouge (base 45% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **79%** · continue >prix actuel 56% ; creux résiduel méd -1.5% (q20 -3.69%) → **SL/trailing à −3.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +3.68% → **scale +1.68% / runner +3.68%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **13%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.35%** (au-delà de la MAE q10 -6.35%), cible rebond +1.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.28% .. +2.59%] · haut q95 +3.4% · bas q05 -4.47%
   - 60min (n=160) : retour [-3.62% .. +4.52%] · haut q95 +5.8% · bas q05 -5.42%
   - 2h (n=160) : retour [-4.93% .. +4.63%] · haut q95 +7.34% · bas q05 -7.19%
   - 4h (n=160) : retour [-6.68% .. +5.64%] · haut q95 +7.91% · bas q05 -8.13%
   - 6h (n=160) : retour [-6.87% .. +6.21%] · haut q95 +8.46% · bas q05 -8.61%
   - session (n=160) : retour [-7.13% .. +6.58%] · haut q95 +8.46% · bas q05 -8.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 6.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **19%**. Lecture précoce 30 min : signature présente → 10% vs absente 1% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.17% / p90 1.78%) · ~3.44 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 20.23 min, n=30)
   - −1.0% → **87%** (reprise méd 34.74 min, n=11)
   - −1.5% → **68%** (reprise méd 30.12 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.78%** (p90, défaut prudent ; serré/agressif −1.17%) ; extension open→close méd +7.78% (q75 +8.2% / q95 +11.4%), MFE méd +8.31% / q90 +10.89%
   - Échelle scale-out : +8.31% (33%) / +8.56% (33%) / +10.89% (34%)
- **DÉSARMER** : repli > **−1.78%** depuis le plus-haut = décay → P(retournement) **47%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.89% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.96%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.23 · part idiosyncratique 0.77
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.5  _(neutre)_
- **ADX** : 10.7  _(pas de tendance nette)_
- **MACD** : hist 3487.15  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 19.7%
- **ATR** : 81428.57 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.021  _(neutre)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 55.4  _(transition)_
- **MA** : MA20 1758550.0 · MA50 1684734.39 · MA200 1398642.81  _(prix > MA20)_
- **Dist MA** : MA20 +0.4% · MA50 +4.8% · MA200 +26.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (557942 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
