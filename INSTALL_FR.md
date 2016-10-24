Installez Directions
====================

Linux
-----

**Stack**

Pour beaucoup Unix systèmes d'exploitation exécutez la commande suivante pour installer Stack:

```bash
$ wget -qO- https://get.haskellstack.org/ > installer
$ sha256sum installer
$ bash installer
```

Stack Checksum: ``a651e631e2ce9b69259badac3d88a3b7278b0a5f626854cc62f2f0f13a32e4ba``

**LLVM**

Le compilateur LLVM toolchain peut être installé via le gestionnaire de paquets
du système. Sur Debian Variantes:

```bash
$ sudo apt-get install llvm-3.5 llvm-3.5-dev
```

Vérifier

```bash
$ llvm-config --ldflags
-L/usr/lib/llvm-3.8/lib  -lpthread -lffi -ltinfo -ldl -lm
```

**Z3**

Le démonstrateur Z3 peut être installé via le gestionnaire de paquets du système. Sur Debian
variantes:

```bash
$ sudo apt-get install z3 libz3-dev
```

Le paquet existe sous Ubuntu mais n'est valable que sur l'unstable de Debian.

Vérifier

```bash
$ z3 -version
Z3 version 4.4.1
```

Mac OSX
-------

**Stack**

Il existe plusieurs façons d'installer Stack sur OSX:

[Installateur graphique](https://www.stackage.org/stack/osx-x86_64)

ou

```bash
$ brew install haskell-stack
```

**LLVM**

Le compilateur LLVM toolchain peut être installé via la brew formule:

```bash
$ brew install libffi llvm35
```

Vérifier

```bash
$ $(brew --prefix llvm35)/bin/llvm-config-3.5 --ldflags
-L/usr/local/Cellar/llvm35/3.5.1/lib/llvm-3.5/lib
```

**Z3**

Le démonstrateur Z3 peut être installé via la brew formule:

```bash
$ brew install z3
```

Vérifier

```bash
$ z3 -version
Z3 version 4.4.1
```

Haskell
-------

Pour construire le projet:

```bash
$ git clone https://github.com/sdiehl/paris-fp.git
$ cd paris-fp
$ stack setup
$ stack build
```

enfin lancez le script petit 
```bash
$ ./petit
...
Environnement est bon!
```

Si vous voyez ce message, tout marche !
