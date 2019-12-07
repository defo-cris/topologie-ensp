in questa topologia si hanno 

- 2 switch
- 4 pc

sono state impostare 2 vlan (--> 2 e 3) per fare in modo che PC1 e PC3 siano direttamente connessi, PC2 e PC4 sono direttamente connessi. ma PC1 e PC2 sono in lan differenti --> vedi schema logico.



il collegamento tra i 2 switch e' di tipo trunk, quello con i pc di tipo access.

e' stata impostata la bpdu-filter per evitare che venissero inoltrate BPDU a gli host. 