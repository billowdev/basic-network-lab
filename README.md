# basic-network-lab

<pre>
1. enable  # เปิดใช้งาน switch
2. configure terminal # เชื่อมต่อterminal
3. vlan 14 # สร้าง vlan เป็นหมายเลข 14
	status -> switch(config-vlan)
4. name cs63 
5. exit # กลับสู่สถานะ cofig
status -> switch(config)
6. interface fastEthernet0/5
 # access to fa0/5 for set vlan
	status -> Switch(config-if)
7. switchport access vlan 14
	#add port fa0/5 to vlan 
8. exit
9. exit
10. show vlan

result
Switch#show vlan

VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/6, Fa0/7, Fa0/8, Fa0/9
                                                Fa0/10, Fa0/11, Fa0/12, Fa0/13
                                                Fa0/14, Fa0/15, Fa0/16, Fa0/17
                                                Fa0/18, Fa0/19, Fa0/20, Fa0/21
                                                Fa0/22, Fa0/23, Fa0/24
10   CS                               active    Fa0/1
11   IT                               active    Fa0/2
12   Akkarapon                        active    Fa0/3
13   game                             active    Fa0/4
14   cs63                             active    Fa0/5
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    

VLAN Type  SAID       MTU   Parent RingNo BridgeNo Stp  BrdgMode Trans1 Trans2
---- ----- ---------- ----- ------ ------ -------- ---- -------- ------




# การ ลบ vlan

1. enable
2. configure terminal
3. no vlan 14
4. exit 
5. show vlan


-------------------- result ---------------------------
VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/6, Fa0/7, Fa0/8, Fa0/9
                                                Fa0/10, Fa0/11, Fa0/12, Fa0/13
                                                Fa0/14, Fa0/15, Fa0/16, Fa0/17
                                                Fa0/18, Fa0/19, Fa0/20, Fa0/21
                                                Fa0/22, Fa0/23, Fa0/24
10   CS                               active    Fa0/1
11   IT                               active    Fa0/2
12   Akkarapon                        active    Fa0/3
13   game                             active    Fa0/4
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    

VLAN Type  SAID       MTU   Parent RingNo BridgeNo Stp  BrdgMode Trans1 Trans2
---- ----- ---------- ----- ------ ------ -------- ---- -------- ------ ------
1    enet  100001     1500  -      -      -        -    -        0      0
10   enet  100010     1500  -      -      -        -    -        0      0
11   enet  100011     1500  -      -      -        -    -        0      0

</pre>
