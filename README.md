from sklearn.cluster import KMeans
import matplotlib.pyplot as plt

# Dados fictícios
notas_matematica = [70, 80, 90, 60, 85, 75, 95, 65, 55, 50]
notas_ciencias = [60, 70, 80, 50, 75, 65, 85, 55, 45, 40]

# Agrupamento
X = list(zip(notas_matematica, notas_ciencias))
kmeans = KMeans(n_clusters=2)
kmeans.fit(X)

# Visualização
plt.scatter(notas_matematica, notas_ciencias, c=kmeans.labels_)
plt.title("Agrupamento de Alunos")
plt.xlabel("Matemática")
plt.ylabel("Ciências")
plt.show()
