# documenta

# Como recuperar website de VPS

1. Habilitar el acceso root en la configuración abriendo
el archivo sshd_config con el comando:
```nano /etc/ssh/sshd_config```

2. Busca la línea que dice #PermitRootLogin ... o 
PermitRootLogin prohibit-password.Cámbiala para que quede
exactamente así:
```PermitRootLogin yes```

3. Guarda los cambios (Ctrl+O, luego Enter) y sal(Ctrl+X)
Para que el servidor "se entere" del cambio,debes 
reiniciarlo:
```systemctl restart ssh```

4. Halar el archivo desde tu máquina local(wsl2), abre
tu terminal de Ubuntu desde windows y ejecuta esto:
```scp -r root@179.50.90.170:~/teleporta-recovery/ ~/Escritorio/```

5. Un truco pro
```rsync -avzP root@179.50.90.170:~/teleporta-recovery/ ~/mis-archivos-recuperados/```

