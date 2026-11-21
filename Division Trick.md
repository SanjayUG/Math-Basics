## ⚡ Fast Division Approximation

### 🎯 Key Rules
* **🔢 Setup:** Top = **first 2 digits** | Bottom = **first 1 rounded digit**
* **🔄 Round Bottom (2nd digit):** **`5–9`** ⬆️ round UP (`856 → 9`) | **`0–4`** ➡️ keep (`638 → 6`)
* **⚠️ `100s / 200s` Rule:** Starts with **`1` or `2`** → keep **2 digits** (`178 → 18`, `248 → 25`)
* **📍 Shift (`Top Ignored − Bottom Ignored`):**
  * $\dfrac{\text{5-digit}}{\text{3-digit}}$ : `3 − 2 = +1` ➡️ **`× 10`** (add 1 zero)
  * $\dfrac{\text{3-digit}}{\text{5-digit}}$ : `1 − 4 = −3` ➡️ **`÷ 1,000`** (3 decimals left)

---

### 📊 Examples

| Case                                      | Fraction               | Simplified                 | Estimate     | Exact     | Error    | Note                                |
| :---------------------------------------: | :--------------------: | :------------------------: | :----------: | :-------: | :------: | :---------------------------------- |
| $\dfrac{\text{5-digit}}{\text{3-digit}}$  | $\dfrac{74,859}{867}$  | $\dfrac{74}{9} \times 10$  | **`82.2`**   | `86.34`   | **4.8%** | `867 → 9` (`900`)                   |
| $\dfrac{\text{5-digit}}{\text{3-digit}}$  | $\dfrac{53,914}{678}$  | $\dfrac{54}{7} \times 10$  | **`77.1`**   | `79.52`   | **3.0%** | `678 → 7` (`700`)                   |
| $\dfrac{\text{5-digit}}{\text{3-digit}}$  | $\dfrac{63,418}{856}$  | $\dfrac{63}{9} \times 10$  | **`70.0`**   | `74.09`   | **5.5%** | `856 → 9` (`900`)                   |
| $\dfrac{\text{5-digit}}{\text{3-digit}}$  | $\dfrac{85,642}{718}$  | $\dfrac{86}{7} \times 10$  | **`122.8`**  | `119.28`  | **3.0%** | `85,642 → 86`; `718 → 7` (`700`)    |
| $\dfrac{\text{3-digit}}{\text{5-digit}}$  | $\dfrac{648}{78,943}$  | $\dfrac{64}{8} \div 1,000$ | **`0.0080`** | `0.00821` | **2.5%** | `78,943 → 8` (`80,000`)             |
| $\dfrac{\text{3-digit}}{\text{5-digit}}$  | $\dfrac{487}{63,819}$  | $\dfrac{48}{6} \div 1,000$ | **`0.0080`** | `0.00763` | **4.8%** | `63,819 → 6` (`60,000`)             |
| $\dfrac{\text{3-digit}}{\text{5-digit}}$  | $\dfrac{542}{85,639}$  | $\dfrac{54}{9} \div 1,000$ | **`0.0060`** | `0.00633` | **5.2%** | `85,639 → 9` (`90,000`)             |
| $\dfrac{\text{3-digit}}{\text{5-digit}}$  | $\dfrac{856}{41,280}$  | $\dfrac{86}{4} \div 1,000$ | **`0.0215`** | `0.02074` | **3.7%** | `856 → 86`; `41,280 → 4` (`40,000`) |
