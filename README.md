**Classification des Styles Architecturaux par CNN**

📌 **Description du projet**

Ce projet consiste à développer un modèle de Deep Learning basé sur un _CNN (Convolutional Neural Network)_ capable de classifier des images selon leur style architectural.

Le modèle est entraîné sur un dataset d’images organisées par catégories architecturales, puis testé sur plusieurs images afin d’évaluer ses performances.


🧠** Objectif**
L’objectif principal est de :

Construire un modèle CNN pour la classification d’images
Appliquer les techniques de prétraitement des images
Diviser le dataset en entraînement et validation
Évaluer la performance du modèle
Tester le modèle sur de nouvelles images

📂** Dataset**
Le dataset est fourni sous forme d’un fichier .zip contenant plusieurs dossiers :

Dataset/
│
├── Gothic/
├── Moorish/
├── Russian/
├── Amazigh/
├── Buddhist/
├── Egyptian/
├── ...

Chaque dossier représente une classe architecturale.

Le dataset est divisé automatiquement en :

**80%** → Training set
**20%** → Validation set

Grâce à la bibliothèque split-folders.

⚙️** Technologies utilisées**
Python
TensorFlow / Keras
NumPy
Matplotlib
split-folders
Google Colab
🧱 Architecture du Modèle CNN

Le modèle Sequential contient :

🔹 Conv2D (32 filtres)
🔹 MaxPooling
🔹 Conv2D (64 filtres)
🔹 MaxPooling
🔹 Conv2D (128 filtres)
🔹 MaxPooling
🔹 Flatten
🔹 Dense (256 neurones)
🔹 Dropout (0.5)
🔹 Dense (Softmax – classification multi-classe)

Taille des images :
224 x 224 x 3

Batch size :
32

Nombre d’epochs :
50

📊** Analyse des données**

Une visualisation est réalisée pour analyser la répartition des images par classe dans le dataset d’entraînement.

Cela permet de vérifier l’équilibre entre les différentes catégories architecturales.

🚀 Entraînement du modèle

Le modèle est entraîné avec :

model.fit(
    train_gen,
    validation_data=val_gen,
  _ ** epochs=50**_
)

Les métriques suivies :

Accuracy
Loss
Validation Accuracy
Validation Loss

Des graphiques sont générés pour analyser :

L’évolution de la précision
L’évolution de la perte

💾 Sauvegarde du modèle
Le modèle entraîné est sauvegardé au format :

mydata.h5
🖼️ Tests du modèle

Le modèle est testé sur plusieurs images :

_**Russian architecture
Moorish architecture
Amazigh architecture
Gothic architecture
Buddhist architecture
Egyptian architecture**_

Chaque image est :
Redimensionnée en 224x224
Normalisée
Prédite par le modèle
Affichée avec la classe prédite

📈** Résultats**

Le modèle obtient des résultats satisfaisants sur les images de test.

Les performances peuvent être améliorées par :

Data augmentation
Transfer Learning (VGG16, ResNet…)
Augmentation du dataset
Fine-tuning

 Améliorations futures
Utilisation du Transfer Learning
Optimisation des hyperparamètres
Déploiement sous forme d’application web
Création d’une interface utilisateur

** Conclusion**
Ce projet démontre l’efficacité des réseaux de neurones convolutifs pour la classification d’images architecturales.

Il constitue une base solide pour des projets plus avancés en vision par ordinateur et Deep Learning.
