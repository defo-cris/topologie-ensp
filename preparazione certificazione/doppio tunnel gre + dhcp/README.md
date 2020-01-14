le reti usate sono tutte 192.168

- 0.0 /24 --> host
- 1.0 /24 --> host
- 2.0 /24 --> host
- 3.0 /24 --> host
- 4.0 /24 --> host
- 5.0 /29 --> ha ancora qualche ip disponibile
- 5.8 /30  --> full
- 5.12 /30 --> full
- 5.16 /30 --> full

in questa topologia sono presenti

- 2 tunnel gre
  - tunnel 0/0/2 = da R1 ge1 --> 192.168.1.0 /24 a R3 ge1 192.168.3.0 /24 
    passando per la rete 192.168.5.16 /30 (il tunnel)
    in R1 il tunnel ha ip 5.17
    in R3 il tunnel ha ip 5.18
  - tunnel 0/0/1 = da 192.168.0.0 /24 a 192.168.2.0 /24
    il tunnel e' la rete 162.168.5.12 (vedi foto per ip)
- ospf in running nelle reti
  - 5.8 /30 --> rete tra r1 e r4 
    network type p2p
  - 5.0 /29 --> tra r4 r3 r2
  - 4.0 /24 --> dedicata a host pc6 pc7
- dhcp in running su R4 interfaccia gig 0/0/1 rete 4.0







BISOGNA SISTEMARE PC8 PERCHE' DA FASTIDIO --> POSSIBILMENTE NATTARLO

inoltre e' da sistemare che 

1. pc1 deve poter comunicare con pc6, pc7 e pc8 fuori dal tunnel
2. pc2 solo nel tunnel
3. pc3 solo fuori dal tunnel

DA FARE OVVIAMENTE CON LE ACL!

