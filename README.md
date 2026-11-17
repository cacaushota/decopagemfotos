# decopagemfotos
comando para decopagem de fotos :D 
use esse prompt antes de rodar: 
Analise todas as fotos da pasta [CAMINHO_DA_PASTA] e faça a curadoria sem alterar nenhum arquivo original.

Regras de segurança e escopo:
- NÃO modifique, renomeie, mova ou exclua nada na pasta original. Use apenas leitura.
- NÃO tente criar pastas nem copiar arquivos diretamente na minha máquina. Sua entrega termina na lista selecionada e no código bash para eu executar no Terminal.
- Ignore arquivos de vídeo (.MOV, .MP4, etc.), mantendo-os intactos.

Etapa 1 — Verificação e leitura das imagens:
- Liste todos os arquivos da pasta.
- Se houver arquivos RAW (como .CR2), NÃO use `sips` diretamente (gera imagens pretas). Extraia o preview JPEG embutido (> 50 KB) para uma pasta temporária no seu workspace (ex: via Perl) antes de visualizar.
- Inspecione visualmente 100% das imagens em lotes.

Etapa 2 — Agrupamento e seleção:
- Agrupe as fotos por tema, cenário e elemento/objeto principal da cena (ex: o que a pessoa está segurando, pose ou ação).
- Descarte fotos com olhos fechados, tremido/desfoque, subexposição severa, obstruções (ex: tripé/objetos na frente) ou enquadramento ruim.
- De cada grupo idêntico ou muito parecido, selecione no máximo 2 a 3 fotos utilizáveis (as melhores em nitidez, expressão e composição) para evitar repetição.
- Classifique todas as fotos restantes como não utilizáveis/redundantes.

Etapa 3 — Entrega:
Entregue apenas:
1. A lista das fotos selecionadas agrupadas por tema (com os nomes exatos dos arquivos) e o resumo numérico (total analisado, selecionadas e descartadas/redundantes).
2. Um script bash pronto para copiar e colar no Terminal do macOS que crie as subpastas `01_UTILIZAVEIS` e `02_NAO_UTILIZAVEIS` dentro da pasta original e copie (`cp -p`) cada arquivo para sua respectiva pasta, mantendo os originais intactos.

