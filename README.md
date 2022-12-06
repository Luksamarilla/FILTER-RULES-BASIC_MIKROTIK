# FILTER-RULES-BASIC_MIKROTIK
FILTER RULES BASIC EVITAR PING FLOOD
/ip firewall filter
add chain=input comment="Aceita 30 mensagens ICMP por segundo" limit=30,5 protocol=icmp
add action=drop chain=input comment="Dropa todo ICMP" protocol=icmp
