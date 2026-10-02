# 267260

**Generated** : 2026-10-02T21:57:10.763702+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩678000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot ₩678000.00 (+5.5% vs entrée) · entrée ₩642771.14 · stop ₩591349.45 · T1 ₩656128.28 · R/R 0.26  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩640892.35–₩644649.92 (mid ₩642771.14)
- Spot actuel : ₩678000.00 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : ₩591349.45 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩656128.28 · R/R 0.26 | T2 ₩669485.42 · R/R 0.52 | T3 ₩682842.57 · R/R 0.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩591349.45


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.37 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 15.37 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.67 % | p01 -4.805 % | pire -11.715 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0633** [0.034 ; 0.107] _(largeur 7.3 pt, n_eff 173.1)_
   - swing : **0.5056** [0.453 ; 0.5581] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4656** [0.4135 ; 0.5183] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.68 %** | CVaR **-8.85 %** | vol 4.43 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.78 % contre 4.91 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.81 % vs -11.99 % si l'on extrapolait par √5 _(rapport 0.901 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0344** (β de hausse 0.8407, asymétrie 1.2305) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.102 | EV/share : ₩-5228.204 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 16 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 7.3 | side 7.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.196% → cible +2.078% / stop −8.0%, p_fill 22%, n_eff≈29.7) : P(cible|rempli) **41%** · **EV/risk -0.007** (×p_fill ; si rempli -0.24% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=13))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=12))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→65% · +2.0%→43% · +3.0%→30% · +5.0%→10% · +8.0%→3%
- Range intraday médian 5.43% (p90 9.76%) · excursion haute méd. +1.61% / basse méd. −3.14%
- Profil de vol intra : ouverture 3.862% vs midi 1.056% vs clôture 1.135% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 84% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.096)_ ; drift intra méd. -0.754% ; recovery-V 20%
- **σ réalisé intraday** 3.145% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 65% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 666312.5 (VA 658437.5–682062.5 ; dernier close 665000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 73% · **stop −4.39%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.5 (high win-rate)
- Gaps overnight (n=152) : méd. 0.42% · baisse 39% (gap-down >1% 21% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −1.48% (p90 −3.67%) · haut méd +0.82% · range méd 2.5%
- Excursion ouverture 15min (n=160) : bas méd −1.66% (p90 −3.96%) · haut méd +0.88% · range méd 3.05%
- Excursion ouverture 30min (n=160) : bas méd −1.82% (p90 −4.64%) · haut méd +0.97% · range méd 3.22%
- Excursion ouverture 60min (n=160) : bas méd −1.95% (p90 −4.79%) · haut méd +1.08% · range méd 3.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 662000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (103/152) · gap 31% · délai 0.0min · rebond 50% (49/103) (MFE +0.99%)
   - −1.0% : fill 30min 55% · séance 67% (96/152) · gap 21% · délai 0.1min · rebond 54% (53/96) (MFE +1.18%)
   - −1.5% : fill 30min 49% · séance 64% (89/152) · gap 18% · délai 0.4min · rebond 60% (54/89) (MFE +1.18%)
   - −2.0% : fill 30min 42% · séance 57% (81/152) · gap 13% · délai 1.1min · rebond 66% (54/81) (MFE +1.62%)
   - −3.0% : fill 30min 33% · séance 49% (68/152) · gap 8% · délai 3.4min · rebond 70% (49/68) (MFE +1.77%)
   - −4.0% : fill 30min 21% · séance 35% (52/152) · gap 4% · délai 8.8min · rebond 73% (37/52) (MFE +1.72%)
   - −5.0% : fill 30min 12% · séance 26% (40/152) · gap 2% · délai 37.1min · rebond 73% (29/40) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −3.14%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.98% (p90 −3.02%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −3.95%) → stop au-delà de −3.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=829 jambes) : jambe baissière méd −1.16% (p90 −3.18%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 100% (50/50) · rebond 48% (25/50)
      · −2.0% : fill 99% (47/50) · rebond 62% (29/47)
      · −3.0% : fill 92% (43/50) · rebond 75% (31/43)
      · −4.0% : fill 68% (34/50) · rebond 75% (24/34)
      · −5.0% : fill 52% (27/50) · rebond 76% (21/27)
   - **flat** (16 séances) :
      · −1.0% : fill 97% (15/16) · rebond 65% (9/15)
      · −2.0% : fill 66% (11/16) · rebond 55% (8/11)
      · −3.0% : fill 54% (9/16) · rebond 34% (5/9)
      · −4.0% : fill 35% (7/16) · rebond 63% (4/7)
      · −5.0% : fill 35% (7/16) · rebond 72% (5/7)
   - **gap-up** (86 séances) :
      · −1.0% : fill 39% (31/86) · rebond 59% (19/31)
      · −2.0% : fill 28% (23/86) · rebond 79% (17/23)
      · −3.0% : fill 19% (16/86) · rebond 75% (13/16)
      · −4.0% : fill 13% (11/86) · rebond 72% (9/11)
      · −5.0% : fill 6% (6/86) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 33% en base · 43% si les 15 1res min sont vertes (63 cas) · 28% si rouges (97 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:30** → P(séance verte=clôture>ouverture) 74% si début vert vs 13% si rouge (base 33% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **74%** · continue >prix actuel 47% ; creux résiduel méd -1.44% (q20 -3.73%) → **SL/trailing à −3.73%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.56% / q75 +2.75% → **scale +1.56% / runner +2.75%**, sortie à la clôture
  - **si ROUGE au coude** (n=97) : edge inversé — récupère vert seulement **13%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.23%** (au-delà de la MAE q10 -4.23%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.37% .. +2.67%] · haut q95 +3.82% · bas q05 -5.13%
   - 60min (n=160) : retour [-5.23% .. +2.47%] · haut q95 +4.31% · bas q05 -5.71%
   - 2h (n=160) : retour [-5.69% .. +3.48%] · haut q95 +4.62% · bas q05 -6.46%
   - 4h (n=160) : retour [-6.41% .. +3.52%] · haut q95 +4.79% · bas q05 -7.88%
   - 6h (n=160) : retour [-6.79% .. +4.63%] · haut q95 +5.43% · bas q05 -8.58%
   - session (n=160) : retour [-6.57% .. +4.61%] · haut q95 +5.75% · bas q05 -8.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.5%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.6  _(survente)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist -3512.777  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 15.4%
- **ATR** : 26714.29 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.128  _(distribution)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 713050.0 · MA50 733970.26 · MA200 911027.26  _(prix < MA20)_
- **Dist MA** : MA20 -4.9% · MA50 -7.6% · MA200 -25.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (542843 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
