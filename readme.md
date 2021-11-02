# Exercices sur le Langage de Manipulation des Données

Pour réaliser les exercices de ce laboratoire, relire la théorie concernant le LMD, ainsi que le résumé donné dans le
cahier de laboratoire de la page 65 à la page 72. Créer également la base de donnée Hopital complète avec les scripts
fournis.

Créer également la base de donnée `Hopital` complète avec les scripts fournis dans le centre de
ressources ([CreationHopital.sql](./Hopital/CreationHopital.sql) et [0-InsertAll.sql](./Hopital/InsertionDesDonnees/0-InsertAll.sql)).

## LMD 1

Afficher, triés par âge, le numéro de SIS, le libellé de la mutuelle et l'âge de tous les patients du
médecin `Collignon` habitant à `Tenneville`. Attention, le code `mutuelle` n'est pas toujours précisé dans la table
Patients. Pour ces patients-là, on affichera, au lieu du libellé de la mutuelle, `Pas de mutuelle`. Résoudre au moyen de
requêtes ensemblistes ainsi qu'au moyen de jointures.

```sql
-- Requête ensembliste :

-- Requête avec jointure :
```

Résultats :

| NRSIS | NOM | MUTUELLE | AGE |
| :--- | :--- | :--- | :--- |
| 86012200206 | MATITA | Pas de Mutuelle | 35 |
| 86030800127 | BELANGE | Pas de Mutuelle | 35 |
| 84092300166 | CLOSE | Caisse des Soins de sante de la SNCB Centre Medical Regional | 37 |
| 84011100621 | COLLURA | Pas de Mutuelle | 37 |
| 83042600572 | COSENTINO | Pas de Mutuelle | 38 |
| 75092100025 | JIANG | Office regional de Namur | 46 |
| 74080100511 | VOROBIEVA | Office regional de Namur | 47 |
| 73081800412 | SANGWA MAYANI | Office regional de Namur | 48 |
| 70120200144 | OUAFIQ | Office regional de Namur | 51 |

## LMD 2

Afficher, triés par `nom`, le `nom` et le `prénom` des patients `célibataires` de `Saint-Nicolas`, de moins de `39` ans
et qui n'ont pas de médecins. À résoudre par requêtes ensemblistes, imbriquées, corrélées et au moyen de jointures.

```sql
-- Requête ensembliste :

-- Si on ne veut afficher que nom et prénom, mais continuer à traiter les homonymes, on aura la solution suivante : 

-- Requêtes imbriquées :

-- Requêtes corrélées :

-- Requête avec jointure :
```

Résultat en 2021 :

| NOM | PRENOM |
| :--- | :--- |
| AIT HMAD | Youcef |
| BELLEN | Antzo |
| BELLOMO | Nazaire |
| ZUCCHETTO | Eozenn |

## LMD3

Afficher, triés par nom, le nom et le prénom des patientes nées dans les années `1970` qui se font soigner par les
médecins `Geoffroy Munnix` et `Lala Kaison`. À résoudre par requêtes ensemblistes, imbriquées, corrélées et au moyen de
jointures.

```sql
-- Requête ensembliste :

-- Requêtes imbriquées :

-- Requêtes corrélées :
-- Requête avec jointure :
```

## LMD 4

Rechercher, triés par ordre alphabétique, le `nom` et le `prénom` de tous les médecins homme, `célibataires` qui ne sont
chef d'aucun service. À résoudre par requêtes ensemblistes, imbriquées, corrélées et au moyen de jointures.

```sql
-- Requête ensembliste :
-- Requêtes imbriquées :


-- Requêtes corrélées :

-- Requête avec jointure :
```

## LMD 5

Enregistrer la patiente `Lea Dupont` de nationalité `française`, domiciliée `Rue du centre` à `Yvoir`. Cette patient
est `célibataire`, elle est née le 14 juillet 1975 et est affiliée à la mutuelle `Office régional de Namur`. Cette
patiente est allergique à la substance `Codéine`. Elle se fait soigner par le médecin chef de service de
la `Neuropsychiatrie` de l'hôpital `Clinique Saint-Vincent`. Le `NrSis` est constitué de 11 caractères sous la
forme `YYMMDDXXXXX` `YYMMDD` sont l'année, le moi et le jour de la date de naissance du patien. `XXXXX` est le numéro de
SIS le plus élevé mémorisé dans la base plus UN.

````sql

Rollback;
````

Rem : On devrait faire un `commit`, mais on fait un rollback dans le cadre du labo afin de pouvoir refaire le test et de
ne pas modifier les données de la base.

## LMD 6

Le patient qui a le plus d'allergies vient de se marier. Il faut donc mettre son état civil à `M`. Il change de médecin(
s). Il se fait soigner par tous les médecins de plus de 55 ans domiciliés dans sa localité. Faire les modifications
nécessaires dans la base de données.

```sql
-- Pas besoin de patients dans requête imbriquée !!!


Rollback;
```

Rem : On devrait faire un `commit`, mais on fait un rollback dans le cadre du labo afin de pouvoir refaire le test et de
ne pas modifier les données de la base.

## LMD 7

Tous les patients de Welkenraedt nés en 1982 qui n'avaient pas d'allergies sont allergiques à toutes les substances du
médicament Emcoretic. Faire les modifications nécessaires dans la base de données.

```sql

rollback; 
```

## LMD 8

Le médecin `Miquel Brasseur` prend sa retraire. Il cède tous ses patients au médecin de sa spécialité habitant sa
commune. On désire ne plus garder de trace de ce médecin.

```sql

Rollback;
```

