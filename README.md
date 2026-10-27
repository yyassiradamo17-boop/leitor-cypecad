# Leitor CYPECAD

Ferramenta web que lê as listagens exportadas do CYPECAD e transforma-as em dados limpos, verificação EC2 e memória de cálculo. Corre inteiramente no navegador: os ficheiros que arrasta para a página não saem do computador.

## O que faz

1. **Importar** listagens do CYPECAD em HTML, PDF (com texto), DOCX, RTF, TXT, XLSX/XLS/ODS, CSV ou ODT.
2. **Reconhecer** as tabelas: elemento, planta, combinação ou hipótese, posição, N, Mx, My, Qx, Qy, T, armaduras, geometria e medições, com conversão de unidades.
3. **Estruturar** os dados, exportáveis em JSON (sessão), Excel ou CSV.
4. **Usar** os dados:
   - envolventes e valores críticos por elemento;
   - verificação independente EC2 (vigas, pilares em flexão desviada, punçoamento, sapatas, muros por metro), com diferenças acima da tolerância assinaladas;
   - quantidades (betão, cofragem, aço por diâmetro) por bloco ou revisão;
   - comparação entre revisões;
   - memória de cálculo em HTML, PDF ou Word (.docx).

## Experimentar

Abra o site e use **Carregar exemplo (2 revisões)**, ou arraste os ficheiros da pasta [`exemplos/`](exemplos). São listagens fictícias, geradas ao estilo do CYPECAD.

## Notas

- Precisa de ligação à Internet para as bibliotecas de PDF (pdf.js), Excel (SheetJS) e ZIP (JSZip), servidas pela cdnjs.
- Os resultados da verificação independente são de apoio ao projecto e devem ser confirmados pelo projectista. Os efeitos de 2.ª ordem em pilares não estão incluídos.
- Os botões de envio abrem as calculadoras publicadas já preenchidas com os esforços:
  - [Dimensionamento BA · EC2](https://yyassiradamo17-boop.github.io/EC2BAMosley.html/)
  - [Seletor de Armaduras](https://yyassiradamo17-boop.github.io/Seletor-de-armaduras/)

  Os endereços podem ser alterados em **Definições › Ligação às ferramentas**. O navegador tem de permitir janelas pop-up para o leitor.
