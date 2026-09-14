# 005930

**Generated** : 2026-09-14T22:00:31.690972+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩249000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩249000.00 (+1.4% vs entrée) · entrée ₩245516.67 · stop ₩234945.24 · T1 ₩258391.11 · R/R 1.22  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.183 _(réel 5 s)_ (GBM 0.364) · ¼-Kelly 0.036 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩242941.78–₩248091.56 (mid ₩245516.67)
- Spot actuel : ₩249000.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩234945.24 (stop swing_plan-based (-5.64%))
- Targets : T1 ₩258391.11 · R/R 1.22 | T2 ₩271265.55 · R/R 2.44 | T3 ₩284139.99 · R/R 3.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩234945.24


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.11 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.64 %)** : le gap seul le franchit 0.411 % des séances (5 fois sur 1218).
   - exécution **2.15 pt plus bas** dans le cas TYPIQUE (médiane), 4.05 au p90, **5.302 au pire**
   - perte réelle **7.795 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 5.64 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0088 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.482 % | p01 -4.951 % | pire -10.942 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0474** [0.0229 ; 0.0868] _(largeur 6.4 pt, n_eff 173.1)_
   - swing : **0.3431** [0.2945 ; 0.3943] _(largeur 10.0 pt, n_eff 345.6)_
   - deep : **0.3063** [0.2595 ; 0.3564] _(largeur 9.7 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 35.2 observations effectives », dont la borne haute a 95 % vaut environ 8.5 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 33.6 observations effectives », dont la borne haute a 95 % vaut environ 8.9 %.
- ⚠ **5 s — échantillon insuffisant sur : swing (30.9 pt), deep (31.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.73 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.71 % contre 5.78 % aujourd'hui, rapport 0.47)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.38 % vs -7.31 % si l'on extrapolait par √5 _(rapport 0.874 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1699** (β de hausse 1.3374, asymétrie 0.8748) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.364 | EV/share : ₩3852.536 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 29 % | T3 15 %
- Kelly (position) : f* 0.145 | ¼-Kelly 0.036 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.2 | bear 5.1 | side 9.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.641% → cible +6.271% / stop −8.0%, p_fill 86%, n_eff≈36.8) : P(cible|rempli) **14%** · **EV/risk -0.028** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −1.394% → cible +5.244% / stop −4.306%, p_fill 82%, n_eff≈35.2) : P(cible|rempli) **37%** · **EV/risk -0.183** (×p_fill ; si rempli -0.96% du capital)
  - **deep** (entrée dip −2.162% → cible +7.416% / stop −6.509%, p_fill 83%, n_eff≈33.6) : P(cible|rempli) **36%** · **EV/risk -0.245** (×p_fill ; si rempli -1.92% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→46% · +3.0%→36% · +5.0%→22% · +8.0%→4%
- Range intraday médian 6.16% (p90 9.84%) · excursion haute méd. +1.88% / basse méd. −3.0%
- Profil de vol intra : ouverture 3.103% vs midi 1.331% vs clôture 1.544% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓1% ; spike-down 67% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.088)_ ; drift intra méd. -0.38% ; recovery-V 24%
- **σ réalisé intraday** 3.594% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 68% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 254825.0 (VA 254525.0–258725.0 ; dernier close 256000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 51% · **stop −6.12%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.17 (high win-rate)
- Gaps overnight (n=159) : méd. 0.85% · baisse 44% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.64%) · haut méd +0.6% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.35%) · haut méd +0.8% · range méd 2.07%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.13%) · haut méd +1.01% · range méd 2.44%
- Excursion ouverture 60min (n=160) : bas méd −1.56% (p90 −3.58%) · haut méd +1.23% · range méd 3.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 255500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 68% (97/159) · gap 38% · délai 0.0min · rebond 46% (48/97) (MFE +0.92%)
   - −1.0% : fill 30min 46% · séance 60% (88/159) · gap 36% · délai 0.0min · rebond 57% (49/88) (MFE +1.3%)
   - −1.5% : fill 30min 43% · séance 53% (77/159) · gap 29% · délai 0.0min · rebond 60% (45/77) (MFE +1.52%)
   - −2.0% : fill 30min 37% · séance 51% (72/159) · gap 25% · délai 0.0min · rebond 62% (44/72) (MFE +1.83%)
   - −3.0% : fill 30min 30% · séance 44% (62/159) · gap 23% · délai 0.0min · rebond 51% (34/62) (MFE +1.05%)
   - −4.0% : fill 30min 21% · séance 34% (47/159) · gap 10% · délai 5.8min · rebond 50% (27/47) (MFE +1.06%)
   - −5.0% : fill 30min 13% · séance 25% (36/159) · gap 9% · délai 18.2min · rebond 51% (23/36) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.88%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −2.88%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.71%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=772 jambes) : jambe baissière méd −1.21% (p90 −3.02%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 97% (59/62) · rebond 49% (29/59)
      · −2.0% : fill 89% (51/62) · rebond 51% (27/51)
      · −3.0% : fill 84% (48/62) · rebond 46% (25/48)
      · −4.0% : fill 70% (38/62) · rebond 46% (21/38)
      · −5.0% : fill 52% (30/62) · rebond 41% (17/30)
   - **flat** (14 séances) :
      · −1.0% : fill 73% (11/14) · rebond 58% (6/11)
      · −2.0% : fill 48% (7/14) · rebond 81% (5/7)
      · −3.0% : fill 33% (5/14) · rebond 33% (2/5)
      · −4.0% : fill 24% (3/14) · rebond 25% (1/3)
      · −5.0% : fill 24% (3/14) · rebond 100% (3/3)
   - **gap-up** (83 séances) :
      · −1.0% : fill 30% (18/83) · rebond 77% (14/18)
      · −2.0% : fill 22% (14/83) · rebond 88% (12/14)
      · −3.0% : fill 15% (9/83) · rebond 82% (7/9)
      · −4.0% : fill 8% (6/83) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/83) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 60% si les 15 1res min sont vertes (79 cas) · 22% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 72% si début vert vs 9% si rouge (base 40% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 216min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **72%** · continue >prix actuel 62% ; creux résiduel méd -1.3% (q20 -4.5%) → **SL/trailing à −4.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.16% / q75 +4.03% → **scale +2.16% / runner +4.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **9%** (continue à baisser 69%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.34%** (au-delà de la MAE q10 -6.34%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +2.61%] · haut q95 +3.44% · bas q05 -3.68%
   - 60min (n=160) : retour [-3.07% .. +4.19%] · haut q95 +4.93% · bas q05 -4.26%
   - 2h (n=160) : retour [-4.5% .. +4.63%] · haut q95 +5.86% · bas q05 -5.54%
   - 4h (n=160) : retour [-5.86% .. +5.26%] · haut q95 +6.82% · bas q05 -7.38%
   - 6h (n=160) : retour [-6.62% .. +5.26%] · haut q95 +6.92% · bas q05 -7.66%
   - session (n=160) : retour [-6.16% .. +5.39%] · haut q95 +6.92% · bas q05 -8.38%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 9.4  _(pas de tendance nette)_
- **MACD** : hist -105.735  _(bearish_recent)_
- **BB** : %B 0.15 · largeur 13.7%
- **ATR** : 10571.43 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.013  _(neutre)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 53.6  _(transition)_
- **MA** : MA20 261525.0 · MA50 258720.0 · MA200 216337.37  _(prix < MA20)_
- **Dist MA** : MA20 -4.8% · MA50 -3.8% · MA200 +15.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (480419 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
