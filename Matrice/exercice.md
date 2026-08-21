## Exercice : notes d’élèves et PCA

On étudie les résultats d’un groupe d’élèves dans trois matières :

$$
X_1=\text{Mathématiques}
$$

$$
X_2=\text{Programmation}
$$

$$
X_3=\text{Réseaux}
$$

Après centrage des données, on obtient la matrice de covariance suivante :

$$
C=
\begin{pmatrix}
4 & 2 & 0\\
2 & 4 & 0\\
0 & 0 & 1
\end{pmatrix}
$$

### Questions

1. Que représentent les éléments diagonaux de cette matrice ?

2. Que signifie la valeur :

$$
C_{1,2}=2
$$

dans le contexte des notes de maths et de programmation ?

3. Utiliser NumPy pour calculer les **valeurs propres** et les **vecteurs propres** de la matrice.

Pour une matrice de covariance, utiliser :

```python
np.linalg.eigh()
```

Code de départ :

```python
import numpy as np

C = np.array([
    [4, 2, 0],
    [2, 4, 0],
    [0, 0, 1]
])

# À compléter
```

4. Identifier la plus grande valeur propre.

5. Récupérer le vecteur propre associé.

6. Interpréter les trois coordonnées de ce vecteur propre par rapport à :

$$
(\text{Maths},\text{Programmation},\text{Réseaux})
$$

7. Calculer la variance totale :

$$
\lambda_1+\lambda_2+\lambda_3
$$

8. Calculer le pourcentage de variance expliqué par chaque valeur propre :

$$
\boxed{
\text{variance expliquée}
\frac{\lambda_i}
{\lambda_1+\lambda_2+\lambda_3}
\times100
}
$$

9. Quelle composante principale semble la plus importante ?

10. Peut-on réduire les trois matières à seulement une ou deux composantes principales sans perdre trop d’information ? Justifier avec les pourcentages obtenus.
