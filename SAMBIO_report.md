# 207940

**Generated** : 2026-10-01T00:20:49.444796+00:00  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩1391000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩1391000.00 (+2.2% vs entrée) · entrée ₩1361375.00 · stop ₩1252465.00 · T1 ₩1376910.71 · R/R 0.14  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1359579.17–₩1363170.83 (mid ₩1361375.00)
- Spot actuel : ₩1391000.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1252465.00 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩1376910.71 · R/R 0.14 | T2 ₩1392446.43 · R/R 0.29 | T3 ₩1407982.14 · R/R 0.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1252465.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (6.92 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 6.92 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.276 % | p01 -2.672 % | pire -5.458 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0039** [0.0003 ; 0.0231] _(largeur 2.3 pt, n_eff 173.1)_
   - swing : **0.518** [0.4654 ; 0.5703] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5184** [0.4658 ; 0.5707] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 42.0 observations effectives », dont la borne haute a 95 % vaut environ 7.2 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 22.5 observations effectives », dont la borne haute a 95 % vaut environ 13.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.3 pt), swing (38.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.06 %** | CVaR **-5.87 %** | vol 2.56 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.54 % contre 2.65 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.55 % vs -6.16 % si l'on extrapolait par √5 _(rapport 0.901 ; < 1 = le √5 surestime)_
- **β de baisse : 0.312** (β de hausse 0.2187, asymétrie 1.4265) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : ₩-4270.139 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 30 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 69.2 | side 25.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.13% → cible +1.141% / stop −8.0%, p_fill 35%, n_eff≈42.0) : P(cible|rempli) **46%** · **EV/risk +0.005** (×p_fill ; si rempli +0.12% du capital)
  - **swing** (entrée dip −4.686% → cible +2.62% / stop −2.344%, p_fill 19%, n_eff≈22.5) : P(cible|rempli) **58%** · **EV/risk +0.032** (×p_fill ; si rempli +0.40% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=14))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→53% · +2.0%→33% · +3.0%→21% · +5.0%→4% · +8.0%→2%
- Range intraday médian 3.64% (p90 6.09%) · excursion haute méd. +1.04% / basse méd. −1.54%
- Profil de vol intra : ouverture 2.243% vs midi 0.637% vs clôture 0.773% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑1%/↓2% ; spike-down 48% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.104)_ ; drift intra méd. -0.17% ; recovery-V 21%
- **σ réalisé intraday** 1.901% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 57% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 1371112.5 (VA 1369087.5–1388662.5 ; dernier close 1384000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 40% · rebond 60% · **stop −2.76%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.46 (high win-rate)
- Gaps overnight (n=152) : méd. 0.07% · baisse 40% (gap-down >1% 19% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.1%) · haut méd +0.46% · range méd 1.28%
- Excursion ouverture 15min (n=160) : bas méd −0.87% (p90 −2.47%) · haut méd +0.55% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.68%) · haut méd +0.59% · range méd 1.73%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −3.16%) · haut méd +0.77% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1385000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 81% (110/152) · gap 27% · délai 0.2min · rebond 46% (50/110) (MFE +0.89%)
   - −1.0% : fill 30min 48% · séance 64% (89/152) · gap 19% · délai 1.1min · rebond 54% (43/89) (MFE +1.01%)
   - −1.5% : fill 30min 35% · séance 51% (71/152) · gap 8% · délai 2.7min · rebond 51% (32/71) (MFE +1.07%)
   - −2.0% : fill 30min 24% · séance 40% (58/152) · gap 5% · délai 6.2min · rebond 60% (31/58) (MFE +1.28%)
   - −3.0% : fill 30min 10% · séance 19% (34/152) · gap 2% · délai 29.9min · rebond 46% (17/34) (MFE +0.92%)
   - −4.0% : fill 30min 5% · séance 11% (18/152) · gap 2% · délai 50.2min · rebond 55% (9/18) (MFE +1.38%)
   - −5.0% : fill 30min 2% · séance 6% (10/152) · gap 2% · délai 110.1min · rebond 80% (8/10) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.96%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.11%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=396 jambes) : jambe baissière méd −1.07% (p90 −2.65%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 100% (43/44) · rebond 63% (24/43)
      · −2.0% : fill 69% (32/44) · rebond 72% (17/32)
      · −3.0% : fill 26% (18/44) · rebond 44% (9/18)
      · −4.0% : fill 18% (10/44) · rebond 58% (5/10)
      · −5.0% : fill 10% (6/44) · rebond 100% (6/6)
   - **flat** (40 séances) :
      · −1.0% : fill 64% (26/40) · rebond 35% (7/26)
      · −2.0% : fill 39% (14/40) · rebond 30% (6/14)
      · −3.0% : fill 29% (10/40) · rebond 50% (6/10)
      · −4.0% : fill 12% (5/40) · rebond 60% (3/5)
      · −5.0% : fill 5% (2/40) · rebond 55% (1/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 36% (20/68) · rebond 54% (12/20)
      · −2.0% : fill 18% (12/68) · rebond 67% (8/12)
      · −3.0% : fill 7% (6/68) · rebond 42% (2/6)
      · −4.0% : fill 5% (3/68) · rebond 38% (1/3)
      · −5.0% : fill 3% (2/68) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 77% si les 15 1res min sont vertes (54 cas) · 27% si rouges (106 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **24min** → P(séance verte=clôture>ouverture) 79% si début vert vs 20% si rouge (base 45% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 220min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **79%** · continue >prix actuel 50% ; creux résiduel méd -1.09% (q20 -1.92%) → **SL/trailing à −1.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.13% / q75 +2.34% → **scale +1.13% / runner +2.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=98) : edge inversé — récupère vert seulement **20%** (continue à baisser 59%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.28%** (au-delà de la MAE q10 -3.28%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.06% .. +2.38%] · haut q95 +2.82% · bas q05 -3.49%
   - 60min (n=160) : retour [-3.27% .. +2.27%] · haut q95 +3.1% · bas q05 -3.82%
   - 2h (n=160) : retour [-3.3% .. +2.96%] · haut q95 +4.03% · bas q05 -4.46%
   - 4h (n=160) : retour [-3.33% .. +2.6%] · haut q95 +4.14% · bas q05 -4.77%
   - 6h (n=160) : retour [-4.02% .. +3.2%] · haut q95 +4.59% · bas q05 -5.06%
   - session (n=160) : retour [-3.89% .. +3.15%] · haut q95 +4.59% · bas q05 -5.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 1.99%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.0  _(momentum baissier)_
- **ADX** : 24.7  _(pas de tendance nette)_
- **MACD** : hist -2517.858  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 11.4%
- **ATR** : 31071.43 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.036  _(neutre)_
- **Vol ratio** : 1.39  _(volume normal)_
- **Choppiness** : 58.1  _(transition)_
- **MA** : MA20 1425550.0 · MA50 1479180.0 · MA200 1552000.0  _(prix < MA20)_
- **Dist MA** : MA20 -2.4% · MA50 -6.0% · MA200 -10.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (549397 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
