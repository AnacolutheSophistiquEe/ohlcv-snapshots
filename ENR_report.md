# ENR

**Generated** : 2026-07-17T21:40:28.900362+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €147.66  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €147.66 (+6.3% vs entrée) · entrée €138.86 · stop €127.75 · T1 €141.41 · R/R 0.23  
> ↳ P(T1 av. stop) 47 % · EV/risk -0.031 · ¼-Kelly 0.077 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -69 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €138.35–€139.37 (mid €138.86)
- Spot actuel : €147.66 (+6.3% au-dessus de la zone — repli à attendre)
- Stop : €127.75 (stop swing_plan-based (-14.89%))
- Targets : T1 €141.41 · R/R 0.23 | T2 €143.95 · R/R 0.46 | T3 €146.50 · R/R 0.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.75


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : €-0.347 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 19 % | T3 9 %
- Kelly (position) : f* 0.307 | ¼-Kelly 0.077 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.4 | bear 26.3 | side 66.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→60% · +2.0%→45% · +3.0%→25% · +5.0%→9% · +8.0%→0%
- Range intraday médian 4.08% (p90 6.03%) · excursion haute méd. +1.47% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.104% vs midi 0.913% vs clôture 1.151% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.01)_ ; drift intra méd. -0.447% ; recovery-V 23%
- **σ réalisé intraday** 2.527% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 65% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 148.0012 (VA 147.0938–149.4532 ; dernier close 148.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 15% · rebond 67% · **stop −2.92%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.33% · baisse 40% (gap-down >1% 22% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.85%) · haut méd +0.44% · range méd 1.2%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.22%) · haut méd +0.59% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.88% (p90 −2.39%) · haut méd +0.6% · range méd 1.86%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.66%) · haut méd +0.66% · range méd 1.99%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 148.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (117/159) · gap 30% · délai 0.4min · rebond 54% (61/117) (MFE +1.15%)
   - −1.0% : fill 30min 52% · séance 70% (106/159) · gap 22% · délai 1.2min · rebond 58% (63/106) (MFE +1.36%)
   - −1.5% : fill 30min 41% · séance 61% (91/159) · gap 19% · délai 10.5min · rebond 61% (58/91) (MFE +1.54%)
   - −2.0% : fill 30min 25% · séance 45% (66/159) · gap 14% · délai 11.3min · rebond 58% (39/66) (MFE +1.26%)
   - −3.0% : fill 30min 15% · séance 33% (49/159) · gap 5% · délai 92.0min · rebond 65% (35/49) (MFE +1.51%)
   - −4.0% : fill 30min 8% · séance 23% (37/159) · gap 3% · délai 285.2min · rebond 60% (25/37) (MFE +1.23%)
   - −5.0% : fill 30min 3% · séance 15% (21/159) · gap 1% · délai 203.6min · rebond 67% (14/21) (MFE +1.36%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.73%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −2.04%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.45%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=493 jambes) : jambe baissière méd −1.04% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 96% (47/48) · rebond 56% (27/47)
      · −2.0% : fill 72% (34/48) · rebond 61% (22/34)
      · −3.0% : fill 57% (28/48) · rebond 55% (19/28)
      · −4.0% : fill 44% (23/48) · rebond 55% (16/23)
      · −5.0% : fill 32% (15/48) · rebond 63% (10/15)
   - **flat** (27 séances) :
      · −1.0% : fill 75% (21/27) · rebond 74% (15/21)
      · −2.0% : fill 32% (9/27) · rebond 56% (4/9)
      · −3.0% : fill 16% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 14% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 8% (2/27) · rebond 74% (1/2)
   - **gap-up** (84 séances) :
      · −1.0% : fill 50% (38/84) · rebond 51% (21/38)
      · −2.0% : fill 32% (23/84) · rebond 54% (13/23)
      · −3.0% : fill 23% (16/84) · rebond 78% (13/16)
      · −4.0% : fill 12% (10/84) · rebond 67% (7/10)
      · −5.0% : fill 6% (4/84) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 88% si les 15 1res min sont vertes (75 cas) · 23% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 88% si début vert vs 23% si rouge (base 49% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **88%** · continue >prix actuel 71% ; creux résiduel méd -1.16% (q20 -2.08%) → **SL/trailing à −2.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.32% → **scale +2.05% / runner +3.32%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **23%** (continue à baisser 66%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.81%** (au-delà de la MAE q10 -4.81%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.27% .. +2.25%] · haut q95 +2.65% · bas q05 -2.86%
   - 60min (n=160) : retour [-2.5% .. +2.34%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.86% .. +2.62%] · haut q95 +3.06% · bas q05 -3.91%
   - 4h (n=160) : retour [-2.75% .. +2.62%] · haut q95 +3.95% · bas q05 -3.97%
   - 6h (n=160) : retour [-3.32% .. +3.66%] · haut q95 +4.61% · bas q05 -4.43%
   - session (n=160) : retour [-5.2% .. +4.34%] · haut q95 +5.45% · bas q05 -5.74%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 1.3% / strong 3.7%) · base = 8 séances trend-up (n_eff 6.1)
- **ARMER** : fenêtre la + prédictive = **30 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 25% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.14% / p90 1.33%) · ~3.0 replis/séance, durée méd 68.37 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 40.0 min, n=24)
   - −1.0% → **100%** (reprise méd 77.51 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.33%** (p90, défaut prudent ; serré/agressif −1.14%) ; extension open→close méd +4.34% (q75 +4.76% / q95 +6.23%), MFE méd +4.72% / q90 +6.39%
   - Échelle scale-out : +4.72% (33%) / +5.59% (33%) / +6.39% (34%)
- **DÉSARMER** : repli > **−1.33%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.39% : P(retournement après) 0% (mèche méd 0.4%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.53%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.7  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist -1.179  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 18.1%
- **ATR** : 7.16 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.094  _(distribution)_
- **Vol ratio** : 1.15  _(volume normal)_
- **Choppiness** : 49.3  _(transition)_
- **MA** : MA20 158.42 · MA50 162.44 · MA200 142.44  _(prix < MA20)_
- **Dist MA** : MA20 -6.8% · MA50 -9.1% · MA200 +3.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93717 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
