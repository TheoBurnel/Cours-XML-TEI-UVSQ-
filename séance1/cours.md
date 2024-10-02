# Introduction à XML-TEI

## À quoi sert la TEI ?

La TEI (Text Encoding Initiative) est une **norme internationale** utilisée pour encoder des textes, en particulier dans les sciences humaines et les lettres. Elle sert à structurer, annoter, et préserver des textes dans des formats numériques de manière à ce qu'ils soient lisibles et exploitables par les machines, tout en restant fidèle au texte original.

### Pourquoi la TEI est-elle utile ?

1. **Préservation et Accessibilité** : La TEI permet de conserver et de rendre accessibles des textes anciens, rares, ou importants dans un format numérique. Elle garantit que le texte reste lisible et exploitable à long terme, même si les technologies évoluent.

2. **Interopérabilité** : La TEI utilise le langage XML, un standard largement accepté, ce qui permet aux textes encodés d'être utilisés dans différents logiciels et systèmes sans perdre d'informations. Cela facilite la collaboration entre chercheurs, bibliothèques, éditeurs, et institutions.

3. **Analyse Textuelle Avancée** : Grâce à l'encodage TEI, les chercheurs peuvent analyser des textes de manière précise et détaillée, en utilisant des outils numériques pour des recherches linguistiques, littéraires, historiques, etc.

4. **Documentation et Annotation** : La TEI permet d'ajouter des informations contextuelles, des commentaires, des liens, des métadonnées, et bien d'autres annotations directement dans le texte. Cela enrichit le texte et le rend plus utile pour les recherches futures.

### À quel moment les étudiants de lettres utiliseront-ils la TEI dans le monde professionnel ?

1. **Édition de Textes Anciens ou Rares** :
   - **Exemple** : Si vous travaillez dans l'édition numérique ou dans une bibliothèque, vous pourriez être chargé de numériser et d'annoter des manuscrits médiévaux ou des textes littéraires classiques. La TEI vous permettra de représenter fidèlement les particularités du texte, telles que les variantes orthographiques, les notes marginales, ou les corrections.

2. **Recherche Académique** :
   - **Exemple** : En tant que chercheur ou assistant de recherche, vous pourriez encoder des corpus de textes pour des analyses statistiques ou stylistiques. Par exemple, encoder les œuvres complètes d'un auteur pour étudier l'évolution de son style ou la fréquence de certains motifs littéraires.

3. **Travail dans des Bibliothèques ou Archives** :
   - **Exemple** : Si vous travaillez dans une bibliothèque ou un centre d'archives, la TEI sera essentielle pour cataloguer et rendre accessibles les collections numériques. Vous pourriez être responsable de l'encodage de collections de correspondances, de journaux intimes, ou de documents historiques.

4. **Humanités Numériques (Digital Humanities)** :
   - **Exemple** : Dans des projets de humanités numériques, la TEI est souvent utilisée pour créer des bases de données textuelles complexes. Par exemple, pour un projet collaboratif de cartographie littéraire, où des textes sont encodés pour permettre l'exploration des lieux mentionnés dans les récits.

5. **Musées et Institutions Culturelles** :
   - **Exemple** : Si vous travaillez dans un musée ou une institution culturelle, vous pourriez participer à la numérisation et à l'annotation de collections pour les rendre accessibles au public en ligne, avec des transcriptions et des annotations détaillées.

### En Conclusion
 Si on vous enseigne de la TEI, c’est parce dans le monde de plus en plus numérique de la recherche et de la culture, la maîtrise de la TEI pourrait vous être demandée pour un emploi. Vous aurez à la fin de l’année un master, il serait dommage qu’une opportunité se ferme pour vous uniquement parce que vous n’avez pas cette compétence technique

## Exemple : Arrêt du Parlement de Bordeaux, 17 décembre 1562
L'édition propose le texte en version originale, avec ses rayures, et le texte corrigé :
http://xtf.bvh.univ-tours.fr/xtf/view?docId=tei/FRAD0330635101_1B252_179/FRAD0330635101_1B252_179_tei.xml&doc.view=notice;

## Exemple : L’année 1437 dans la pratique de Pierre Christofle, notaire du Châtelet d’Orléans
L’édition électronique intégrale des notes du notaire Pierre Christofle pour l’année 1437 est un projet d’abord mené à l’université d’Ottawa par Kouky Fianu, professeur à l’université d’Ottawa,  avec la collaboration d’Anne Fortier, étudiante de maîtrise de l’université d’Ottawa, puis développé dans sa version électronique par Florence Clavaud, conservateur en chef du patrimoine aux Archives nationales, membre du Centre Jean-Mabillon à l’École nationale des chartes.

La source :
https://www.archives-loiret.fr/decouverte-des-archives/notre-actualite-1/2020/notaires#visionneuse-cms_13707121_2

L'encodage XML-TEI :
https://raw.githubusercontent.com/Segolene-Albouy/XML-TEI_M2TNAH/main/01-Introduction_XML/Exemples_encodage/Christofle-septembre2016.xml

Résultat :
http://elec.enc.sorbonne.fr/christofle/index.html

---
## Le texte informatisé
### 1. Texte Brut

Un **texte brut** est une version simple et non formatée d'un texte, contenant uniquement les caractères (lettres, chiffres, symboles) sans aucune mise en forme ou balise. Ce type de texte est très basique, utile pour le stockage ou la manipulation rapide, mais il ne contient aucune information sur la structure ou la présentation.

**Exemple :**
```plaintext
Bonjour à tous. Aujourd'hui, nous allons étudier les bases de la TEI.
```

Dans cet exemple, le texte est simplement une séquence de caractères. Il n'y a aucune indication sur la structure (comme des paragraphes ou des titres) ni sur la présentation (comme la mise en gras ou en italique).

### 2. Texte Balisé

Un **texte balisé** utilise des balises pour décrire la structure et le contenu du texte. Dans le contexte de la TEI (ou XML en général), ces balises aident à organiser et à donner un sens aux différentes parties du texte. Le balisage ajoute une couche d'information qui peut être utilisée pour l'analyse, l'affichage ou la transformation du texte.

**Exemple :**
```xml
<document>
  <title>Introduction à la TEI</title>
  <body>
    <p>Bonjour à tous. <emphasis> Aujourd'hui, nous allons étudier</emphasis> les bases de la TEI.</p>
  </body>
</document>
```

Dans cet exemple, le texte brut a été enrichi de balises XML. La balise `<title>` indique le titre du document, tandis que la balise `<p>` indique un paragraphe. La balise `<emphasis>` indique que la phrase "Aujourd'hui, nous allons étudier" doit être mise en évidence, ce qui pourrait se traduire par de l'italique ou du gras lors de l'affichage.

### 3. Texte Formaté

Le **texte formaté** est la version finale qui inclut non seulement le contenu et la structure, mais aussi des éléments de présentation visuelle. Cette forme de texte est celle qui serait affichée à l'utilisateur final, soit sur un écran, soit sur une page imprimée.

**Exemple :**

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Introduction à la TEI</title>
    <style>
        .emphasis {
            font-style: italic;
            color: blue;
        }
    </style>
</head>
<body>
    <h1>Introduction à la TEI</h1>
    <p>Bonjour à tous. <span class="emphasis">Aujourd'hui, nous allons étudier</span> les bases de la TEI.</p>
</body>
</html>
```

Dans cet exemple en HTML, le texte est non seulement structuré (comme dans le texte balisé), mais il est aussi formaté pour être visuellement agréable. Le titre est maintenant représenté par une balise `<h1>`, qui applique une mise en forme particulière (plus grand, en gras). La phrase "Aujourd'hui, nous allons étudier" est non seulement mise en évidence avec une balise `<span>` (ce qui est analogue à `<emphasis>` dans XML), mais elle est également stylisée pour apparaître en italique et en bleu grâce à un style CSS.

### Conclusion

Ces trois étapes montrent comment un texte peut évoluer depuis sa forme brute jusqu'à une version richement formatée et structurée, prête à être affichée ou imprimée. Chacune de ces étapes ajoute une couche supplémentaire d'information ou de présentation, rendant le texte plus utile, plus informatif, et plus accessible pour différents usages. <br>
Dans le cadre de notre cours sur la TEI, nous produirons uniquement des textes balisés, c'est à dire des textes enrichis, mais qui demeurent dans un format libre.

## Qu'est-ce qu'un texte?
Quelles peuvent être ses caractéristiques ? Comment les retranscrire numériquement ? <br>
Voici une structure simplifiée :
![Structure d'un texte](ressources/structure-texte.png) 

Lorsqu'on pense à une structure de texte en trois temps comme métadonnées, contenu intellectuel, et matérialité, la TEI s'intéresse de manière détailée à chacun de ces éléments :

### 1. Métadonnées
Les métadonnées sont des informations qui décrivent le texte, plutôt que d'en faire partie directement. Elles incluent des éléments tels que :
- Informations sur l'œuvre : Titre, auteur, date de création, lieu de publication.
- Informations sur le document : Édition, révision, source d'origine, format physique.
- Informations sur l'encodage : Qui a encodé le texte, quand, selon quelles règles ou conventions. <br>

Exemple en TEI :

**Exemple :**
```xml
<teiHeader>
  <fileDesc>
    <titleStmt>
      <title>Le Cid</title>
      <author>Pierre Corneille</author>
    </titleStmt>
    <publicationStmt>
      <publisher>Gallimard</publisher>
      <pubPlace>Paris</pubPlace>
      <date>1637</date>
    </publicationStmt>
    <sourceDesc>
      <bibl>Corneille, Pierre. *Le Cid*. Paris: Gallimard, 1637.</bibl>
    </sourceDesc>
  </fileDesc>
</teiHeader>
```

Ces balises permettent de structurer et de récupérer des informations sur le texte pour le catalogage, la recherche ou l’archivage.

### 2. Contenu Intellectuel
Le contenu intellectuel fait référence à ce qui constitue la substance du texte, c'est-à-dire les mots, les idées, la narration, les dialogues, etc. La TEI permet de structurer et d'enrichir ce contenu.

- Structuration du texte : Chapitres, sections, paragraphes.
- Éléments littéraires : Discours direct, citations, poésie, dialogues.
- Annotation sémantique : Références croisées, allusions, annotations critiques.

Exemple en TEI :

**Exemple :**
```xml
<text>
  <body>
    <div type="act" n="1">
      <head>Acte I</head>
      <div type="scene" n="1">
        <head>Scène 1</head>
        <sp who="#Rodrigue">
          <p>Ô rage ! ô désespoir ! ô vieillesse ennemie !</p>
        </sp>
      </div>
    </div>
  </body>
</text>
```

Ici, la TEI encode la structure dramatique d'une pièce de théâtre, en distinguant les actes, les scènes et les dialogues, tout en conservant la richesse du contenu intellectuel.

### 3. Matérialité
La matérialité du texte renvoie à ses aspects physiques ou visuels, c'est-à-dire comment le texte est présenté sur la page ou dans le document numérique. Cela peut inclure :

- Mise en page : Marges, sauts de ligne, alignement, colonnes.
- Typographie : Polices, tailles, styles (gras, italique).
- Annotations matérielles : Notes de marge, corrections, ajouts manuels.
- Matérialité physique : État de conservation du document, supports (papier, parchemin).

Exemple en TEI :

**Exemple :**
```xml
<surface>
  <graphic url="manuscript_page.jpg" n="1"/>
  <zone ulx="50" uly="100" lrx="250" lry="200">
    <p>Ô rage ! ô désespoir ! ô vieillesse ennemie !</p>
  </zone>
</surface>
```

Cette structure capture la disposition visuelle d'un texte sur une page manuscrite, montrant où le texte apparaît sur l'image numérisée d'une page.

### Conclusion
La TEI permet de traiter ces trois aspects essentiels d'un texte en fournissant des balises spécifiques pour encoder non seulement le contenu textuel, mais aussi les informations sur le document lui-même (métadonnées) et sa présentation physique (matérialité). Ce niveau de détail permet de préserver et d'analyser non seulement le texte en tant qu'œuvre littéraire, mais aussi ses manifestations matérielles, offrant une vue d'ensemble complète pour l'édition critique.

---
## Caractéristiques du XML
Format de données simple, documenté, conçu pour la description des documents textuels.

### Un standard international
Depuis 1998, XML est un langage libre et documenté. C’est un standard respectant les recommandations du W3C, il facilite :
- la lisibilité par les machines ou par l’œil humain ;
- l’échange de données ;
- la migration vers d’autres plateformes, d’autres logiciels, d’autres formats.

Il existe plusieurs langages XML :
- TEI: encodage des documents patrimoniaux
- EAD: description des fonds archivistiques
- XHTML: structure d'une page web
- SVG: documents vectoriels

### Un langage à balise
Nous allons apprendre à passer d'un texte brut à texte balisé dans le cadre de cours.
C'est à dire de passer de ce texte :
```plaintext
Haïku
Takahama Kyoshi

Le serpent s’esquiva
Mais le regard qu’il me lança
Resta dans l’herbe.
```

à cet encodage :
```xml
{poeme}
    {meta}
{type}Haïku{type}
{auteur}Takahama Kyoshi{auteur}
    {meta}
    {contenu}
{vers}Le serpent s’esquiva{vers}
{vers}Mais {gras}le regard{gras} qu’il me lança{vers}
{vers}Resta dans l’herbe.{vers}
    {contenu}
{poeme}
```

---
## Principes fondamentaux du XML
Les principes fondamentaux du balisage en XML reposent sur un ensemble de règles et de conventions qui permettent de structurer et de présenter un texte. Voici un aperçu de ces principes :

### 1. La Déclaration XML

Il est obligatoire de commencer son document par une déclaration XML. C'est ce qui identifie le document et le rend intelligble par la machine. Dans un premier temps, nous allons seulement faire cette déclaration simple. Elle sera toujours écrite en première ligne du document. 

``` xml
<?xml version="1.0" encoding="UTF-8"?>
```

### 2. Les Balises

Les balises TEI sont des éléments de base qui définissent la structure et le contenu d'un document numérique. Chaque balise est entourée de crochets angulaires (`< >`) et vient généralement par paires : une balise ouvrante et une balise fermante.

- **Balise ouvrante** : Indique le début d'un élément. Par exemple, `<p>` pour commencer un paragraphe.
- **Balise fermante** : Indique la fin d'un élément. Elle se distingue par une barre oblique (`/`). Par exemple, `</p>` pour terminer un paragraphe.

**Exemple :**
```xml
<p>Bonjour, ceci est un paragraphe.</p>
```
Dans cet exemple, `<p>` ouvre un paragraphe, et `</p>` le ferme.

En TEI, les balises entourent les éléments textuels pour leur donner un sens spécifique.

- **Balise ouvrante** : Par exemple, `<title>` pour indiquer le titre d'une œuvre.
- **Balise fermante** : La balise fermante correspondante serait `</title>`.
Exemple :

```xml
<title>Le Cid</title>
```

Ici, `<title>` indique que "Le Cid" est le titre de l'œuvre.


### 3. Imbrication des Balises

L'imbrication des balises fait référence au fait d'inclure une balise à l'intérieur d'une autre. L'ordre de fermeture des balises est important : la balise ouverte en dernier doit être fermée en premier.

**Règle d'imbrication :**
```xml
<parent>
  <enfant>
    <petit-enfant></petit-enfant>
  </enfant>
</parent>
```

**Exemple en TEI:**
```xml
<text>
  <body>
    <div type="act" n="1">
      <head>Acte I</head>
      <p>Voici le début de l'acte I.</p>
    </div>
  </body>
</text>
```

**Exemple correct :**
```xml
<p>Ce texte est <hi rend="italic">important</hi>.</p>
```

**Exemple incorrect :**
```xml
<p>Ce texte est <hi rend="italic">important.</p></hi>
```

Dans l'exemple incorrect, la balise `<hi>` est fermée après la balise `<p>`, ce qui n'est pas correct. L'erreur d'imbrication en TEI pourrait entraîner des problèmes d'analyse ou d'affichage lors du traitement du texte.


### 4. Héritage des Styles

En TEI, l'héritage des styles n'existe pas de la même manière qu'en HTML/CSS, mais on peut parler d'héritage des attributs ou de la signification sémantique. Par exemple, certains éléments peuvent hériter des attributs de leurs éléments parents.

**Exemple :**
```xml
<text xml:lang="fr">
  <body>
    <p>Voici un paragraphe en français.</p>
  </body>
</text>
```

Dans cet exemple, l'attribut `xml:lang="fr"` spécifie que le texte est en français. Cet attribut est hérité par tout le contenu de l'élément `<text>`.


### 5. Les Attributs

Les balises TEI peuvent également contenir des attributs qui fournissent des informations supplémentaires sur les éléments textuels, comme des indications sur le style, la langue, ou des identifiants spécifiques.

**Exemples d'attributs :**
- **`xml:id`** : Identifiant unique pour un élément.
- **`rend`** : Pour indiquer une mise en forme (ex. `rend="italic"` pour de l'italique).
- **`type`** : Pour préciser le type d'un élément, comme une division dans un texte (`div`).

**Exemple d'utilisation :**
```xml
<p xml:id="p1" rend="italic">Ceci est un paragraphe en italique.</p>
```

Ici, xml:id="p1" attribue un identifiant unique au paragraphe, et rend="italic" spécifie que le texte doit être en italique.

### 6. Auto-fermantes et Balises Vides

Certaines balises en TEI peuvent être auto-fermantes, surtout lorsqu'elles ne contiennent pas de contenu textuel direct.

**Exemples :**
```xml
<lb n="1"/>
<lb n="2"/>
```

Ici, `<lb/>` est une balise pour les sauts de ligne dans un texte transcrit. Elle est auto-fermante puisqu'elle n'a pas de contenu interne.

### 7. L'Importance de la Sémantique

Les balises TEI sont conçues pour être sémantiques, c'est-à-dire qu'elles portent une signification précise relative au texte qu'elles encadrent. Cela aide à représenter la structure logique et le contenu intellectuel du texte.

**Exemple :**
```xml
<teiHeader>
  <fileDesc>
    <titleStmt>
      <title>Le Cid</title>
      <author>Pierre Corneille</author>
    </titleStmt>
  </fileDesc>
</teiHeader>
```

Dans cet exemple, les balises `<titleStmt>`, `<title>`, et `<author>` sont sémantiques : elles indiquent respectivement le titre de l'œuvre et le nom de l'auteur.

### Conclusion

En TEI, les principes de balisage reposent sur la rigueur de l'imbrication des balises, l'utilisation appropriée des attributs, et une attention particulière à la sémantique. 

---
## Exercice
À l’aide des balises suivantes, structurer le texte proposé : 
- `<texte>`
- `<chapitre>`
- `<titreChapitre>`
- `<paragraphe>`
- `<nomPersonnage>`
- `<noteDeBasDePage>`

Le texte : 
```plaintext
Blanche-Neige mange la pomme empoisonnée
  Il était une fois Blanche-Neige1 que sa belle-mère détestait. [...]

Blanche-Neige attend le prince Charmant
  Un jour Charmant2 arriva sur son cheval blanc et la sauva. [...]
  
1 Elle porte ce nom, car son visage est blanc comme la neige
2 Nom du prince qui sauve Blanche-Neige.
```
En version XML-TEI:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<texte>
    <chapitre>
        <titreChapitre>Blanche-Neige mange la pomme empoisonnée</titreChapitre>
        <paragraphe>Il était une fois <nomPersonnage>Blanche-Neige</nomPersonnage>
            <noteDeBasDePage>Elle porte ce nom, car son visage est blanc comme la
                neige</noteDeBasDePage> que sa belle-mère détestait </paragraphe>
    </chapitre>
    <chapitre>
        <titreChapitre>Blanche-Neige attend le nain Charmant</titreChapitre>
        <paragraphe>Un jour, <nomPersonnage>Charmant</nomPersonnage><noteDeBasDePage>Nom du prince
                qui sauve Blanche-Neige</noteDeBasDePage>arriva sur son cheval blanc et la sauva. </paragraphe>
    </chapitre>
</texte>
```
---
## Les composants du XML-TEI
Le XML-TEI repose sur des composants qui structurent et enrichissent le document.

### 1. Éléments

Les **éléments** sont les blocs de construction de base du XML et de TEI. Ils encapsulent le contenu et la structure d’un document. Les éléments sont définis par des balises ouvrantes et fermantes.

#### Exemples d'Éléments TEI :

**a. Éléments de Structure**
```xml
<text>
  <body>
    <div type="chapter" n="1">
      <head>Chapitre 1</head>
      <p>Ceci est le texte du premier chapitre.</p>
    </div>
  </body>
</text>
```
- `<text>` : Élement racine pour un document TEI.
- `<body>` : Contient le contenu principal du texte.
- `<div>` : Division du texte, par exemple, un chapitre.
- `<head>` : Titre ou en-tête de la division.
- `<p>` : Paragraphe.

**b. Éléments de Contenu**
```xml
<person>
  <name>Jean Valjean</name>
  <role>Protagoniste</role>
</person>
```
- `<person>` : Représente une personne dans le texte.
- `<name>` : Nom de la personne.
- `<role>` : Rôle ou fonction de la personne.

### 2. Attributs

Les **attributs** ajoutent des informations supplémentaires aux éléments. Ils se trouvent à l'intérieur de la balise ouvrante et se composent d’un nom et d’une valeur.

#### Exemples d'Attributs TEI :

**a. Attributs pour la Mise en Forme**
```xml
<p rend="italic">Ceci est un texte en italique.</p>
```
- `rend="italic"` : Indique que le texte doit être mis en italique.

**b. Attributs pour la Classification**
```xml
<person xml:id="p1" role="author">
  <name>Victor Hugo</name>
</person>
```
- `xml:id="p1"` : Identifiant unique pour la personne.
- `role="author"` : Spécifie le rôle de la personne.

### 3. Entités

Les **entités** sont des références qui remplacent des caractères spéciaux ou des séquences de caractères dans le texte XML. Elles permettent de gérer des caractères réservés ou d'inclure des caractères non imprimables.

#### Exemples d'Entités TEI :

**a. Entités HTML Standard**
```xml
<p>Le symbole d&rsquo;apostrophe est &rsquo; dans le texte.</p>
```
- `&rsquo;` : Entité pour une apostrophe droite (`’`).

**b. Entités Personnalisées** <br>
Les entités peuvent également être définies dans une DTD ou un schéma XML pour représenter des caractères ou des séquences fréquemment utilisés.

```xml
<!ENTITY copy "©">
<p>Les droits d&rsquo;auteur sont protégés par &copy; 2024.</p>
```
- `&copy;` : Entité pour le symbole de copyright (`©`).

### 4. Commentaires

Les **commentaires** permettent d'inclure des notes explicatives dans le code XML. Ils ne sont pas affichés ou traités comme du contenu par les processeurs XML.

#### Exemples de Commentaires TEI :

**a. Commentaires Simples**
```xml
<!-- Ceci est un commentaire qui explique la section suivante -->
<text>
  <body>
    <p>Ceci est un paragraphe du texte.</p>
  </body>
</text>
```
- `<!-- Ceci est un commentaire -->` : Un commentaire pour documenter le code XML.

**b. Commentaires pour Documentation**
```xml
<text>
  <!-- Ce bloc contient le texte principal du document -->
  <body>
    <div type="section">
      <head>Introduction</head>
      <p>Le texte de l'introduction commence ici.</p>
    </div>
  </body>
</text>
```
- Les commentaires expliquent la structure ou le contenu des différentes sections du texte.

---
## Un encodage bien formé?
Un encodage bien formé suit les règles suivantes :
- 1 balise ouvrante = 1 balise fermante
- respect de l'imbrication
- un attribut du même nom par balise
- un seul élément racine

**Exercices** <br>
Bien formé ou mal formé ?
```xml
<paragraphe>du texte</paragraphe>
<paragraphe><article>du</article><nom>texte</nom></paragraphe>
<paragraphe><article>du <nom></article>texte</nom></paragraphe>
<paragraphe><article>du <nom>texte</nom></article></paragraphe>
<paragraphe type="texte">du texte</paragraphe>
<paragraphe type=texte>du texte</paragraphe>
<paragraphe type="texte">du texte<paragraphe/>
<paragraphe type="texte">du texte<nom>nom</paragraphe>
<paragraphe type="texte">du texte</Paragraphe>
<segment type="texte" type="nombre">du texte</paragraphe>
```
---
## Des exercices
Voici trois exemples supplémentaires, chacun illustrant un aspect spécifique : utilisation des éléments, ajout d'attributs, et inclusion de commentaires.

### Exemple 1 : Utilisation des éléments

**Texte :**
```plaintext
Le Petit Poucet trouve les bottes de sept lieues
  Il était une fois Le Petit Poucet que ses parents abandonnèrent dans la forêt. [...]

Le Petit Poucet trompe l'ogre
  Un jour, Poucet mit les bottes de l'ogre et sauva ses frères. [...]
```

**Élements à utiliser**
- `<text>`
- `<chapitre>`
- `<titreChapitre>`
- `<paragraphe>`
- `<nomPersonnage>`

**Version XML-TEI :**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<texte>
    <chapitre>
        <titreChapitre>Le Petit Poucet trouve les bottes de sept lieues</titreChapitre>
        <paragraphe>Il était une fois <nomPersonnage>Le Petit Poucet</nomPersonnage>
            que ses parents abandonnèrent dans la forêt.</paragraphe>
    </chapitre>
    <chapitre>
        <titreChapitre>Le Petit Poucet trompe l'ogre</titreChapitre>
        <paragraphe>Un jour, <nomPersonnage>Poucet</nomPersonnage> mit les bottes de l'ogre et sauva ses frères.</paragraphe>
    </chapitre>
</texte>
```

### Exemple 2 : Ajout d'attributs

**Texte :**
```plaintext
Cendrillon perd sa pantoufle de verre
  Il était une fois Cendrillon3 qui vivait avec ses horribles demi-sœurs. [...]

Cendrillon retrouve son prince
  Le prince4 trouva la pantoufle et chercha la jeune fille dans tout le royaume. [...]

3. Cendrillon vivait avec ses horribles demi-sœurs après la mort de son père.
4. Le prince, charmé par Cendrillon, fit tout pour la retrouver.
```

**Élements et attributs à utiliser**
- `<text>`
- `<chapitre>`
- `<titreChapitre>`
- `<paragraphe>`
- `<nomPersonnage>`
- `<noteDeBasDePage>`
- `@type`, pour qualifier les personnage
- `@id`, pour indiquer le numéro de la note

**Version XML-TEI :**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<texte>
    <chapitre>
        <titreChapitre>Cendrillon perd sa pantoufle de verre</titreChapitre>
        <paragraphe>Il était une fois <nomPersonnage type="protagoniste">Cendrillon</nomPersonnage>
            <noteDeBasDePage id="3">Cendrillon vivait avec ses horribles demi-sœurs après la mort de son père.</noteDeBasDePage>
            qui vivait avec ses horribles demi-sœurs.</paragraphe>
    </chapitre>
    <chapitre>
        <titreChapitre>Cendrillon retrouve son prince</titreChapitre>
        <paragraphe>Le <nomPersonnage type="antagoniste">prince</nomPersonnage>
            <noteDeBasDePage id="4">Le prince, charmé par Cendrillon, fit tout pour la retrouver.</noteDeBasDePage>
            trouva la pantoufle et chercha la jeune fille dans tout le royaume.</paragraphe>
    </chapitre>
</texte>
```

### Exemple 3 : Inclusion de commentaires

**Texte :**
```plaintext
La Belle au Bois Dormant reçoit une malédiction
  Il était une fois une princesse qui reçut une malédiction d'une fée jalouse. [...]

La Belle au Bois Dormant se réveille
  Un prince la réveilla avec un baiser d'amour sincère. [...]
```

**Élements et attributs à utiliser**
- `<text>`
- `<chapitre>`
- `<titreChapitre>`
- `<paragraphe>`
- commenter la place du paragraphe dans le conte

**Version XML-TEI :**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<texte>
    <chapitre>
        <titreChapitre>La Belle au Bois Dormant reçoit une malédiction</titreChapitre>
        <!-- Ce paragraphe décrit le début du conte -->
        <paragraphe>Il était une fois une princesse qui reçut une malédiction d'une fée jalouse.</paragraphe>
    </chapitre>
    <chapitre>
        <titreChapitre>La Belle au Bois Dormant se réveille</titreChapitre>
        <!-- Ce paragraphe décrit la conclusion du conte -->
        <paragraphe>Un prince la réveilla avec un baiser d'amour sincère.</paragraphe>
    </chapitre>
</texte>
```

Je comprends mieux, tu veux que le mot "Lune" soit formaté en gras dans le texte XML directement. Voici l'exemple modifié avec `<rend="bold">` pour indiquer le texte en gras dans un format XML-TEI.

### Exemple 4 : Vers un texte plus enrichi

**Texte :**
```plaintext
Le Chevalier de la Lune reçoit une quête
  Dans une nuit sans étoiles, le Chevalier de la Lune1 fut convoqué par le roi pour accomplir une quête sacrée.

Le Chevalier de la Lune affronte le Serpent des Abysses
  Après de nombreux périls, le chevalier se retrouva face au Serpent des Abysses2, gardien de l'entrée du royaume perdu.

1. Le Chevalier de la Lune est un personnage mythique, symbolisant le lien entre la lumière et l'ombre.
2. Le Serpent des Abysses est une créature ancestrale, symbole des dangers cachés dans les profondeurs de l'âme humaine.
```

**Éléments et attributs à utiliser**
- `<texte>`
- `<chapitre>`
- `<titreChapitre>`
- `<paragraphe>`
- commenter la place du paragraphe dans le déroulement de l'histoire
- `<nomPersonnage>` avec attribut `@id` pour les références
- `<noteDeBasDePage>` avec attribut `@id` pour les notes explicatives
- Mettre **quête** et **périls** en gras avec `<rend="bold">`

**Version XML-TEI :**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<texte>
    <chapitre>

        <titreChapitre>Le Chevalier de la Lune reçoit une <hi rend="bold">quête</hi></titreChapitre>
        <!-- Ce paragraphe présente le point de départ de l'aventure, où le héros accepte son destin -->

        <paragraphe>Dans une nuit sans étoiles, <nomPersonnage id="1">le Chevalier de la Lune </nomPersonnage><noteDeBasDePage id="1"><nomPersonnage id="1">Le Chevalier de la Lune </nomPersonnage>est un personnage mythique, symbolisant le lien entre la lumière et l'ombre.</noteDeBasDePage> fut convoqué par le roi pour accomplir une <hi rend="bold">quête</hi> sacrée.</paragraphe>
    </chapitre>

    <chapitre>
        <titreChapitre>Le Chevalier de la Lune affronte le Serpent des Abysses</titreChapitre>
        <!-- Ce paragraphe décrit l'apogée du conte, où le héros doit faire face à son plus grand adversaire -->
        
        <paragraphe>Après de nombreux <hi rend="bold">périls</hi>, <nomPersonnage id="1">le Chevalier de la Lune</nomPersonnage> se retrouva face au <nomPersonnage id="2">Serpent des Abysses</nomPersonnage><noteDeBasDePage id="2"><nomPersonnage id="2">Le Serpent des Abysses</nomPersonnage> est une créature ancestrale, symbole des dangers cachés dans les profondeurs de l'âme humaine.</noteDeBasDePage>, gardien de l'entrée du royaume perdu.</paragraphe>
    </chapitre>

</texte>
```

