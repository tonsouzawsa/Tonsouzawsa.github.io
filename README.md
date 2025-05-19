# Aplicativo de Orçamento de Obra - WSA Construções

Este é um aplicativo web simples desenvolvido para gerar orçamentos de obras diretamente do celular ou computador. Criado por Wellington da WSA Construções, o app permite simular os custos de construção de forma prática e profissional.

## Funcionalidades

- Inserção da localização e tipo de obra
- Informar área da construção
- Seleção de serviços como:
  - Limpeza
  - Fundação
  - Estrutura
  - Elétrica
  - Acabamento
- Inserção de valores para materiais e mão de obra
- Cálculo automático do orçamento total
- Divisão das formas de pagamento: 30% início, 40% durante, 30% entrega
- Exibição da missão, visão e valores da empresa
- Inclusão da logomarca no topo

## Missão

Oferecer soluções em construção civil com excelência, atendendo às necessidades dos nossos clientes com qualidade e pontualidade.

## Visão

Ser reconhecida como referência em inovação e sustentabilidade no setor da construção civil.

## Valores

- Compromisso  
- Qualidade  
- Transparência  
- Respeito  

## Acesso

Você pode abrir o arquivo `index.html` localmente no navegador ou acessar o site publicado no GitHub Pages (após subir o arquivo):

**Exemplo:**  
[https://seu-usuario.github.io](https://seu-usuario.github.io)

(Substitua `seu-usuario` pelo seu nome de usuário do GitHub)

## Autor

Desenvolvido por **Wellington**, fundador da **WSA Construções**.
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Teste PDF</title>
</head>
<body>
  <h1>Gerador de Orçamento</h1>

  <textarea id="texto" rows="10" cols="50">Digite aqui o conteúdo do orçamento...</textarea><br><br>
  <button onclick="gerarPDF()">Salvar em PDF</button>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script>
    function gerarPDF() {
      const { jsPDF } = window.jspdf;
      const texto = document.getElementById("texto").value;
      const doc = new jsPDF();
      doc.text(texto, 10, 10);
      doc.save("orcamento_teste.pdf");
    }
  </script>
</body>
</html>

