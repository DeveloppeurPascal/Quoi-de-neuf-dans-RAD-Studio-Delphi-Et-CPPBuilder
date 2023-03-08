# Quoi de neuf dans RAD Studio 11.3 Alexandria ?

## Préalables
* rappels fonctionnement Twitch
https://www.twitch.tv/patrickpremartin
* rappel pour poser des questions depuis le tchat
* rappel pour poser des questions depuis le formulaire de contact depuis blog
https://developpeur-pascal.fr/nous-contacter.php

## Introduction
* contenu présentation
* qui suis-je ?
https://www.linkedin.com/in/patrickpremartin/
https://developpeur-pascal.fr
* mes liens
* liens utiles
* infos Barnsten
https://www.barnsten.com/fr/

## Embarcadero en 2022
* page web EMB
https://www.embarcadero.com
* Delphi (28 ans)
https://delphi.embarcadero.com
* C++Builder (25 ans)
https://25.cppbuilder.dev
* Interbase 2020 update 4
https://www.embarcadero.com/products/interbase

## RAD Studio 11.3 Alexandria
* annonce de sortie par Marco Cantu
https://blogs.embarcadero.com/announcing-the-availability-of-rad-studio-11-3-alexandria/
* contenu de cette version
https://docwiki.embarcadero.com/RADStudio/Alexandria/en/11_Alexandria_-_Release_3
* plateformes prises en charge
https://docwiki.embarcadero.com/PlatformStatus/en/Main_Page
* tickets publics clôturés
https://quality.embarcadero.com/secure/Dashboard.jspa?selectPageId=13100
* liste des tickets de la version
https://docwiki.embarcadero.com/RADStudio/Alexandria/en/New_features_and_customer_reported_issues_fixed_in_RAD_Studio_11.3
* rediffusion de la présentation officielle proposée par Embarcadero
https://youtu.be/x-STTV2tRMA
* session spéciale de Q&A le jeui 9 mars à 17 heures
https://register.gotowebinar.com/register/4280764234281569631?source=Twitch

## IDE
* nouvelles améliorations sur la prise en charge des écrans à haute résolution
* optimisations dans certains écrans (notamment des listes passant maintenant par TControlList)
* indique en barre de titre si on l'a ouvert en "administrateur"
* création et modification de fichiers Markdown (en code source mais avec prévisualisation possible)
* DEMO : création d'un fichier Markdown vierge, copie de ce document dedans
* mise en surbrillance des mots sélectionnés dans un code source
* DEMO : ouverture d'un projet, parcourt du code source, double clic sur un mot, options d'environnement pour montrer où le changer
* DLL de subversion plus fournie => charge aux développeurs d'utiliser la version qu'ils veulent et la maintenir comme pour Git et Mercurial
* DEMO : afficher l'écran de bienvenue post installation de l'IDE et montrer les options de paramétrage
* DEMO : chemin vers les options de l'IDE pour modifier ce paramètre
* accès aux dossiers de compilation d'un projet
* DEMO : ouverture d'un projet FMX avec plusieurs plateformes compilées et utilisation du menu contextuel sur le gestionnaire de projets pour accéder aux dossiers disponibles

## IDE et son API
* l'IDE a une API accessible aux développeurs d'extensions : la ToolsAPI
https://developpeur-pascal.fr/ressources-et-informations-sur-l-open-tools-api-otapi.html
* personnalisation de la page d'accueil de l'IDE
* DEMO
C:\Users\Public\Documents\Embarcadero\Studio\22.0\Samples\Object Pascal\VCL\VCL WelcomePage
https://github.com/Embarcadero/RADStudio11Demos/tree/main/Object%20Pascal/VCL/VCL%20WelcomePage
* personnalisation de l'éditeur de code
* DEMO
C:\Users\Public\Documents\Embarcadero\Studio\22.0\Samples\Object Pascal\ToolsAPI\Editor Demos
https://github.com/Embarcadero/RADStudio11Demos/tree/main/Object%20Pascal/ToolsAPI/Editor%20Demos

## Aide en ligne et à la saisie
* optimisations sur LSP Serveur
* Code Insight : améliorations sur code générique et anonyme, amélioration de la pertinence
* Help Insight : amélioration de la pertinence, correction de bogues sur affichage XMLDoc
* manipulations du code : Ctrl+Click amélioré, Ctrl flèche amélioré

## Documentation XML
* c'est quoi ?
https://docwiki.embarcadero.com/RADStudio/Alexandria/en/XML_Documentation_Comments
* pris en charge par Help Insight
* des templates de code prérenseignés
* désormais dans les DCU pour distribution sans code source
* DEMO : montrer ce que donne XMLDoc avec un simple projet utilisant une unité
* DEMO : montrer comment saisir la doc compatible et les templates de code disponibles

## Réseau, Internet et API
* des changements sur TMultipartContentParser
* TOAuth2Authenticator modifié pour retenter une demande de token automatiquement (utile avec API Google)
* TRESTResponseDataSetAdapter amélioré pour les JSON à plusieurs niveaux (nested elements)
* des changements sur TEMSDataSetResource et les serveurs SOAP
* mise à jour des composants et librairies d'accès à Amazon AWS dispo sur GetIt avec "Appercept AWS SDK for Delphi"
https://getitnow.embarcadero.com/aws-sdk-for-delphi-preview/

https://www.esegece.com/openapi/what-is-openapi

## GetIt
* accélération de l'interface utilisateur
* mise à niveau de nombreux paquets au fil des mois
* ajout des plateformes manquantes sur "Radiant Shapes"
* une version beta de XML Mapper disponible
* DEMO : comment trouver GetIt dans l'IDE, le lancer, faire des recherches dedans

https://getitnow.embarcadero.com

## Projet AutoGetIt
* avantages et inconvénients de GetIt depuis l'IDE
* comme de nombreuses fonctionnalités de Delphi GetIt est aussi en ligne de commande
* projet open source de David Cornelius
* liens : blog
https://corneliusconcepts.tech
* liens : livre
https://delphi-books.com/en/Fearless-Cross-Platform-Development-with-Delphi.html
* explications par Jim McKeeth
https://blogs.embarcadero.com/streamlining-rad-studio-upgrades-with-getit/
* DEMO : installation DOSCommand depuis GetIt ou son dépôt, téléchargement, compilation, utilisation
https://github.com/TurboPack/DOSCommand
https://github.com/corneliusdavid/AutoGetIt

## RTL
* optimisations, améliorations et corrections internes
* prise en charge des processeurs récents pour la compilation de System.Move permettant des gains jusqu'à x5 en copie de zones mémoires d'après les tests effectués sur de vrais ordinateurs et des VM
* mise à niveau de ZLib en 1.2.13
* accélération de la récupération des fichiers depuis un dossier bien rempli (TDirectory.GetFiles)

## VCL
* poursuite des améliorations liées à la résolution d'écran (High DPI, 4K) dans l'IDE
* poursuite des améliorations liées à la résolution d'écran (High DPI, 4K) dans les composants VCL
* poursuite des améliorations liées à la résolution d'écran (High DPI, 4K) dans les styles VCL
* des modifications sur différents composants
* TNumberBox : la saisie de nombres quand on a une valeur minimale a été corrigée
* DEMO : projet VCL avec composant TNumberBox
https://github.com/DeveloppeurPascal/Delphi-samples/tree/main/VCL-Samples/011-TNumberBox-MinValue
* TControlList : sélection multiple ajoutée
https://docwiki.embarcadero.com/RADStudio/Alexandria/en/Using_VCL_TControlList_Control
https://serialstreameur.fr/webinaire-20210520.php
* DEMO : montrer la configuration prédéfinie du TControlList sur un projet VCL vierge
* DEMO : projet VCL TControlList avec multisélection activée par code (car c'est un helper)
https://github.com/DeveloppeurPascal/Delphi-samples/tree/main/VCL-Samples/012-TControlList-MultiSelect
* TTouchKeyboard : correction de la prise en charge du background provenant du style VCL du projet
* DEMO : projet VCL avec un style et un TTouchKeyboard
https://github.com/DeveloppeurPascal/Delphi-samples/tree/main/VCL-Samples/013-TTouchKeyboard-Style

## FireMonkey
* des améliorations liées à la résolution d'écran (High DPI, 4K) en FMX
* optimisations sur TCanvas et TBitmap
* optimisations sur un ensemble de composants en saisie et affichage (liées aux changements ci-dessus et aux ascenseurs)
* correction de la propriété FocusControl sur TLabel
* DEMO : projet FMX avec TLabel, touche de raccourci et TEdit
https://github.com/DeveloppeurPascal/Delphi-samples/tree/main/FireMonkey-Samples/016-TLabel_Shortcut-and-Tabulation
* amélioration de la tabulation (TAB et Shift+TAB) sur les appareils utilisant un clavier
* modification gestion mémoire pour Android (suite à changement dans l'OS en version 12)
* nouvelle interface IFMXPhoneDialerListenerService pour Android
https://docwiki.embarcadero.com/Libraries/Alexandria/en/FMX.PhoneDialer.IFMXPhoneDialerListenerService
* nouvelle modification du manifest sur Android pour fonctionner en 12 et plus (exported sur Activity)
* DEMO : contenu du fichier TemplateManifest pour Android
* nouveau composant TBiometricAuth pour iOS et Android
https://docwiki.embarcadero.com/Libraries/Alexandria/en/FMX.BiometricAuth.TBiometricAuth
* DEMO : projet FMX sur iOS/Android utilisant le TBiometricAuth
https://github.com/DeveloppeurPascal/Delphi-samples/tree/main/FireMonkey-Samples/017-TBiometricAuth

## Platform Assistant Server (PAServer)
* pour faire quoi ? débogage, déploiement distant, travail avec Mac, iOS et Linux
https://docwiki.embarcadero.com/RADStudio/Alexandria/en/PAServer,_the_Platform_Assistant_Server_Application
* PAServer en pratique
https://serialstreameur.fr/webinaire-20191105.php
* mis à niveau comme à chaque version
* utilisation de Python 3 pour débogage partout avec possibilité de basculer en 2.7 sur anciens Mac (cf notes de version)
* debogueur LLDB partout sauf Windows

## Déploiement de projets
* ajout "Team ID" sur macOS et macOS ARM pour déploiement "ID Développeur"
* DEMO : montrer écran de paramétrage
* ajout de l'URL d'un serveur de signature sur Windows 32 et 64 bits pour déploiement "Ad-Hoc"
* DEMO : montrer écran de paramétrage
* proposer alternative avec EXE Bulk Signing
https://github.com/DeveloppeurPascal/ExeBulkSigning
* DEMO : montrer le fonctionnement d'Exe Bulk Signing
* rediffusion des extraits du stream Twitch du 28 février 2023 :
- config plateformes cibles : https://developpeur-pascal.fr/configuration-des-plateformes-cibles-dans-rad-studio-113-alexandria.html
- config approvisionnements : https://developpeur-pascal.fr/configuration-des-informations-d-approvisionnement-dans-rad-studio-113-alexandria.html

## Bases de données
* IB 2020 update 4 fourni en Developer Server, IBToGo et IBLite
* mise à jour driver PostgreSQL pour FireDAC (14, 15.1) et nouveau paramètre pour Fast Fetch
* mise à jour driver Oracle
* mise à jour de la librairie d'accès à MongoDB
* prise en charge d'UTF-8 sur Linux pour TStringField et les ensembles de données FireDAC

## Conclusion
* où trouver la doc ?
https://docwiki.embarcadero.com
* comment soumettre des demandes (nouveautés, corrections)
https://quality.embarcadero.com
* où revoir cette présentation ?
https://serialstreameur.fr/quoi-de-neuf-dans-la-version-113-alexandria.html
* contact Barnsten et moi
https://www.barnsten.com/fr/
