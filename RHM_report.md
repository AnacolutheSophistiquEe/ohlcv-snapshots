# RHM

**Generated** : 2026-08-17T00:01:55.213059+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €1202.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1202.00 (+1.4% vs entrée) · entrée €1185.15 · stop €1161.45 · T1 €1198.47 · R/R 0.56  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk -0.013 _(réel 5 s)_ (GBM 0.141) · ¼-Kelly 0.053 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 76.0 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1182.49–€1187.81 (mid €1185.15)
- Spot actuel : €1202.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : €1161.45 (stop swing_plan-based (-7.96%))
- Targets : T1 €1198.47 · R/R 0.56 | T2 €1211.79 · R/R 1.12 | T3 €1225.12 · R/R 1.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1161.45


## Edge, scénarios & sizing

- EV/risk : 0.141 | EV/share : €3.337 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 68 % | T2 45 % | T3 28 %
- Kelly (position) : f* 0.214 | ¼-Kelly 0.053 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.4 | bear 5.4 | side 78.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.398% → cible +1.124% / stop −2.0%, p_fill 53%, n_eff≈21.7) : P(cible|rempli) **41%** · **EV/risk -0.013** (×p_fill ; si rempli -0.05% du capital)
  - **swing** (entrée dip −3.081% → cible +2.514% / stop −5.034%, p_fill 41%, n_eff≈15.4) : P(cible|rempli) **74%** · **EV/risk +0.053** (×p_fill ; si rempli +0.66% du capital)
  - **deep** (entrée dip −4.761% → cible +3.555% / stop −7.684%, p_fill 25%, n_eff≈16.4) : P(cible|rempli) **38%** · **EV/risk -0.107** (×p_fill ; si rempli -3.25% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→74% · +2.0%→52% · +3.0%→34% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.23% / basse méd. −1.51%
- Profil de vol intra : ouverture 2.667% vs midi 0.933% vs clôture 1.107% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.086 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.133% ; recovery-V 33%
- **σ réalisé intraday** 2.88% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 60% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 1200.275 (VA 1195.925–1207.525 ; dernier close 1201.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 40% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. 0.24% · baisse 34% (gap-down >1% 10% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −1.53%) · haut méd +0.59% · range méd 1.37%
- Excursion ouverture 15min (n=160) : bas méd −0.87% (p90 −1.97%) · haut méd +0.73% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −0.91% (p90 −2.26%) · haut méd +0.99% · range méd 2.04%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.58%) · haut méd +1.08% · range méd 2.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1201.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 70% (117/159) · gap 23% · délai 0.4min · rebond 56% (63/117) (MFE +1.28%)
   - −1.0% : fill 30min 39% · séance 63% (106/159) · gap 10% · délai 6.2min · rebond 63% (62/106) (MFE +1.31%)
   - −1.5% : fill 30min 26% · séance 53% (85/159) · gap 6% · délai 28.4min · rebond 62% (48/85) (MFE +1.38%)
   - −2.0% : fill 30min 20% · séance 40% (72/159) · gap 6% · délai 30.4min · rebond 67% (45/72) (MFE +1.57%)
   - −3.0% : fill 30min 9% · séance 24% (45/159) · gap 4% · délai 116.9min · rebond 62% (27/45) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 18% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 10% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.62%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.75%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.78%) → stop au-delà de −1.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=519 jambes) : jambe baissière méd −1.07% (p90 −2.55%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 94% (46/48) · rebond 65% (27/46)
      · −2.0% : fill 80% (38/48) · rebond 66% (25/38)
      · −3.0% : fill 53% (26/48) · rebond 63% (16/26)
      · −4.0% : fill 41% (16/48) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/48) · rebond 83% (7/9)
   - **flat** (47 séances) :
      · −1.0% : fill 64% (33/47) · rebond 72% (21/33)
      · −2.0% : fill 25% (17/47) · rebond 72% (10/17)
      · −3.0% : fill 17% (10/47) · rebond 55% (5/10)
      · −4.0% : fill 15% (8/47) · rebond 36% (2/8)
      · −5.0% : fill 10% (6/47) · rebond 22% (1/6)
   - **gap-up** (64 séances) :
      · −1.0% : fill 44% (27/64) · rebond 53% (14/27)
      · −2.0% : fill 26% (17/64) · rebond 67% (10/17)
      · −3.0% : fill 12% (9/64) · rebond 66% (6/9)
      · −4.0% : fill 7% (4/64) · rebond 61% (3/4)
      · −5.0% : fill 2% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 62% si les 15 1res min sont vertes (81 cas) · 40% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 69% si début vert vs 31% si rouge (base 51% · écart 39 pts) ; prédictivité sature ensuite (plafond brut 300min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **69%** · continue >prix actuel 42% ; creux résiduel méd -1.49% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +2.03% → **scale +1.31% / runner +2.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **31%** (continue à baisser 46%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.62% .. +3.31%] · haut q95 +3.81% · bas q05 -3.22%
   - 60min (n=160) : retour [-2.84% .. +3.23%] · haut q95 +4.51% · bas q05 -4.1%
   - 2h (n=160) : retour [-3.27% .. +3.1%] · haut q95 +4.51% · bas q05 -4.56%
   - 4h (n=160) : retour [-3.61% .. +3.37%] · haut q95 +4.87% · bas q05 -4.72%
   - 6h (n=160) : retour [-4.27% .. +3.43%] · haut q95 +5.0% · bas q05 -5.21%
   - session (n=160) : retour [-5.78% .. +4.19%] · haut q95 +5.11% · bas q05 -6.17%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 76.0  _(surachat)_
- **ADX** : 23.7  _(pas de tendance nette)_
- **MACD** : hist 8.964  _(pas de croisement recent)_
- **BB** : %B 0.8 · largeur 28.2%
- **ATR** : 58.64 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.063  _(distribution)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 53.1  _(transition)_
- **MA** : MA20 1108.18 · MA50 1097.52 · MA200 1433.8  _(prix > MA20)_
- **Dist MA** : MA20 +8.5% · MA50 +9.5% · MA200 -16.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91075 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
