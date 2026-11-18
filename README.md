# Learning to Open a Door Faster in MetaWorld

Our STAT 546 project builds on the HW3 waypoint controller for `door-open-v3`. On 50 validation tasks, the controller opened the door every time, with a median of 124 steps to first success. We will investigate whether a robot can open the door earlier while maintaining reliability across tasks and training seeds. We will compare two approaches under the same reward function and 200-step episode limit.

## Team responsibilities

| Team member | Responsibilities | Deliverables |
| --- | --- | --- |
| Yan Xiyu | Lead the HW3 baseline and cross-entropy method (CEM) experiments. Compare the original training procedure, checkpoint selection on validation tasks, and independent restarts under a fixed interaction budget. | Nine trained policies across three variants and three seeds, learning curves, and a comparison of return, opening speed, and training cost. |
| Junhyung Ahn | Lead the soft actor-critic (SAC) experiments. Compare learning actions directly with learning corrections to the frozen HW3 controller. Analyze when the corrections help and how much additional training they require. | Direct and residual SAC models, validation curves, a training-cost comparison, and a side-by-side rollout video. |
| Yasong Qin | Prepare and deliver the two-minute introduction using a baseline table supplied by Yan and a rollout image supplied by Junhyung. | Two opening slides. The first introduces the door-opening task. The second uses the HW3 results to explain why opening speed matters. |

## Evaluation

Yan and Junhyung will freeze their policies before evaluating them on the same 200 held-out tasks. They will jointly report mean cumulative return, success rate, the fraction of episodes that succeed by step 150, and variability across training seeds. Each will present the results for their own method.
