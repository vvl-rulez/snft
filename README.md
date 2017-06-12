# Скрипт для простого управления firewall на базе nftables.
***
### Использование: 
```
snft [команда] [параметры]
Доступные команды:
    -b,  --block          заблокировать IP-адрес,
         [IP-адрес1] [IP-адрес2] ...
    -u,  --unblock        разблокировать IP-адрес,
         [IP-адрес1] [IP-адрес2] ...
    -ba, --block-all      заблокировать все соединения, кроме текущего IP,
         -f, --force      не запрашивать подтверждение для действий,
    -d,  --ddos           найти и заблокировать соединения с IP-адресами, с которыми превышено указанное количество соединений,
         -f, --force      не запрашивать подтверждение для действий,
         [2-∞]            количество соединений с IP-адресом, выше которого IP-адрес считается атакующим,
    -l,  --list           список заблокированных IP-адресов,
    -rr, --reset-rules    сбросить правила snft,
         -f, --force      не запрашивать подтверждение для действий,
         -b, --block      удалить правила с заблокированными вручную IP-адресами,
         -ba, --block-all удалить правило blockall,
         -d,  --ddos      удалить правила, созданные параметром ddos,
         -a,  --all       удалить все правила snft
    -h,  --help         показать справку.
    ```
