## Paper Revision Notes

We thank all reviewers for their comments. We uploaded a revised PDF, with changes marked in blue.

## Summary
* **Schedule -> Pipeline:** the method is described as a periodic pipeline
* **T_sus Experiment:** Section 6.3 adds the sustained period experiemnt, to evaluate long-term execution improvement.
* **Success rate:** Section 6 now reports deployment precision (Q4) instead of 16-bit.
* **Mobile control validation:** in Appendix C, the phone computes every action chunk that controls the robot in the LIBERO environment.
* **Implementation details:** the appendix adds pseudocode, profiling details and extensive experiments.


## Detailed Content

<details>
<summary><b>Reviewer ekKW</b></summary>

- **W1 / Q1 (periodic vs. NPU-only in closed loop):** Table 1 adds NPU-only at $\Delta=5$ next to VLA-Duo at $\Delta=10$, both at deployment precision.
- **Q1 (inpainting on $\pi_0$ and $\pi_{0.5}$):** Appendix B.2 explains the $\pi_0$ drop, which comes from the action output projection. Table 5 adds the deployment precision.
- **W2 / Q2 (eager admission, fixed-period replay, overruns):** Section 3.3 states the overrun policy. Section 6.3 reports $T_{sus}$, latency and power. Appendix H lists each sustained run and explains the two admission modes.
- **Differences from our reply:** the reference in our reply (88.0) was single-seed, and the revision uses the three-seed mean 87.7.

</details>

<details>
<summary><b>Reviewer zeUa</b></summary>

- **W1 (real robot):** Appendix C adds a phone-in-the-loop evaluation on Snapdragon 8 Elite.
- **W2 (atom definition):** Appendix E gives the atom template and the atom counts.
- **W3 ("scheduler"):** the method is described as a periodic pipeline. (except title)
- **Q1 / Q2 (other models and VLA families):** Appendix I reports SmolVLM2 and OpenVLA.
- **Q3 (CPU):** answered in our reply, but didn't add to the paper.
- **Q4 (single cut):** Appendix D gives the DP algorithm and experiments for exactly $k$ cuts, $k\in [1,10)$
- **Q5 (cut location):** Section 6.4 gives the location of the selected cuts, next to Figure 6.

</details>

<details>
<summary><b>Reviewer rfmz</b></summary>

- **Q1 (sustained execution and timing):** Section 3.3 states the overrun policy. Section 6.3 reports $T_{sus}$, latency and power. Appendix H lists each sustained run.
- **Q2 (closed loop with measured timing):** Table 1 adds NPU-only at $\Delta=5$ next to VLA-Duo at $\Delta=10$, both at deployment precision.
- **Q3 ($\pi_0$ at deployment precision):** Appendix B.2 explains the $\pi_0$ drop, which comes from the action output projection. Table 5 adds the deployment precision with three-seed means.
- **Q4 (prefix inpainting):** Appendix G gives the update rule and its relation to RTC Appendix A.4.
- **Q5 (profiling cost):** Appendix F gives the profiling method, its cost and the time quantum $\tau$.
- **Differences from our reply:** the reference in our reply (88.0) was single-seed, and the revision uses the three-seed mean 87.7. Our reply pointed to Section 3.2 for $\tau$, which is now in Appendix F.

</details>

<details>
<summary><b>Reviewer BGAT</b></summary>

- **W1 / Q1 (sustained measurements):** Section 6.3 reports $T_{sus}$, core temperature and power. Appendix H lists each sustained run, with no overrun.
- **W2 / Q2 (measured timing in the closed loop):** Table 1 adds NPU-only at $\Delta=5$ next to VLA-Duo at $\Delta=10$, both at deployment precision.
- **Q2 ($\pi_0$ in Table 5, uncertainty):** Appendix B.2 explains the $\pi_0$ drop, which comes from the action output projection. Table 5 adds the deployment precision with three-seed means.
- **Differences from our reply:** the reference in our reply (88.0) was single-seed, and the revision uses the three-seed mean 87.7.

</details>
