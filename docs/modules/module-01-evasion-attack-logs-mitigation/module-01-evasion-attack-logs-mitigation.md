# Module 1 – Evasion Attack: Logs + Mitigation

**ATLAS Reference:** AML.T0043.001 (White-box Evasion)

## 1. Scenario

A simple CNN classifier trained on MNIST achieves 99% accuracy. An attacker with model access uses FGSM (Fast Gradient Sign Method) to craft adversarial inputs that cause misclassification.

**Threat Model:** White-box (attacker has full model access)

## 2. Baseline

- Model: 2-layer CNN, 421K parameters
- Training: 3 epochs, Adam optimizer
- Test Accuracy: 99.04%
- Mean Confidence: 0.99

## 3. Attack

**FGSM Attack Results:**

| Epsilon | Accuracy | Confidence |
|---------|----------|------------|
| 0.00    | 99.0%    | 0.99       |
| 0.05    | 96.3%    | 0.97       |
| 0.10    | 88.5%    | 0.92       |
| 0.15    | 70.2%    | 0.85       |
| 0.20    | 44.1%    | 0.79       |
| 0.30    | 7.5%     | 0.78       |

Key insight: Small perturbations (ε=0.15) invisible to humans drop accuracy by 30%.

## 4. Observability

**Detection Signals:**
- Confidence drop: 0.99 → 0.85 (14% decrease)
- Std deviation: 0.05 → 0.16 (3x increase)
- Distribution shift visible in histograms

**Monitoring hooks:**
- Alert on mean confidence < 0.90
- Alert on confidence std > 0.10
- Track prediction entropy over time

## 5. Mitigation

**Adversarial Training (1 epoch):**

| Epsilon | Original | Robust  |
|---------|----------|---------|
| 0.00    | 99.0%    | 98.1%   |
| 0.15    | 70.2%    | 90.8%   |
| 0.30    | 7.5%     | 57.7%   |

Trade-off: Slight clean accuracy drop for significant adversarial robustness.

## 6. Lessons Learned

1. Neural nets are vulnerable to small, targeted perturbations
2. Confidence metrics provide detection signals before accuracy drops
3. Adversarial training is effective but requires attack knowledge
4. White-box attacks assume worst-case scenario

## Hands-On

→ [Run the notebook](https://github.com/mlsecops-labs/modules/tree/main/module-01-evasion-logs-mitigation)