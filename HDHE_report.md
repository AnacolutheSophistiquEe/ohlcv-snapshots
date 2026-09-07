# 267260

**Generated** : 2026-09-07T00:24:59.277780+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩714000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩714000.00 (+1.5% vs entrée) · entrée ₩703750.00 · stop ₩647450.00 · T1 ₩739394.58 · R/R 0.63  
> ↳ P(T1 av. stop) 15 % _(réel 5 s)_ · EV/risk -0.001 _(réel 5 s)_ (GBM -0.188) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩700673.22–₩706826.78 (mid ₩703750.00)
- Spot actuel : ₩714000.00 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : ₩647450.00 (stop swing_plan-based (-9.51%))
- Targets : T1 ₩739394.58 · R/R 0.63 | T2 ₩744578.23 · R/R 0.73 | T3 ₩749761.87 · R/R 0.82
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩647450.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.03 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.51 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1217).
   - exécution **2.205 pt plus bas** dans le cas TYPIQUE (médiane), 2.205 au p90, **2.205 au pire**
   - perte réelle **11.715 %** en moyenne _(tirée par la queue)_, jusqu'à **11.715 %** — au lieu des 9.51 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0018 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.659 % | p01 -4.805 % | pire -11.715 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0812** [0.0474 ; 0.1289] _(largeur 8.2 pt, n_eff 173.1)_
   - swing : **0.3686** [0.319 ; 0.4204] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3185** [0.2711 ; 0.369] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 32.5 observations effectives », dont la borne haute a 95 % vaut environ 9.2 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 28.2 observations effectives », dont la borne haute a 95 % vaut environ 10.6 %.
- ⚠ **5 s — échantillon insuffisant sur : swing (33.1 pt), deep (35.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.68 %** | CVaR **-8.85 %** | vol 4.43 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.86 % contre 5.02 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.98 % vs -11.99 % si l'on extrapolait par √5 _(rapport 0.916 ; < 1 = le √5 surestime)_
- **β de baisse : 1.044** (β de hausse 0.8365, asymétrie 1.248) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.188 | EV/share : ₩-10556.250 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.6 | bear 7.1 | side 7.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.435% → cible +5.065% / stop −8.0%, p_fill 88%, n_eff≈37.7) : P(cible|rempli) **15%** · **EV/risk -0.001** (×p_fill ; si rempli -0.01% du capital)
  - **swing** (entrée dip −3.157% → cible +4.873% / stop −6.56%, p_fill 76%, n_eff≈32.5) : P(cible|rempli) **51%** · **EV/risk -0.111** (×p_fill ; si rempli -0.96% du capital)
  - **deep** (entrée dip −4.881% → cible +6.892% / stop −10.018%, p_fill 69%, n_eff≈28.2) : P(cible|rempli) **51%** · **EV/risk -0.123** (×p_fill ; si rempli -1.79% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→64% · +2.0%→42% · +3.0%→35% · +5.0%→12% · +8.0%→4%
- Range intraday médian 6.64% (p90 10.49%) · excursion haute méd. +1.58% / basse méd. −4.07%
- Profil de vol intra : ouverture 4.476% vs midi 1.219% vs clôture 1.308% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 83% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. -1.024% ; recovery-V 29%
- **σ réalisé intraday** 4.014% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 38% / bas 68% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 714037.5 (VA 710012.5–714037.5 ; dernier close 713000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 79% · **stop −4.45%** sous le fill (sous le bruit) · cible +2.45% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.91% · baisse 37% (gap-down >1% 19% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −1.72% (p90 −3.84%) · haut méd +0.86% · range méd 2.83%
- Excursion ouverture 15min (n=160) : bas méd −2.06% (p90 −4.32%) · haut méd +0.94% · range méd 3.5%
- Excursion ouverture 30min (n=160) : bas méd −2.27% (p90 −4.83%) · haut méd +1.03% · range méd 3.78%
- Excursion ouverture 60min (n=160) : bas méd −2.59% (p90 −5.0%) · haut méd +1.06% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 714000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 74% (109/159) · gap 30% · délai 0.0min · rebond 51% (57/109) (MFE +1.06%)
   - −1.0% : fill 30min 56% · séance 70% (101/159) · gap 19% · délai 0.2min · rebond 58% (60/101) (MFE +1.31%)
   - −1.5% : fill 30min 50% · séance 66% (91/159) · gap 16% · délai 0.7min · rebond 64% (58/91) (MFE +1.27%)
   - −2.0% : fill 30min 42% · séance 60% (81/159) · gap 11% · délai 1.2min · rebond 69% (56/81) (MFE +1.66%)
   - −3.0% : fill 30min 34% · séance 48% (66/159) · gap 8% · délai 3.4min · rebond 75% (50/66) (MFE +1.92%)
   - −4.0% : fill 30min 23% · séance 39% (52/159) · gap 5% · délai 11.3min · rebond 75% (37/52) (MFE +2.1%)
   - −5.0% : fill 30min 16% · séance 31% (42/159) · gap 2% · délai 11.5min · rebond 79% (31/42) (MFE +2.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.92% (p90 −3.65%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −3.14%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.43%) → stop au-delà de −3.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=831 jambes) : jambe baissière méd −1.22% (p90 −3.26%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 100% (50/50) · rebond 44% (25/50)
      · −2.0% : fill 96% (44/50) · rebond 62% (27/44)
      · −3.0% : fill 88% (40/50) · rebond 75% (29/40)
      · −4.0% : fill 77% (34/50) · rebond 73% (24/34)
      · −5.0% : fill 63% (28/50) · rebond 84% (22/28)
   - **flat** (16 séances) :
      · −1.0% : fill 96% (15/16) · rebond 74% (10/15)
      · −2.0% : fill 73% (12/16) · rebond 73% (10/12)
      · −3.0% : fill 56% (10/16) · rebond 49% (7/10)
      · −4.0% : fill 51% (8/16) · rebond 62% (4/8)
      · −5.0% : fill 51% (8/16) · rebond 73% (6/8)
   - **gap-up** (93 séances) :
      · −1.0% : fill 47% (36/93) · rebond 70% (25/36)
      · −2.0% : fill 34% (25/93) · rebond 80% (19/25)
      · −3.0% : fill 22% (16/93) · rebond 89% (14/16)
      · −4.0% : fill 12% (10/93) · rebond 92% (9/10)
      · −5.0% : fill 7% (6/93) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 34% en base · 45% si les 15 1res min sont vertes (67 cas) · 29% si rouges (93 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:18** → P(séance verte=clôture>ouverture) 72% si début vert vs 15% si rouge (base 34% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **72%** · continue >prix actuel 43% ; creux résiduel méd -1.79% (q20 -3.65%) → **SL/trailing à −3.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +2.67% → **scale +1.57% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=94) : edge inversé — récupère vert seulement **15%** (continue à baisser 38%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.72%** (au-delà de la MAE q10 -4.72%), cible rebond +1.58% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.93% .. +2.7%] · haut q95 +4.23% · bas q05 -5.45%
   - 60min (n=160) : retour [-5.58% .. +2.56%] · haut q95 +4.45% · bas q05 -5.92%
   - 2h (n=160) : retour [-6.24% .. +3.61%] · haut q95 +4.83% · bas q05 -7.08%
   - 4h (n=160) : retour [-6.83% .. +3.23%] · haut q95 +5.03% · bas q05 -8.32%
   - 6h (n=160) : retour [-6.97% .. +4.44%] · haut q95 +5.89% · bas q05 -8.86%
   - session (n=160) : retour [-7.15% .. +4.51%] · haut q95 +5.99% · bas q05 -9.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.8  _(momentum baissier)_
- **ADX** : 14.8  _(pas de tendance nette)_
- **MACD** : hist -692.0  _(bearish_recent)_
- **BB** : %B 0.21 · largeur 18.9%
- **ATR** : 45357.14 (35.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.068  _(accumulation)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 47.6  _(transition)_
- **MA** : MA20 756070.17 · MA50 790835.58 · MA200 918359.93  _(prix < MA20)_
- **Dist MA** : MA20 -5.6% · MA50 -9.7% · MA200 -22.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (481743 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
