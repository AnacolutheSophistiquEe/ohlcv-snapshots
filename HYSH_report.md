# 298040

**Generated** : 2026-10-02T21:58:34.245538+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩2785000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot ₩2785000.00 (+1.9% vs entrée) · entrée ₩2734100.03 · stop ₩2515372.03 · T1 ₩2788135.75 · R/R 0.25  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 126 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2724994.32–₩2743205.75 (mid ₩2734100.03)
- Spot actuel : ₩2785000.00 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : ₩2515372.03 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩2788135.75 · R/R 0.25 | T2 ₩2842171.46 · R/R 0.49 | T3 ₩2896207.18 · R/R 0.74
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2515372.03


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.20 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.88 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1219).
   - exécution **2.806 pt plus bas** dans le cas TYPIQUE (médiane), 2.806 au p90, **2.806 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 8.88 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0023 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.475 % | p01 -4.657 % | pire -11.686 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.061** [0.0324 ; 0.1041] _(largeur 7.2 pt, n_eff 173.1)_
   - swing : **0.5618** [0.5092 ; 0.6134] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.5315** [0.4788 ; 0.5837] _(largeur 10.5 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.94 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.48 % contre 5.73 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.96 % vs -12.54 % si l'on extrapolait par √5 _(rapport 0.954 ; < 1 = le √5 surestime)_
- **β de baisse : 1.073** (β de hausse 0.9972, asymétrie 1.076) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.076 | EV/share : ₩-16708.317 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 25 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 8.2 | side 6.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.826% → cible +1.976% / stop −8.0%, p_fill 66%, n_eff≈75.3) : P(cible|rempli) **43%** · **EV/risk -0.065** (×p_fill ; si rempli -0.79% du capital)
  - **swing** (entrée dip −4.021% → cible +10.126% / stop −5.063%, p_fill 59%, n_eff≈69.0) : P(cible|rempli) **30%** · **EV/risk +0.026** (×p_fill ; si rempli +0.22% du capital)
  - **deep** (entrée dip −6.214% → cible +12.701% / stop −6.351%, p_fill 54%, n_eff≈60.7) : P(cible|rempli) **25%** · **EV/risk -0.084** (×p_fill ; si rempli -0.99% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→50% · +3.0%→34% · +5.0%→18% · +8.0%→5%
- Range intraday médian 5.73% (p90 9.57%) · excursion haute méd. +2.0% / basse méd. −3.17%
- Profil de vol intra : ouverture 3.922% vs midi 1.028% vs clôture 1.049% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 23% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.067)_ ; drift intra méd. -0.709% ; recovery-V 29%
- **σ réalisé intraday** 3.154% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 58% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 2786387.5 (VA 2770862.5–2808812.5 ; dernier close 2782000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 75% · **stop −4.27%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.52 (high win-rate)
- Gaps overnight (n=152) : méd. 0.67% · baisse 34% (gap-down >1% 23% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −1.29% (p90 −2.95%) · haut méd +0.5% · range méd 2.09%
- Excursion ouverture 15min (n=160) : bas méd −1.78% (p90 −3.81%) · haut méd +0.79% · range méd 2.72%
- Excursion ouverture 30min (n=160) : bas méd −2.04% (p90 −4.19%) · haut méd +0.83% · range méd 3.14%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −4.74%) · haut méd +1.16% · range méd 3.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2773000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 70% (101/152) · gap 29% · délai 0.1min · rebond 54% (56/101) (MFE +1.15%)
   - −1.0% : fill 30min 53% · séance 64% (93/152) · gap 23% · délai 0.6min · rebond 47% (48/93) (MFE +0.91%)
   - −1.5% : fill 30min 45% · séance 54% (82/152) · gap 20% · délai 2.3min · rebond 51% (45/82) (MFE +1.02%)
   - −2.0% : fill 30min 40% · séance 51% (76/152) · gap 17% · délai 3.6min · rebond 50% (38/76) (MFE +0.99%)
   - −3.0% : fill 30min 30% · séance 42% (63/152) · gap 9% · délai 7.1min · rebond 65% (40/63) (MFE +1.58%)
   - −4.0% : fill 30min 21% · séance 36% (55/152) · gap 5% · délai 21.8min · rebond 67% (40/55) (MFE +2.23%)
   - −5.0% : fill 30min 13% · séance 26% (41/152) · gap 4% · délai 57.8min · rebond 75% (30/41) (MFE +2.24%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.85% (p90 −2.87%) → stop au-delà de −2.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.96% (p90 −2.53%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −2.46%) → stop au-delà de −1.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=830 jambes) : jambe baissière méd −1.33% (p90 −3.29%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 94% (46/47) · rebond 35% (22/46)
      · −2.0% : fill 90% (41/47) · rebond 43% (19/41)
      · −3.0% : fill 90% (40/47) · rebond 66% (25/40)
      · −4.0% : fill 78% (36/47) · rebond 69% (25/36)
      · −5.0% : fill 57% (27/47) · rebond 83% (21/27)
   - **flat** (21 séances) :
      · −1.0% : fill 87% (17/21) · rebond 55% (10/17)
      · −2.0% : fill 48% (13/21) · rebond 31% (5/13)
      · −3.0% : fill 26% (8/21) · rebond 57% (5/8)
      · −4.0% : fill 26% (8/21) · rebond 54% (6/8)
      · −5.0% : fill 20% (4/21) · rebond 40% (2/4)
   - **gap-up** (84 séances) :
      · −1.0% : fill 39% (30/84) · rebond 60% (16/30)
      · −2.0% : fill 28% (22/84) · rebond 72% (14/22)
      · −3.0% : fill 18% (15/84) · rebond 66% (10/15)
      · −4.0% : fill 13% (11/84) · rebond 66% (9/11)
      · −5.0% : fill 10% (10/84) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 57% si les 15 1res min sont vertes (58 cas) · 31% si rouges (102 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 73% si début vert vs 20% si rouge (base 39% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **73%** · continue >prix actuel 40% ; creux résiduel méd -1.68% (q20 -3.41%) → **SL/trailing à −3.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.47% / q75 +2.92% → **scale +1.47% / runner +2.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=97) : edge inversé — récupère vert seulement **20%** (continue à baisser 55%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.45%** (au-delà de la MAE q10 -5.45%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.59% .. +3.88%] · haut q95 +5.86% · bas q05 -5.06%
   - 60min (n=160) : retour [-4.92% .. +3.28%] · haut q95 +5.93% · bas q05 -5.44%
   - 2h (n=160) : retour [-5.38% .. +3.62%] · haut q95 +6.11% · bas q05 -6.32%
   - 4h (n=160) : retour [-6.38% .. +4.58%] · haut q95 +6.12% · bas q05 -7.89%
   - 6h (n=160) : retour [-7.23% .. +5.18%] · haut q95 +6.33% · bas q05 -8.46%
   - session (n=160) : retour [-6.55% .. +5.41%] · haut q95 +6.33% · bas q05 -8.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.12 · part idiosyncratique 0.88
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.5  _(momentum baissier)_
- **ADX** : 6.9  _(pas de tendance nette)_
- **MACD** : hist -8084.634  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 10.6%
- **ATR** : 108071.43 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.04  _(neutre)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 57.8  _(transition)_
- **MA** : MA20 2834200.0 · MA50 2783380.0 · MA200 2837691.2  _(prix < MA20)_
- **Dist MA** : MA20 -1.7% · MA50 +0.1% · MA200 -1.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (546053 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
