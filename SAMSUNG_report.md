# 005930

**Generated** : 2026-09-03T00:15:37.786931+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩250500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot ₩250500.00 (+3.8% vs entrée) · entrée ₩241259.21 · stop ₩225652.06 · T1 ₩255192.06 · R/R 0.89  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.112 _(réel 5 s)_ (GBM 0.297) · ¼-Kelly 0.039 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩238472.63–₩244045.78 (mid ₩241259.21)
- Spot actuel : ₩250500.00 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : ₩225652.06 (stop swing_plan-based (-9.92%))
- Targets : T1 ₩255192.06 · R/R 0.89 | T2 ₩269124.92 · R/R 1.79 | T3 ₩283057.78 · R/R 2.68
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩225652.06


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.92 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1217).
   - exécution **1.022 pt plus bas** dans le cas TYPIQUE (médiane), 1.022 au p90, **1.022 au pire**
   - perte réelle **10.942 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 9.92 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0008 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.437 % | p01 -4.952 % | pire -10.942 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2904** [0.2267 ; 0.3611] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.2409** [0.1981 ; 0.288] _(largeur 9.0 pt, n_eff 345.6)_
   - deep : **0.2104** [0.17 ; 0.2557] _(largeur 8.6 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.2 pt), swing (36.5 pt), deep (36.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.71 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.61 % contre 5.80 % aujourd'hui, rapport 0.45)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.36 % vs -7.17 % si l'on extrapolait par √5 _(rapport 0.887 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1701** (β de hausse 1.3369, asymétrie 0.8753) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.297 | EV/share : ₩4638.112 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 27 % | T3 12 %
- Kelly (position) : f* 0.157 | ¼-Kelly 0.039 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 43.4 | bear 7.5 | side 49.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.68% → cible +6.753% / stop −3.376%, p_fill 68%, n_eff≈32.2) : P(cible|rempli) **7%** · **EV/risk -0.178** (×p_fill ; si rempli -0.88% du capital)
  - **swing** (entrée dip −3.69% → cible +5.775% / stop −6.469%, p_fill 54%, n_eff≈26.3) : P(cible|rempli) **35%** · **EV/risk -0.112** (×p_fill ; si rempli -1.33% du capital)
  - **deep** (entrée dip −5.705% → cible +8.167% / stop −9.911%, p_fill 64%, n_eff≈27.0) : P(cible|rempli) **52%** · **EV/risk -0.017** (×p_fill ; si rempli -0.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→49% · +3.0%→39% · +5.0%→25% · +8.0%→5%
- Range intraday médian 6.25% (p90 9.84%) · excursion haute méd. +1.9% / basse méd. −3.0%
- Profil de vol intra : ouverture 3.174% vs midi 1.376% vs clôture 1.574% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 69% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.137 ; mean-reverting — autocorr -0.104)_ ; drift intra méd. -0.357% ; recovery-V 26%
- **σ réalisé intraday** 3.845% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 63% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 260536.25 (VA 259083.75–262196.25 ; dernier close 260300.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 51% · **stop −6.12%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.17 (high win-rate)
- Gaps overnight (n=159) : méd. 0.33% · baisse 45% (gap-down >1% 37% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −1.65%) · haut méd +0.6% · range méd 1.55%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.35%) · haut méd +0.93% · range méd 2.15%
- Excursion ouverture 30min (n=160) : bas méd −1.22% (p90 −3.2%) · haut méd +1.05% · range méd 2.61%
- Excursion ouverture 60min (n=160) : bas méd −1.62% (p90 −3.59%) · haut méd +1.33% · range méd 3.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 261000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 68% (97/159) · gap 39% · délai 0.0min · rebond 49% (50/97) (MFE +0.95%)
   - −1.0% : fill 30min 47% · séance 60% (88/159) · gap 37% · délai 0.0min · rebond 58% (50/88) (MFE +1.31%)
   - −1.5% : fill 30min 43% · séance 53% (76/159) · gap 29% · délai 0.0min · rebond 61% (45/76) (MFE +1.52%)
   - −2.0% : fill 30min 37% · séance 50% (71/159) · gap 25% · délai 0.0min · rebond 63% (44/71) (MFE +1.85%)
   - −3.0% : fill 30min 30% · séance 44% (61/159) · gap 23% · délai 0.0min · rebond 54% (34/61) (MFE +1.13%)
   - −4.0% : fill 30min 22% · séance 34% (46/159) · gap 11% · délai 5.6min · rebond 53% (27/46) (MFE +1.24%)
   - −5.0% : fill 30min 14% · séance 26% (36/159) · gap 9% · délai 18.2min · rebond 51% (23/36) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −1.94%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −2.87%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.7%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=778 jambes) : jambe baissière méd −1.21% (p90 −3.02%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 96% (59/62) · rebond 52% (30/59)
      · −2.0% : fill 88% (51/62) · rebond 54% (28/51)
      · −3.0% : fill 82% (47/62) · rebond 48% (25/47)
      · −4.0% : fill 68% (37/62) · rebond 49% (21/37)
      · −5.0% : fill 55% (30/62) · rebond 41% (17/30)
   - **flat** (14 séances) :
      · −1.0% : fill 73% (11/14) · rebond 58% (6/11)
      · −2.0% : fill 48% (7/14) · rebond 81% (5/7)
      · −3.0% : fill 33% (5/14) · rebond 33% (2/5)
      · −4.0% : fill 24% (3/14) · rebond 25% (1/3)
      · −5.0% : fill 24% (3/14) · rebond 100% (3/3)
   - **gap-up** (83 séances) :
      · −1.0% : fill 28% (18/83) · rebond 74% (14/18)
      · −2.0% : fill 20% (13/83) · rebond 85% (11/13)
      · −3.0% : fill 16% (9/83) · rebond 82% (7/9)
      · −4.0% : fill 9% (6/83) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/83) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 60% si les 15 1res min sont vertes (78 cas) · 23% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 84% si début vert vs 7% si rouge (base 41% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 74min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **84%** · continue >prix actuel 64% ; creux résiduel méd -0.89% (q20 -3.29%) → **SL/trailing à −3.29%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.65% / q75 +3.47% → **scale +2.65% / runner +3.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **7%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.77%** (au-delà de la MAE q10 -6.77%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +2.68%] · haut q95 +3.45% · bas q05 -3.69%
   - 60min (n=160) : retour [-3.11% .. +4.23%] · haut q95 +4.97% · bas q05 -4.72%
   - 2h (n=160) : retour [-4.53% .. +4.7%] · haut q95 +5.87% · bas q05 -5.59%
   - 4h (n=160) : retour [-5.92% .. +5.35%] · haut q95 +6.83% · bas q05 -7.5%
   - 6h (n=160) : retour [-6.85% .. +5.29%] · haut q95 +6.94% · bas q05 -7.73%
   - session (n=160) : retour [-6.38% .. +5.41%] · haut q95 +6.94% · bas q05 -8.44%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.98%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.2  _(neutre)_
- **ADX** : 12.0  _(pas de tendance nette)_
- **MACD** : hist 673.881  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 23.0%
- **ATR** : 15607.14 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.002  _(neutre)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 61.6  _(transition)_
- **MA** : MA20 255675.0 · MA50 268970.29 · MA200 209855.84  _(prix < MA20)_
- **Dist MA** : MA20 -2.0% · MA50 -6.9% · MA200 +19.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (214300 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
