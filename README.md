# Central de Software VIP

Central em HTML puro para disponibilizar downloads de softwares Windows e macOS usando links do SharePoint.

## Como funciona

- O site fica no GitHub Pages ou intranet.
- Os instaladores ficam no SharePoint.
- Cada botão de download aponta para o link individual do arquivo no SharePoint.
- Não é necessário subir `.exe`, `.dmg` ou `.pkg` no GitHub.

## Estrutura

```text
central-software-vip/
  index.html
  README.md
  .gitignore
  assets/
    img/
```

## Publicar no GitHub

```powershell
git add .
git commit -m "Atualiza central com links do SharePoint"
git push -u origin main --force
```

Se o repositório já tiver histórico com arquivos grandes, recrie o histórico limpo:

```powershell
git checkout --orphan clean-main
git rm -r --cached . 2>$null
git add .
git commit -m "Publica central VIP usando links do SharePoint"
git branch -M main
git push -u origin main --force
```

## Observação

Os links do SharePoint precisam estar liberados para o público correto, por exemplo: pessoas da organização com o link.
