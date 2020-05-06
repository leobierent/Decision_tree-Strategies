# Decision_tree-Strategies
### Instructions :
Nous allons aplatir l'arbre de decision (tree_to_convert.txt) pour en faire un ensemble de stratégies.

Une stratégie est une combinaison de

● Une définition de stratégie: une séquence de conditions de la forme entité = valeur ou entité! = valeur, séparée uniquement par les opérateurs «et».

● Une valeur feuille:  La syntaxe est donnée par [définition de stratégie]: [valeur_feuille].

Voici un exemple d'arbre : 

0:[device_type=pc||or||browser=7] yes=2,no=1
	2:[os_family=5] yes=6,no=5
		6:[browser=8] yes=12,no=11
			12:[language=2] yes=20,no=19
				20:leaf=0.000559453
				19:leaf=0.000594593
			11:[size=300x600] yes=18,no=17
				18:leaf=0.000597397
				17:leaf=0.00063461
		5:[browser=8||or||browser=5] yes=10,no=9
			10:leaf=0.000625534
			9:[position=2] yes=16,no=15
				16:leaf=0.00066727
				15:leaf=0.000708484
	1:[browser=8] yes=4,no=3
		4:leaf=0.000881108
		3:[os_family=5] yes=8,no=7
			8:leaf=0.000842268
			7:[region=FR:A5] yes=14,no=13
				14:leaf=0.000939982
				13:leaf=0.000999001

Par exemple, la feuille 4 se traduit par la stratégie suivante: 
device_type! = Pc & browser! = 7 & browser = 8: 0.000881108

