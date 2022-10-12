<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# Interoperabilidade

JuezLTI utiliza a versão 1.0 do _standard_ de interoperabilidade de ferramentas de aprendizagem (LTI) para a integração no LMS. 
Este _standard_ de interoperabilidade foi proposta pelo IMS Global Learning Consortium \cite{lti2010}. 
e é suportado por vendedores de LMS de referência como Moodle, Canvas, ou Sakai.

Com o LTI, pode ser utilizado um conjunto de serviços educativos para alargar a funcionalidade do LMS utilizando uma Arquitectura Orientada para Serviços (SOA). 
O LMS torna-se um mercado onde o professor pode seleccionar os recursos de diferentes fornecedores para melhorar a experiência de aprendizagem. 

JuezLTI é baseado em TSUGI, uma _framework_ que simplifica o desenvolvimento e implementação de aplicações LTI. 
A primeira aplicação do TSUGI foi um MOOC autónomo para formação em Python -- py4e.com. 
Foi implementado por um dos seus autores, Dr. Charles Severance, fundador do LMS Open Source Sakai e trabalha actualmente para o IMS.
LTI tem sido utilizado amplamente desde 2010, não apenas para testes de código mas também para fornecer avaliações complexas não suportadas directamente pelo LMS, como o Dig4E, uma ferramenta para aprender sobre _standards_ para 
criação de imagens estáticas digitais de alta qualidade. 

Para utilizar o JuezLTI, o professor tem de solicitar um par chave/segredo na página web do projecto. 
O professor acrescenta uma actividade externa no LMS com essas credenciais e o URL fornecido. 
Os alunos são directamente identificados no JuezLTI utilizando a informação fornecida pelo LMS. 
Sempre que um estudante ou professor abre a actividade, o LMS comunica com o JuezLTI utilizando o LTI (através da _framework_ TSUGI) para identificar o utilizador e apresentar a interface apropriada. Depois, o LMS envia a propriedade <code>resource_link_id</code> identificando a actividade relevante. 
Desta forma, diferentes actividades podem ser acrescentadas usando a mesma chave. Finalmente, o JuezLTI reporta as notas dos exercícios resolvidos de volta ao LMS utilizando um serviço LTI.

Em suma, existe comunicação bidireccional entre o JuezLTI e o LMS. 
O JuezLTI armazena a informação dos estudantes e os seus resultados e envia as notas obtidas de volta para o LMS. 
