Puppet
======


Ecrit en Ruby.
Les fichiers sont donc aussi en Ruby

## Elements de références

https://puppet.com/docs/puppet/5.5/lang_summary.html


## Elements de concepts

 - Ressources : unité fondamentale de modelisation dans Puppet. Les ressorces decrivents un aspect d'un systeme. Exemple : un service ou un package.
 - Classes :  regroupement organisé de ressources?. Les classes deviennet des unités aggrégées de configuration. Ainsi une classes à titre d'exmple peut décrire tout un service, alors qu'une ressource pourrait être un fichier de configuration du service en question. Les classes peuvent être utilisée à des fins d'aggrations  : une classe peut être un agrégat de classes.
 - Noeud :  un noeud se verra allouer un ensemble de classes. La phase de cconfiguration des clases aux noeuds est la phase de __classification__. Les noeuds peuvent être classifiés via la declaration de noeuds ou bien par le biais d'outils complémentatire à Puppet (ENC, Hiera)
 - les manifest :  fichiers portant l'extension `.pp` Il existe un __main manifest__ qui est défini soit dans la conf du puppet master. Le puppet master peut doit chargé un point d'entrée unique soit un fichier contenant les manifest, et les executer dans l'ordre alphabetique.
 - les modules :  sont des structreus de repertoires contenant des fichiers de configuration et du code (manifest notamment). Le poitn d'entrée du module est le fichier manifest portant le nom `init.pp` la classe déclarée dedans doit porter celle du module
 - catalog : resultantes de la phase de compilation Puppet des manifests. Cette phase de compilation consiste à personnaliser pour un noeud la logique issue du manifest. Ainsi dans un manifest il ya des éléments de logiques (conditions, tests etc...) alors que dans les catalog non. Il s'agit d'une phase d'épuration des manifest pour un seul noeud
