# Utilização de Métodos Estatísticos e Ferramentas de Machine Learning na Apuração da Sensibilidade dos Patrimônios Líquidos dos Fundos de Investimentos aos Fatores de Risco

#### Aluno: [Jorge Alexandre Casara](https://github.com/sandwalker66).
#### Orientadores: [Manoela Kohler](https://github.com/manoelakohler) e [Leonardo Forero Mendoza](https://github.com/leofome8).

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

---

### Resumo


O objetivo do trabalho é o desenvolvimento de ferramenta que detecte erros informacionais sobre a sensibilidade dos fundos de investimento brasileiros aos fatores de risco Dólar, Ibovespa e Taxa Anual de Juros. Os administradores fiduciários dos fundos de investimento têm como obrigação reportar tais dados à CVM, e tratando-se de um universo que supera 15.000 carteiras, e sendo a periodicidade do envio de informação mensal, torna-se fundamental que tal ferramenta seja de fácil usabilidade e interpretabilidade.  
Demonstrou-se que os erros de informação da sensibilidade à variação da taxa de câmbio e variação do IBOVESPA dos fundos das classes Cambial e Ações são detectados por meio de regressões lineares simples, via algoritmos (em Python) que calculam o impacto de uma variação negativa de 1% no fator de risco sobre os ativos e derivativos cujo fator principal de risco seja a variação do dólar ou do IBOVESPA. Verifica-se que o coeficiente da regressão log-log é exatamente a sensibilidade procurada, para essas duas classes de fundos.
Para fundos de Renda Fixa, utilizou-se o módulo PORT da BLOOMBERG, que calcula o choque paralelo de 100 bps na curva de juros para todos os títulos da dívida pública, alguns títulos de crédito privado e contratos futuros de DI de 1 dia. Montando uma carteira teórica contendo tais ativos, construiu-se uma tabela com a variação percentual do valor de cada um, advinda de um choque paralelo de 100 bps na curva de juros. Utilizando scripts em Python, desdobrou-se as carteiras reais dos fundos de investimento do mercado brasileiro, em valor de mercado de cada ativo, mediu-se como cada ativo tem seu valor alterado pelo choque paralelo de 100 bps na curva de juros e somou-se a alteração de valor de todos os ativos da carteira: a soma é exatamente a sensibilidade esperada ao fator de risco “taxa de juros”, que será comparada à informada mensalmente pelo administrador fiduciário.
Desenvolveu-se uma interface com o pacote Streamlit, para que o usuário da ferramenta possa parametrizar seu uso de acordo com (i) os objetivos específicos da Ação de Fiscalização e (ii) a evolução do sistema BLOOMBERG, que futuramente abarcará outros ativos e derivativos além dos descritos acima, ampliando assim o quantitativo de carteiras sob escrutínio do analista. 

---

Matrícula: 191.671.043

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
