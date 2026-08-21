Prenons uniquement deux critères pour plusieurs étudiants :

* (x) = note en **mathématiques**
* (y) = note en **programmation**

Imaginons que les étudiants forts en maths soient souvent aussi forts en programmation. Les deux notes sont donc liées.

On calcule la matrice de covariance et on obtient :

$$
C=
\begin{pmatrix}
2&1\\
1&2
\end{pmatrix}
$$

Cette matrice possède deux valeurs propres :

$$
\boxed{\lambda_1=3}
\qquad
\boxed{\lambda_2=1}
$$

et deux directions propres.

### 1. Première direction : maths et programmation ensemble

Le vecteur propre associé à (3) est :

$$
v_1=
\begin{pmatrix}
1\\
1
\end{pmatrix}
$$

Cela signifie qu'on regarde les deux critères **dans le même sens** :

$$
\text{Maths}+\text{Programmation}
$$

On peut interpréter cela comme :

$$
\boxed{\text{niveau général en informatique/sciences}}
$$

Par exemple :

| Étudiant | Maths | Programmation |
| -------- | ----: | ------------: |
| Alice    |    18 |            17 |
| Bob      |    14 |            15 |
| Charlie  |     8 |             9 |

La principale différence entre ces étudiants est assez évidente : certains sont globalement forts dans **les deux matières**, d'autres plus faibles dans les deux.

C'est cette direction que représente :

$$
\begin{pmatrix}1\\1\end{pmatrix}
$$

Et elle possède la plus grande valeur propre :

$$
\boxed{\lambda=3}
$$

Donc c'est la direction la plus importante.

---

### 2. Deuxième direction : maths contre programmation

Le deuxième vecteur propre est :

$$
v_2=
\begin{pmatrix}
1\\
-1
\end{pmatrix}
$$

Cette fois on regarde :

$$
\text{Maths}-\text{Programmation}
$$

Cela mesure plutôt la différence entre les deux compétences.

Par exemple :

| Étudiant | Maths | Programmation |
| -------- | ----: | ------------: |
| David    |    18 |            10 |
| Emma     |    10 |            18 |

David est plutôt orienté maths, alors qu'Emma est plutôt orientée programmation.

Cette différence existe, mais dans notre exemple elle est moins importante que le niveau général.

Sa valeur propre est :

$$
\boxed{\lambda=1}
$$

---

### 3. Pourquoi (3) est plus important que (1) ?

La variance totale vaut :

$$
3+1=4
$$

La première direction représente :

$$
\frac{3}{4}=75%
$$

La deuxième :

$$
\frac{1}{4}=25%
$$

Donc :

$$
\boxed{75}\%
$$

des différences entre les étudiants peuvent être expliquées par :

> « Est-ce que l'étudiant est globalement bon ou moins bon en maths et programmation ? »

Et seulement :

$$
\boxed{25}\%
$$

par :

> « Est-il plutôt maths ou plutôt programmation ? »

### À retenir

Les **vecteurs propres fabriquent de nouveaux axes** :

$$
\boxed{
\begin{pmatrix}1\\1\end{pmatrix}
\rightarrow
\text{Maths + Programmation}
}
$$

$$
\boxed{
\begin{pmatrix}1\\-1\end{pmatrix}
\rightarrow
\text{Maths - Programmation}
}
$$

Et les **valeurs propres indiquent l'importance de ces axes** :

$$
\boxed{3 \rightarrow 75}\%
$$

$$
\boxed{1 \rightarrow 25}\%
$$

C'est exactement l'idée de base de la PCA : **trouver les directions qui résument le mieux les données**.





Ici, **Maths − Programmation** ne veut pas dire qu’on “soustrait des matières” au sens concret. C’est un **score qui mesure l’écart entre les deux compétences**.

Par exemple, si on prend simplement :

$$
\text{score}=\text{Maths}-\text{Programmation}
$$

Alors :

* Maths = 16, Programmation = 10

$$
16-10=6
$$

Le score est positif : profil plutôt **maths**.

* Maths = 10, Programmation = 16

$$
10-16=-6
$$

Le score est négatif : profil plutôt **programmation**.

* Maths = 14, Programmation = 14

$$
14-14=0
$$

Le score est nul : profil **équilibré**.

Donc, dans notre exemple de vecteur propre :

$$
v=
\begin{pmatrix}
1\\
-1
\end{pmatrix}
$$

on construit un nouvel axe qui oppose les deux variables :

$$
\boxed{\text{Maths} - \text{Programmation}}
$$

Cet axe ne mesure pas le niveau général. Il mesure surtout :

$$
\boxed{\text{dans quelle matière la personne est relativement meilleure}}
$$

À l’inverse,

$$
\begin{pmatrix}
1\\
1
\end{pmatrix}
$$

correspond plutôt à :

$$
\text{Maths}+\text{Programmation}
$$

donc au **niveau global dans les deux matières**.
