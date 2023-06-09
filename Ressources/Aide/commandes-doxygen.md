# Commandes spéciales Doxygen

> **SOMMAIRE**
> + [author / authors](#author--authors)
> + [brief / short](#brief--short)
> + [bug](#bug)
> + [class](#class)
> + [copyright](#copyright)
> + [date](#date)
> + [def](#def)
> + [deprecated](#deprecated)
> + [details](#details)
> + [enum](#enum)
> + [file](#file)
> + [fn](#fn)
> + [interface](#interface)
> + [mainpage](#mainpage)
> + [namespace](#namespace)
> + [package](#package)
> + [page](#page)
> + [param](#param)
> + [remark / remarks](#remark--remarks)
> + [return / result](#return--result)
> + [retval](#retval)
> + [since](#since)
> + [struct](#struct)
> + [throw / throws](#throw--throws)
> + [todo](#todo)
> + [union](#union)
> + [var](#var)
> + [version](#version)
> + [warning](#warning)

---

## author / authors

Noms d'auteurs :

```python
##
# @author Chuck Norris
# @author Chuck Norris Jr.
#
print("Hello World !")
```

## brief / short

Courte description :

```java
/**
* @brief Charge une partie sauvegardée
*/
public void loadData(String filename)
{
	// code...
}
```

## bug

Présence d'un bogue :

```java
/**
* @brief Charge une partie sauvegardée
* @bug Fait planter l'application si le nom du fichier contient des accents
*/
public void loadData(String filename)
{
	// code...
}
```

## class

Classe :

```php
/**
* @class SQLEngine sqlengine.php
* Moteur de connexion à une base de données SQL
*/
class SQLEngine
{
	// code...
}
```

## copyright

Droits d'auteur :

```c
/**
* @copyright Copyright 2021 Norris - Tous droits réservés
*/
#include <stdio.h>

int main(void)
{
	// code...
	return 0;
}
```

## date

Date d'écriture/publication :

```java
/**
* @author Chuck Norris
* @date 23-04-2015
*/
public class App
{
	// code...
}
```

## def

Définition d'une macro (préprocesseur) :

```c
/**
* @def STORAGE_MAX_ITEMS
* Nombre d'objets maximum dans l'inventaire
*/
#define STORAGE_MAX_ITEMS 50
```

## deprecated

Élément obsolète ou dépréciée :

```php
/**
* @brief Se connecte à une base de données MySQL
* @deprecated Utiliser connect_with_PDO() à la place
*/
public function connect_with_mysql()
{
	// code...
}
```

## details

Longue description :

```csharp
/**
* @brief Vérifie si un fichier média peut-être écrasé
* @details Vérifie le niveau de permission du fichier pour enregistrer une nouvelle version de ce dernier
*/
public bool IsWritableMediaFile(MediaFile &f)
{
	// code...
}
```

## enum

Énumération (type à constantes nommées) :

```c
/**
* @enum AlertLevel
* Définit le niveau d'une alerte suivant l'erreur survenue à l'exécution
*/
enum AlertLevel
{
	SUCCESS = 0, 
	INFO = 1, 
	WARNING = 5, 
	ERROR = 6, 
	FATAL_ERROR = 7
};
```

## file

Description d'un fichier :

```cpp
/**
* @file packetstream.cpp
* Gère les paquets réseau sur le flux
*/

PacketStream::encode()
{
	// code...
}

PacketStream::write()
{
	// code...
}
```

## fn

Fonction ou méthode :

```c
/**
* @fn void print_message(const char* message)
* @brief Affiche un message à l'écran
* @param message Message à afficher
*/
void print_message(const char* message);
```

## interface

Interface :

```php
/**
* @interface IExportable exportable.php
* Interface des fonctionnalités d'export d'un fichier en différents formats
*/
interface IExportable
{
	public function export(string $filename);
}
```

## mainpage

Page d'accueil de la documentation :

```
/**
* @mainpage
* # Page d'accueil
* Bonjour et bienvenue sur la documentation !
*/
```

Vous pouvez aussi créer un fichier au format Markdown et le spécifier lors de la génération de la documentation grâce à l'option _USE_MDFILE_AS_MAINPAGE_ (onglet _Expert_ > _Input_) :

```markdown
# Page d'accueil

Bonjour et bienvenue sur la documentation. Retrouvez :

+ Une liste des fonctions
+ L'ensemble des structures
+ Et même un [serveur Discord](https://discord.gg/LaMatrice) pour communiquer vos retours

## Partie 1

Bla bla bla...

## Partie 2

Bla bla bla...
```

## namespace

Espace de nom :

```csharp
using System;

/**
* @namespace Views
* Espace des vues de l'application
*/
namespace Views
{
	class Index
	{
		// code...
	}
}
```

## package

Paquet Java :

```java
/**
* @package Util
* Utilitaires de Chuck Norris (comme s'il en avait besoin)
*/
package ChuckNorris.Util;
```

## page

Page associée dans la documentation :

```cpp
/**
* @page NomDePage
* Bonjour, ceci est le contenu de la page associée...
*/
Util::loadConfig(const std::string filename)
{
	// code...
}
```

## param

Paramètre de fonction/méthode :

```c
/**
* @brief Affiche un message à l'écran
* @param author Auteur du message
* @param text Message à afficher
*/
void print_message(const char* author, const char* text);
```

## remark / remarks

Note mise en avant :

```python
##
# @brief Trie un inventaire par catégorie d'objet
# @remark Cette méthode est très lente à l'exécution
#
def sort_inventory(Inventory i):
	pass
```

## return / result

Retour d'une fonction/méthode :

```c
/**
* @brief Vérifie si une Liste est vide
* @param li La liste à vérifier
* @return Vrai (true) si la Liste est vide, faux (false) sinon
*/
bool isEmptyList(const struct List* li);
```

## retval

Valeur de retour d'une fonction/méthode :

```c
/**
* @brief Vérifie si une Liste est vide
* @param li La liste à vérifier
* @return Un booléen
* @retval Vrai (true) si la Liste est vide
* @etval Faux (false) si la liste contient des éléments
*/
bool isEmptyList(const struct List* li);
```

## since

Indique un élément ajouté à partir d'une certaine version :

```python
##
# Exporte le fichier au format MKV
# @since 3.4
#
def export_to_mkv(filename):
	pass
```

## struct

Structure :

```c
/**
* @struct Point2D
* Définit un point dans un plan à deux dimensions
*/
struct Point2D
{
	int x;
	int y;
};
```

## throw / throws

Donne des indications sur une exception pouvant être déclenchée :

```python
##
# @brief Fait la division de deux nombres entiers
# @throw ZeroDivisionError Déclenchée si le dénominateur est nul
def division(a, b):
	# code...
	pass
```

## todo

Indique un élément à revoir/corriger/écrire plus tard :

```csharp
/**
* @brief Sauvegarde les données
* @todo Ajouter une option d'export au format JSON
*/
public static void Save(string filename)
{
	// code...
}
```

## union

Union :

```c
/**
* @union Book
* Définition d'un ouvrage
*/
union Book
{
	char ISBN_10[11];
	char ISBN_13[14];
};
```

## var

Variable ou valeur nommée :

```php
/**
* @var \Models\UserModel $username
* Nom de l'utilisateur
*/
private string $username;
```

## version

Numéro de version :

```c
/**
* @file list.c
* @version 0.1 Alpha
*/
#include "list.h"

struct List* new_list()
{
	// code...
}
```

## warning

Avertissement :

```java
/**
* @brief Envoie un message sur le flux
* @warning Ne fonctionne pas dans un environnement multi-threadé
*/
public void sendToStream(String msg)
{
	// code...
}
```

---

[Plus de commandes Doxygen...](https://www.doxygen.nl/manual/commands.html)
