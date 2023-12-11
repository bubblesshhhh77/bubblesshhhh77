- 👋 Hi, I’m @bubblesshhhh77
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
bubblesshhhh77/bubblesshhhh77 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import odeint

# Definisi persamaan diferensial
def model(y, t):
    return [y[1], 4 * y[1] - 3 * y[0]]

# Syarat awal
y0 = [0, 1]

# Waktu
t = np.linspace(0, 5, 100)

# Solusi numerik
y = odeint(model, y0, t)

# Plot hasil
plt.figure(figsize=(10, 6))
plt.plot(t, y[:, 0], label='y(t)')
plt.xlabel('t')
plt.ylabel('y(t)')
plt.legend()
plt.show()

