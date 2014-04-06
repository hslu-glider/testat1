# Datenstrukturen - trees
* Sie können einen Baum definieren. Sie können den Grad und die Höhe eines Baumes und das Niveau eines Knotens bestimmen. 
	*	Definition eines Baumes:
	
			//Da in der Dokumentation teilweise unschön übersetzt wird, 
			//habe ich hier die englischen Schlüsselwörter verwendet.
			
			- Ein tree besteht aus nodes welche untereinander mit edges verbunden sind.
			- Besitzt ein tree keine nodes so ist er leer.
			- Wenn der tree, nodes besitzt so können diese vom Typ root, inner node oder leaf sein.
			- Root bezeichnet dabei den ursprungs node
			- inner nodes sind nodes welche mindestens ein child node besitzen.
			- leaf ist ein node welche keine child nodes hat.
			- Ist ein node nach unten über edges mit anderen nodes verbunden, 
			  so sind diese unteren nodes die child's des höhergestellten node.
			- Der höher gestellte node wird auch parent genannt.
			
	* Die order (Ordnung) und degree (Grad):
	
			Order gibt an wieviele child nodes ein inner node höchstens haben darf.
			Degree gibt an wieviele child nodes ein node effektiv hat.
			
	* Path (Pfad):
			
			Ein path von node "x" nach node "y" gibt an, welche edges und nodes besucht werden.
			
	* Depth (Tiefe):
	
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
				if(r!=null)
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
				if(r!=null)
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
					add(r,k);
				}
			}
* Sie kennen das Prinzip des Löschens in einem binären Suchbaum. 
* Sie können einen AVL Baum definieren. 
