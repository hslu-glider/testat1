# Datenstrukturen - trees
* Sie können einen Baum definieren. Sie können den Grad und die Höhe eines Baumes und das Niveau eines Knotens bestimmen. 
	*	tree (Baum):
	
			//Da in der Dokumentation teilweise unschön übersetzt wird, 
			//habe ich hier die englischen Schlüsselwörter verwendet.
			
			- Ein tree besteht aus nodes welche untereinander mit edges verbunden sind.
			- Besitzt ein tree keine nodes so ist er leer.
			- Wenn der tree, nodes besitzt so können diese vom Typ root, inner node oder leaf sein.
			- root bezeichnet dabei den ursprungs node
			- inner nodes sind nodes welche mindestens ein child node besitzen.
			- leaf ist ein node welche keine child nodes hat.
			- Ist ein node nach unten über edges mit anderen nodes verbunden, 
			  so sind diese unteren nodes die child's des höhergestellten node.
			- Der höher gestellte node wird auch parent genannt.
			
	* order (Ordnung) und degree (Grad):
	
			Order gibt an wieviele child nodes ein inner node höchstens haben darf.
			Degree gibt an wieviele child nodes ein node effektiv hat.
			
	* path (Pfad):
			
			Ein path von node "x" nach node "y" gibt an, welche edges und nodes besucht werden.
			
	* depth (Tiefe):
	
			Depth eines node "x" gibt an, wie lange der path zur root ist.
			
	* height (Höhe):
			
			Die height eines trees entspricht der depth des nodes welcher am weitesten von der root entfernt ist.
			
* Sie können die Funktionen insert(), print() und search() eines binären Suchbaumes implementieren.

	* Definition binary tree:
			
			Ein binary tree ist ein tree mit order = 2.
			
	* Definition binary search tree:
	
			Ein binary search tree hat die gleiche Struktur wie ein binary tree
			jedoch wird zu jedem node zusätzlich ein key vergeben.
			
	* search()
	
			//Diese Methode gibt true oder false zurück ob der node mit key = "k" gefunden wurde
			public bool search(Root r, Key k)
			{
				if(r != null)
				{	
					if(k < r.key)
					{
						search(r.left,k);
					}
					else
					{
						if(k > r.key)
						{
							search(r.right,k);
						}
						else
						{
							return true; //Suche war erfolgreich
						}
					}
				}
				else
				{
					return false; //Suche war erfolglos
				}
			}
			
	* insert()
	
			//
			public void insert(Root r, Key k)
			{
				if(r != null)
				{	
					if(k < r.key)
					{
						insert(r.left,k);
					}
					else
					{
						insert(r.right,k);
					}
				}
				else
				{
					add(k);
				}
			}
* Sie kennen das Prinzip des Löschens in einem binären Suchbaum.

	Beim löschen eines nodes müssen die Eigenschaften des binary search trees erhalten werden.
	Hierzu wird zwischen 3 Fällen unterschieden:
	
	* Fall 1: Der zu löschende node n ist ein leaf und hat demzufolge keine child nodes
		
		In diesem Fall wird der zu löschende node einfach gesucht und entfernt.
	
	* Fall 2: Der zu löschende node n ist ein inner node mit degree = 1
	
		In diesem Fall wird der zu löschende node gesucht, gelöscht und durch sine child node ersetzt.
		
	* Fall 3: Der zu löschende node n ist ein inner node mit degree = 2
	
		In diesem Fall muss nach dem löschen ein geeigneter nachfolge node gefunden werden.
		Dieser node wird mithilfe der inorder Reihenfolge gesucht und folgt auf den parent node des gelöschten node.
		
* Sie können einen AVL Baum definieren. 
