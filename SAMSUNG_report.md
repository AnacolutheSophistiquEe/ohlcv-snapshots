# 005930

**Generated** : 2026-10-01T00:16:14.359845+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩268500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩268500.00 (+6.8% vs entrée) · entrée ₩251339.47 · stop ₩241768.04 · T1 ₩262040.65 · R/R 1.12  
> ↳ ¼-Kelly 0.059 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩249513.10–₩253165.84 (mid ₩251339.47)
- Spot actuel : ₩268500.00 (+6.8% au-dessus de la zone — repli à attendre)
- Stop : ₩241768.04 (plancher anti-bruit (R/R<2) ; -3.81 % depuis l'entree)
- Targets : T1 ₩262040.65 · R/R 1.12 | T2 ₩272741.84 · R/R 2.24 | T3 ₩283443.02 · R/R 3.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩241768.04


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.11 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.96 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **0.982 pt plus bas** dans le cas TYPIQUE (médiane), 0.982 au p90, **0.982 au pire**
   - perte réelle **10.942 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 9.96 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0008 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.482 % | p01 -4.951 % | pire -10.942 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4565** [0.3835 ; 0.5309] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3616** [0.3123 ; 0.4132] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3229** [0.2752 ; 0.3735] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 31.6 observations effectives », dont la borne haute a 95 % vaut environ 9.5 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 29.8 observations effectives », dont la borne haute a 95 % vaut environ 10.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (28.3 pt), swing (32.9 pt), deep (34.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.75 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.98 % contre 5.59 % aujourd'hui, rapport 0.53)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.38 % vs -7.36 % si l'on extrapolait par √5 _(rapport 0.868 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1738** (β de hausse 1.3385, asymétrie 0.877) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.327 | EV/share : ₩3127.932 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 37 % | T3 20 %
- Kelly (position) : f* 0.236 | ¼-Kelly 0.059 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 28.2 | bear 5.0 | side 66.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 524.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.904% → cible +1.836% / stop −1.5%, p_fill 39%, n_eff≈45.3) : P(cible|rempli) **37%** · **EV/risk -0.050** (×p_fill ; si rempli -0.19% du capital)
  - **swing** (entrée dip −6.395% → cible +4.258% / stop −3.808%, p_fill 27%, n_eff≈31.6) : P(cible|rempli) **40%** · **EV/risk -0.057** (×p_fill ; si rempli -0.81% du capital)
  - **deep** (entrée dip −9.873% → cible +6.254% / stop −5.933%, p_fill 27%, n_eff≈29.8) : P(cible|rempli) **56%** · **EV/risk +0.041** (×p_fill ; si rempli +0.91% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→68% · +2.0%→45% · +3.0%→31% · +5.0%→18% · +8.0%→3%
- Range intraday médian 4.97% (p90 9.02%) · excursion haute méd. +1.84% / basse méd. −2.04%
- Profil de vol intra : ouverture 2.605% vs midi 1.134% vs clôture 1.278% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 57% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.077)_ ; drift intra méd. -0.167% ; recovery-V 22%
- **σ réalisé intraday** 2.714% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 70% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 270893.75 (VA 270893.75–273981.25 ; dernier close 272000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 48% · **stop −6.28%** sous le fill (sous le bruit) · cible +0.83% · R/R 0.13 (high win-rate)
- Gaps overnight (n=152) : méd. 0.63% · baisse 44% (gap-down >1% 33% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.45%) · haut méd +0.58% · range méd 1.28%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −2.22%) · haut méd +0.75% · range méd 1.91%
- Excursion ouverture 30min (n=160) : bas méd −1.03% (p90 −2.78%) · haut méd +0.93% · range méd 2.23%
- Excursion ouverture 60min (n=160) : bas méd −1.2% (p90 −3.41%) · haut méd +1.17% · range méd 2.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 272500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 48% · séance 63% (90/152) · gap 34% · délai 0.0min · rebond 48% (43/90) (MFE +0.93%)
   - −1.0% : fill 30min 42% · séance 54% (81/152) · gap 33% · délai 0.0min · rebond 57% (43/81) (MFE +1.24%)
   - −1.5% : fill 30min 36% · séance 45% (70/152) · gap 25% · délai 0.0min · rebond 54% (37/70) (MFE +1.5%)
   - −2.0% : fill 30min 31% · séance 43% (66/152) · gap 22% · délai 0.0min · rebond 56% (37/66) (MFE +1.24%)
   - −3.0% : fill 30min 26% · séance 36% (57/152) · gap 21% · délai 0.0min · rebond 47% (30/57) (MFE +0.92%)
   - −4.0% : fill 30min 19% · séance 30% (45/152) · gap 9% · délai 4.0min · rebond 54% (26/45) (MFE +1.18%)
   - −5.0% : fill 30min 9% · séance 19% (32/152) · gap 6% · délai 42.7min · rebond 48% (19/32) (MFE +0.83%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.78%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.41% (p90 −2.52%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.44% (p90 −2.45%) → stop au-delà de −1.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=733 jambes) : jambe baissière méd −1.21% (p90 −2.96%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 97% (54/56) · rebond 47% (24/54)
      · −2.0% : fill 82% (47/56) · rebond 42% (22/47)
      · −3.0% : fill 77% (45/56) · rebond 44% (23/45)
      · −4.0% : fill 67% (37/56) · rebond 51% (21/37)
      · −5.0% : fill 43% (27/56) · rebond 38% (14/27)
   - **flat** (15 séances) :
      · −1.0% : fill 57% (11/15) · rebond 64% (6/11)
      · −2.0% : fill 41% (7/15) · rebond 85% (5/7)
      · −3.0% : fill 18% (4/15) · rebond 18% (1/4)
      · −4.0% : fill 12% (2/15) · rebond 0% (0/2)
      · −5.0% : fill 12% (2/15) · rebond 100% (2/2)
   - **gap-up** (81 séances) :
      · −1.0% : fill 22% (16/81) · rebond 85% (13/16)
      · −2.0% : fill 16% (12/81) · rebond 86% (10/12)
      · −3.0% : fill 10% (8/81) · rebond 78% (6/8)
      · −4.0% : fill 7% (6/81) · rebond 93% (5/6)
      · −5.0% : fill 3% (3/81) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 63% si les 15 1res min sont vertes (78 cas) · 22% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:17** → P(séance verte=clôture>ouverture) 79% si début vert vs 11% si rouge (base 42% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **79%** · continue >prix actuel 61% ; creux résiduel méd -1.08% (q20 -2.63%) → **SL/trailing à −2.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.51% / q75 +3.07% → **scale +1.51% / runner +3.07%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **11%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.93%** (au-delà de la MAE q10 -5.93%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.71% .. +2.46%] · haut q95 +3.2% · bas q05 -3.59%
   - 60min (n=160) : retour [-2.82% .. +3.83%] · haut q95 +4.77% · bas q05 -3.68%
   - 2h (n=160) : retour [-4.24% .. +4.51%] · haut q95 +5.7% · bas q05 -5.26%
   - 4h (n=160) : retour [-5.71% .. +5.05%] · haut q95 +6.33% · bas q05 -7.1%
   - 6h (n=160) : retour [-6.04% .. +5.02%] · haut q95 +6.79% · bas q05 -7.3%
   - session (n=160) : retour [-5.69% .. +5.32%] · haut q95 +6.79% · bas q05 -7.38%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.25 · part idiosyncratique 0.75
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.4  _(neutre)_
- **ADX** : 9.3  _(pas de tendance nette)_
- **MACD** : hist 1356.526  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 16.2%
- **ATR** : 9571.43 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.003  _(neutre)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 46.3  _(transition)_
- **MA** : MA20 263300.0 · MA50 255650.0 · MA200 224655.58  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 +5.0% · MA200 +19.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (558472 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
