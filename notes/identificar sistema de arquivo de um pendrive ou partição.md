Para ver o sistema de arquivos de um pendrive no Linux, siga estes passos:

1. **Conecte o pendrive** ao seu computador.

2. **Abra um terminal**. Você pode fazer isso buscando "Terminal" no menu de aplicativos.

3. **Identifique o dispositivo**. Use o seguinte comando para listar todos os dispositivos de armazenamento conectados:

   ```bash
   lsblk
   ```

   Procure seu pendrive na lista (geralmente aparecerá como `/dev/sdb`, `/dev/sdc`, etc., dependendo de quantos dispositivos você tem).

4. **Verifique o sistema de arquivos**. Após identificar o dispositivo, você pode usar o comando `blkid` para ver o sistema de arquivos:

   ```bash
   sudo blkid /dev/sdX1
   ```

   Substitua `sdX1` pela identificação correta do seu pendrive.

5. **Opcional: montar o pendrive**. Se precisar acessar os arquivos, você pode montá-lo com:

   ```bash
   sudo mount /dev/sdX1 /mnt
   ```

   Depois, você pode acessar os arquivos na pasta `/mnt`.

6. **Desmontar o pendrive**. Quando terminar, não se esqueça de desmontar o dispositivo:

   ```bash
   sudo umount /mnt
   ```

E é isso! Assim você pode ver o sistema de arquivos do seu pendrive no Linux.