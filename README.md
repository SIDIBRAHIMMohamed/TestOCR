### Prétraitement des Images pour OCR

Cette section décrit les différentes étapes de prétraitement des images dans le cadre de notre système OCR (Reconnaissance Optique de Caractères).

## Étapes de Prétraitement

#Inversion de l'image : 

L'inversion correspond à un processus crucial visant à améliorer la qualité de l'image.

#Binarisation : 

La binarisation consiste à convertir l'image en noir et blanc en fonction d'un seuil prédéfini. Cela simplifie le processus de reconnaissance des caractères.

#Suppression du bruit :
 Le bruit dans une image peut perturber le processus de reconnaissance des caractères. Cette étape vise à éliminer le bruit indésirable de l'image, ce qui rend le texte plus clair et plus facile à reconnaître.

#Méthodologie
J'ai utilisé la bibliothèque OpenCV pour effectuer les opérations de prétraitement. Voici un aperçu des étapes impliquées :

1. Ouverture de l'image : J'ai chargé l'image à traiter à l'aide de la bibliothèque OpenCV.

2. Inversion de l'image : J'ai utilisé la fonction cv2.bitwise_not() pour inverser l'image.

3. Binarisation : J'ai converti l'image en niveaux de gris à l'aide de la fonction cv2.cvtColor(), puis j'ai appliqué la binarisation en utilisant la fonction cv2.threshold().

4. Suppression du bruit : J'ai appliqué une série de transformations morphologiques telles que la dilatation, l'érosion et le flou médian pour éliminer le bruit de l'image.

#Exécution
Pour exécuter le prétraitement des images, vous pouvez exécuter le script Pretraitement.py inclus dans le répertoire du projet. Assurez-vous d'avoir installé toutes les dépendances requises répertoriées dans le fichier requirements.txt( pip install -r requirements.txt)


#Apres avoir executer le fichier Prétraitement  pour passer donc a l'execution de l'OCR.

#Implémentation de l'OCR

Le script utilise l'outil Tesseract pour extraire les données textuelles de l'image prétraitée. Il extrait les informations sur le texte, y compris la position et la confiance associées à chaque mot, en utilisant un taux de confiance supérieur à 85%.
 
1. Placez votre image dans le répertoire data.
2. Exécutez le script ocr_extraction.py.
3. Les informations extraites seront enregistrées dans le fichier infos_texte.json.


