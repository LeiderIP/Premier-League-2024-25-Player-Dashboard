# Premier League 2024/25 — Player Dashboard

A full one-page report card for any outfield Premier League player — form, touch heatmap, shot map, and percentile comparison against peers in the same position. Built from StatsBomb event data.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python) ![SVG](https://img.shields.io/badge/Viz-SVG%20%2B%20JS-orange?style=flat-square) ![Data](https://img.shields.io/badge/Data-StatsBomb-red?style=flat-square)

---

## Live Demo

**[Open Player Dashboard](https://leiderip.github.io/Premier-League-2024-25-Player-Dashboard/Player_Dashboard.html)**

---

## Features

- **KPI strip** — minutes, matches, goals, assists, xG, shots, pass completion
- **Recent form** — last 10 matches as colour-coded chips, hoverable for goals/assists that game
- **Percentile rank** — goals, assists, xG, and shots per 90, plus pass completion, all compared only against players in the same broad position group (defenders, midfielders, forwards)
- **Touch heatmap** — average position across every touch of the season, on a full pitch
- **Season shot map** — every shot taken, sized by xG, goals highlighted, hoverable
- **Discipline** — fouls, yellow and red cards
- Search across hundreds of qualifying players
- **Dark / Light theme toggle**

---

## Method

Only outfield players with at least 450 minutes are included; goalkeepers are excluded since they already have a dedicated [Goalkeeper Performance](https://leiderip.github.io/Premier-League-2024-25-Goalkeeper-Performance/Goalkeeper_Performance.html) project built around shot-stopping metrics that don't apply to outfield play.

**Minutes played** uses the corrected StatsBomb substitution convention: in a `Substitution` event, `player_name` is the player leaving the pitch and `substituted_player_name` is the replacement coming on.

**Assists** are detected by matching each completed pass's `assisted_shot_id` against the set of shot IDs that resulted in a goal — StatsBomb doesn't tag assists directly on the pass, only the shot it led to.

**Position group** is the most frequent formation position a player lined up in across the season, bucketed into Defender, Midfielder, or Forward. Percentiles are computed only within that cohort, so a winger's shot volume isn't compared against a center-back's.

---

## Portfolio

| Project | Link |
|---|---|
| Title Race | [Live](https://leiderip.github.io/Premier-League-2024-25-Title-race/pl_position_race.html) |
| xG Race Explorer | [Live](https://leiderip.github.io/Premier-League-2024-25-xG-Title-race-/xG_Race_Explorer.html) |
| Season Shot Map | [Live](https://leiderip.github.io/Premier-League-2024-25-Shot-Map/Shot_Map.html) |
| Top Scorers vs xG | [Live](https://leiderip.github.io/Premier-League-2024-25-Top-Scorers-xG/Top_Scorers_xG.html) |
| Player Heatmap | [Live](https://leiderip.github.io/Premier-League-2024-25-Player-Heatmap/Player_Heatmap.html) |
| Scouting Radar | [Live](https://leiderip.github.io/Premier-League-2024-25-Scouting_Radar/Scouting_Radar.html) |
| Pass Network | [Live](https://leiderip.github.io/Premier-League-2024-25-Pass-Network/Pass_Network.html) |
| Match Momentum | [Live](https://leiderip.github.io/Premier-League-2024-25-Match-Momentum/Match_Momentum.html) |
| Goalkeeper Performance | [Live](https://leiderip.github.io/Premier-League-2024-25-Goalkeeper-Performance/Goalkeeper_Performance.html) |
| Attacking Bands | [Live](https://leiderip.github.io/Premier-League-2024-25-Attacking-Bands/Attacking_Bands.html) |
| Set Piece Threat | [Live](https://leiderip.github.io/Premier-League-2024-25-Set-Piece-Threat/Set_Piece_Threat.html) |
| Goal Rain | [Live](https://leiderip.github.io/Premier-League-2024-25-Goal-Rain/Goal_Rain.html) |
| Team Dashboard | [Live](https://leiderip.github.io/Premier-League-2024-25-Team-Dashboard/Team_Dashboard.html) |
| Player Dashboard | This project |

---

*Data © StatsBomb.*
