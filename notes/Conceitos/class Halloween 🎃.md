---
keywords:
---

**Keywords**
- cluster
- alocação
- setor
- FAT
- arquivo
- metadados

# Utilitário de depuração
-> Acessa infos de inode e bloco de dados
```bash
$ sudo debugfs /dev/sda2
```

```
debugfs: stat ~/arquivo.extensao
```

> [!tip] Interessante

Os CD-ROMs utilizam alocação contígua [[alocação contígua complemento]]

# FAT (File Alocation Table)
![[Pasted image 20241031075953.png]]
-> FAT 5 = 2^5 = 32 lugares para endereçar blocos
-> FAT 16 = 2^16 = 65.536 posições
**Limitações**
- FAT NÃO tem permissão
- FAT não pode ter um arquivo único que ultrapasse 4GB
- Corrupções (pode ter dados sem inode ou inode sem dados)
-> Pendrive geralmente é FAT32
	NTFS
	FAT32
	exFAT

> [!important] Interessante

O Slack space pode chegar a 25% da capacidade total do HD!

![[Pasted image 20241031080202.png]]

-> aprenda a [[identificar sistema de arquivo de um pendrive ou partição]]
-> **fsck** = lost and found (achados e perdidos)
# Journaling filesystems
-> journaling e rollback = log e recuperação (filesystems jornalados)
-> NTFS é jornalado
-> todos sistemas de arquivos atuais são jornalados (segura integridade dos dados)
![[Pasted image 20241031082429.png]]

![[Pasted image 20241031082447.png]]

**para ver o jornal faça**
```
debugfs: logdump -a
```
-> de tempos em tempos o kernel faz sincronização do jornal para sistema de arquivo (flush)

---
**Final de dec90**
Microsoft largou ms-dos e apostou no núcleo NT (New Technology) = NTFS -> substituiu FAT
**NTFS** é sistema de arquivos indexado
