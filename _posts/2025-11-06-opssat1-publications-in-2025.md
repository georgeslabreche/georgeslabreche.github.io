---
title: "OPS-SAT-1 Publications in 2025"
excerpt: "A look at this year's publications: from day-to-day operations to final reentry."
categories:
  - opssat
tags:
  - opssat
  - research
  - publication
  - operations
---

Despite the OPS-SAT-1 mission coming to an end in May 2024, we still had some publications this year. Two were peer-reviewed for AeroConf 2025 in Big Sky, Montana, and the third was presented at SpaceOps 2025 in Montreal, Canada. These publications form a nice series detailing how the mission operationally unfolded to how we handled its final orbits and reentry.

### Innovating ground software systems – a retrospective of OPS-SAT-1 mission

> D. Marszk, D. Fischer, N. R. Carvalho, T. Oerther, M. Henkel, G. Labrèche, "Innovating ground software systems – a retrospective of OPS-SAT-1 mission," The 18th International Conference on Space Operations (SpaceOps 2025), Montreal, Canada, 2025, ([7 — Ground Systems Engineering (GSE) — Paper ID 281](https://star.spaceops.org/2025/paper_lists.php))

- Describes OPS-SAT-1 as a software-defined, multi-tenant "space lab" exposed safely to external experimenters.
- Explains the layered experimenter interfaces (direct packets, CCSDS MO services, higher-level tools) and the virtualized, containerized ground stack.
- Presents ground-segment lessons learned that now feed into successor missions like OPS-SAT VOLT and ORIOLE.

<div style="text-align:center;">
  <table align="center">
    <tr>
      <td>
        <img src="/assets/images/posts/2025-11-06/esa-opssat-nmf-interactions.svg"
             alt="Overview of the OPS-SAT-1 live experimenter interfaces."
             width="640" />
      </td>
    </tr>
    <tr style="text-align:left;">
      <td>
        <figcaption>Overview of the OPS-SAT-1 live experimenter interfaces.</figcaption>
      </td>
    </tr>
  </table>
</div>


### Operational Challenges and Achievements of the OPS-SAT-1 Mission

> D. Evans, V. Zelenevskiy, G. Labrèche, T. Oerther, N. R. Carvalho, G. Honorè, F. Dall'Omo, D. Marszk, "Operational Challenges and Achievements of the OPS-SAT-1 Mission," _2025 IEEE Aerospace Conference_, Big Sky, MT, USA, 2025, doi: [10.1109/AERO63441.2025.11068410](https://doi.org/10.1109/AERO63441.2025.11068410).

- Summarizes the mission's achievements across 285 experiments serving 134 teams from 19 different countries.
- Walks through key problem areas (ADCS, I²C, configuration, automation, testing) using real anomalies and recoveries.
- Presents five high-level operational lessons for future "open" experimental smallsat missions.

<div style="text-align:center;">
  <table align="center">
    <tr>
      <td>
        <img src="/assets/images/posts/2025-11-06/esa-opssat-obsw-release-per-month.svg"
             alt=" OBSW releases per month and cumulative releases. Release months taken from the GitLab release tags."
             width="640" />
      </td>
    </tr>
    <tr style="text-align:left;">
      <td>
        <figcaption> OBSW releases per month and cumulative releases. Release months taken from the GitLab release tags.</figcaption>
      </td>
    </tr>
  </table>
</div>


### OPS-SAT-1's Final Orbits and Reentry Analysis Amid Mission Extension Attempts

> F. Dall'Omo, G. Labrèche, T. Oerther, N. R. Carvalho, G. Honorè, D. Marszk, V. Zelenevskiy, D. Evans, "OPS-SAT-1's Final Orbits and Reentry Analysis Amid Mission Extension Attempts," _2025 IEEE Aerospace Conference_, Big Sky, MT, USA, 2025, doi: [10.1109/AERO63441.2025.11068646](https://doi.org/10.1109/AERO63441.2025.11068646).

- Analyzes how the Horizontal Pointing (HoPo) drag-reduction mode and ADCS anomalies shaped the final reentry profile.
- Shows how UHF plus a SatNOGS amateur radio campaign kept telemetry flowing up to reentry.
- Captures the last weeks of operations and offers end-of-life best practices for future smallsat missions.


<div style="text-align:center;">
  <table align="center">
    <tr>
      <td>
        <img src="/assets/images/posts/2025-11-06/esa-opssat-reentry.png"
             alt="Orbital parameters of OPS-SAT-1 from January 1, 2024 to May 22, 2024, showing the altitude, altitude change per day, and BSTAR"
             width="640" />
      </td>
    </tr>
    <tr style="text-align:left;">
      <td>
        <figcaption>Orbital parameters of OPS-SAT-1 from January 1, 2024 to May 22, 2024, showing the altitude (blue), altitude change per day (orange), and BSTAR (green).</figcaption>
      </td>
    </tr>
  </table>
</div>

