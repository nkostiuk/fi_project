# French Industry Project
## Contexte

L'INSEE est l'institut officiel français qui collecte des données de tous types sur le territoire français. Elles peuvent être démographiques (Naissances, Décès, Densité de la population...), économiques (Salaires, Entreprises par activité / taille...) et plus encore.

Ces données peuvent être d'une grande aide pour observer et mesurer les inégalités au sein de la population française.

## Objectif 
Comparer les inégalités en France : 
- Entreprises en fonction de leur localisation, de leur taille. 
- Population en fonction du salaire et de la localisation.
- Focus sur une grande ville 

## Source de données  
Données : INSEE ([insee.fr/fr/statistiques](https://www.insee.fr/fr/statistiques))

## Description des tables 

- **base_etablissement_par_tranche_effectif.csv** : Informations sur le nombre d'entreprises dans chaque ville française classées par taille.
   - CODGEO : ID géographique de la ville
   - LIBGEO : nom de la ville
   - REG : numéro de région
   - DEP : numéro de département
   - E14TST : nombre total d'entreprises dans la ville
   - E14TS0ND : nombre d'entreprises de taille inconnue ou nulle dans la ville
   - E14TS1 : nombre d'entreprises de 1 à 5 employés dans la ville
   - E14TS6 : nombre d'entreprises de 6 à 9 employés dans la ville
   - E14TS10 : nombre d'entreprises de 10 à 19 employés dans la ville
   - E14TS20 : nombre d'entreprises de 20 à 49 employés dans la ville
   - E14TS50 : nombre d'entreprises de 50 à 99 employés dans la ville
   - E14TS100 :  nombre d'entreprises de 100 à 199 employés dans la ville
   - E14TS200 : nombre d'entreprises de 200 à 499 employés dans la ville
   - E14TS500 : nombre d'entreprises de plus de 500 employés dans la ville

- **entreprises24.csv** : Informations sur le nombre d'entreprises dans chaque ville française classées par taille (Nouvelles données).
   - CODGEO : ID géographique de la ville
   - ET_BE : etablissements actifs de l'industrie au 31/12/2021 
   - ET_BE_0sal : etablissements actifs de l'industrie sans salarié au 31/12/2021
   - ET_BE_1_4 : etablissements actifs de l'industrie de 1 à 4 salariés au 31/12/2021
   - ET_BE_5_9 : etablissements actifs de l'industrie de 5 à 9 salariés au 31/12/2021
   - ET_BE_10_19 : etablissements actifs de l'industrie de 10 à 19 salariés au 31/12/2021
   - ET_BE_20_49 : etablissements actifs de l'industrie de 20 à 49 salariés au 31/12/2021
   - ET_BE_50_99 : etablissements actifs de l'industrie de 50 à 99 salariés au 31/12/2021
   - ET_BE_100_199 : etablissements actifs de l'industrie de 100 à 199 salariés au 31/12/2021
   - ET_BE_200_499 : etablissements actifs de l'industrie de 200 à 499 salariés au 31/12/2021
   - ET_BE_500P : etablissements actifs de l'industrie de 500 salariés ou plus au 31/12/2021

- **name_geographic_information.csv** : Données géographiques sur les villes françaises (principalement la latitude et la longitude, mais aussi les codes et les noms des régions/départements). 

- **net_salary_per_town_categories.csv** : Salaires par villes française par catégories d'emploi, âge et sexe
    - CODGEO : ID géographique de la ville - enlever 0 au début 
    - LIBGEO : nom de la ville
    - SNHM20 : salaire net moyen  par heure 
    - SNHMC20 : salaire net moyen par heure pour les cadres
    - SNHMP20 : salaire net moyen par heure pour un cadre moyen
    - SNHME20 : salaire net moyen par heure pour l'employé
    - SNHMO20 :  salaire net moyen par heure pour le travailleur
    - SNHMF20 : salaire net moyen pour les femmes
    - SNHMFC20 : salaire net moyen par heure pour les cadres féminins
    - SNHMFP20 : salaire net moyen par heure pour les cadres moyens féminins
    - SNHMFE20 : salaire net moyen par heure pour une employée 
    - SNHMFO20 : salaire net moyen par heure pour une travailleuse 
    - SNHMH20 : salaire net moyen pour un homme
    - SNHMHC20 : salaire net moyen par heure pour un cadre masculin
    - SNHMHP20 : salaire net moyen par heure pour les cadres moyens masculins
    - SNHMHE20 : salaire net moyen par heure pour un employé masculin
    - SNHMHO20 : salaire net moyen par heure pour un travailleur masculin
    - SNHM1820 : salaire net moyen par heure pour les 18-25 ans
    - SNHM2620 : salaire net moyen par heure pour les 26-50 ans
    - SNHM5020 : salaire net moyen par heure pour les >50 ans
    - SNHMF1820 : salaire net moyen par heure pour les femmes âgées de 18 à 25 ans
    - SNHMF2620 : salaire net moyen par heure pour les femmes âgées de 26 à 50 ans
    - SNHMF5020 : salaire net moyen par heure pour les femmes de plus de 50 ans
    - SNHMH1820 : salaire net moyen par heure pour les hommes âgés de 18 à 25 ans
    - SNHMH2620 : salaire net moyen par heure pour les hommes âgés de 26 à 50 ans
    - SNHMH5020 : salaire net moyen par heure pour les hommes de plus de 50 ans
      
- **population.csv** : Informations démographiques par ville, âge, sexe et mode de vie
    - NIVGEO : geographic level (arrondissement, communes…)
    - CODGEO : ID géographique de la ville
    - LIBGEO : name of the town
    - MOCO : mode de cohabitation :
        - 11 = enfants vivant avec deux parents
        - 12 = enfants vivant avec un seul parent
        - 21 = adultes vivant en couple sans enfant
        - 22 = adultes vivant en couple avec enfants
        - 23 = adultes vivant seuls avec enfants
        - 31 = personnes étrangères à la famille vivant au foyer
        - 32 = personnes vivant seules
    - AGE80_17 : catégorie d'âge (tranche de 5 ans) | ex : 0 -> personnes âgées de 0 à 4 ans, 5 -> de 5 à 9 ans
    - SEXE : sexe, 1 pour homme | 2 pour femme
    - NB : Nombre de personnes dans la catégorie

- **diplomes_2020_new.csv** : Informations sur le nombre de personnes sans diplôme, ou titulaires d'un CEP, ou d'un diplôme de niveau BAC+5 ou plus.
    - CODGEO : ID géographique de la ville
    - P20_HNSCOL15P_DIPLMIN	: Nombre de hommes non scolarisées de 15 ans ou plus titulaires d'aucun diplôme ou au plus un CEP en 2020
    - P20_HNSCOL15P_SUP5 : Nombre de hommes non scolarisées de 15 ans ou plus titulaires d'un diplôme de l'enseignement supérieur de niveau Bac + 5 ou plus en 2020
    - P20_FNSCOL15P_DIPLMIN	: Nombre de femmes non scolarisées de 15 ans ou plus titulaires d'aucun diplôme ou au plus un CEP en 2020
    - P20_FNSCOL15P_SUP5 : Nombre de femmes non scolarisées de 15 ans ou plus titulaires d'un diplôme de l'enseignement supérieur de niveau Bac + 5 ou plus en 2020
 

