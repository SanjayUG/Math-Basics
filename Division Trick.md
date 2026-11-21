## ⚡ Fast Division Approximation Cheat Sheet

### Key Rules (At a Glance)
* **Core Setup:** Take the **first 2 digits** of the numerator and the **first 1 rounded digit** of the denominator.
* **Denominator Rounding:** Check the 2nd digit of the denominator—if it is **`5–9`**, round the 1st digit **UP** (`856 → 9`); if it is **`0–4`**, keep it **AS IS** (`638 → 6`).
* **`100s / 200s` Exception:** If the denominator starts with **`1` or `2`** (`178`, `248`), keep **2 digits** (`18`, `25`) to avoid large errors.
* **Zero & Decimal Shift (`Top Ignored − Bottom Ignored`):**
  * **Larger ÷ Smaller (`5-digit ÷ 3-digit`):** `3 − 2 = +1` → **Multiply by `10`** (add 1 zero).
  * **Smaller ÷ Larger (`3-digit ÷ 5-digit`):** `1 − 4 = −3` → **Divide by `1,000`** (shift decimal 3 places left).
* **Direction Check:** Rounding the denominator **UP** gives a slight **underestimate** (true value is slightly higher); keeping it **AS IS** gives a slight **overestimate**.

---

### Messy Real-World Examples

| Case                  | Messy Fraction       | How You Simplify | Estimate     | Exact Answer | Error %  | Why It Works                                       |
| :-------------------- | :------------------: | :--------------: | :----------: | :----------: | :------: | :------------------------------------------------- |
| **5-digit ÷ 3-digit** | **`74,859 / 867`**   | `74 / 9 × 10`    | **`82.2`**   | `86.34`      | **4.8%** | `867` rounds UP to `9` (`900`)                     |
| **5-digit ÷ 3-digit** | **`53,914 / 678`**   | `54 / 7 × 10`    | **`77.1`**   | `79.52`      | **3.0%** | `678` rounds UP to `7` (`700`)                     |
| **5-digit ÷ 3-digit** | **`63,418 / 856`**   | `63 / 9 × 10`    | **`70.0`**   | `74.09`      | **5.5%** | `856` rounds UP to `9` (`900`)                     |
| **5-digit ÷ 3-digit** | **`85,642 / 718`**   | `86 / 7 × 10`    | **`122.8`**  | `119.28`     | **3.0%** | `85,642` taken as `86`; `718` stays `7` (`700`)    |
| **3-digit ÷ 5-digit** | **`648 / 78,943`**   | `64 / 8 ÷ 1,000` | **`0.0080`** | `0.00821`    | **2.5%** | `78,943` rounds UP to `8` (`80,000`)               |
| **3-digit ÷ 5-digit** | **`487 / 63,819`**   | `48 / 6 ÷ 1,000` | **`0.0080`** | `0.00763`    | **4.8%** | `63,819` stays `6` (`60,000`)                      |
| **3-digit ÷ 5-digit** | **`542 / 85,639`**   | `54 / 9 ÷ 1,000` | **`0.0060`** | `0.00633`    | **5.2%** | `85,639` rounds UP to `9` (`90,000`)               |
| **3-digit ÷ 5-digit** | **`856 / 41,280`**   | `86 / 4 ÷ 1,000` | **`0.0215`** | `0.02074`    | **3.7%** | `856` taken as `86`; `41,280` stays `4` (`40,000`) |
