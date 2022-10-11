<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# Manual de implementação
O segundo módulo incidirá sobre a instalação do JuezLTI e a sua integração no LMS das instituições de ensino. Embora o consórcio ofereça, durante a execução do projecto, uma plataforma gratuita para a sua utilização (JuezLTI-central), JuezLTI foi concebido para permitir a instalação nos servidores de qualquer instituição que a queira adoptar.

Esta tarefa será realizada principalmente pela [EdF](http://www.edf.global/), uma vez que são especialistas na integração de ferramentas educativas e serão eles que levarão a cabo o desenvolvimento do _container_ Docker.

Graças a este _container_ Docker, JuezLTI permitirá uma instalação simples e modular, permitindo a cada instituição configurar facilmente os módulos (programação / bases de dados / linguagens de marcação) a serem instalados nos seus servidores ou a sua instalação distribuída na nuvem, através de fornecedores de serviços de computação em nuvem.

Tudo isto será definido no segundo módulo através das secções seguintes:
- Instalação do JuezLTI no local
- Implementação do JuezLTI na nuvem
- Configuração do JudgeLTI
- Comunicação entre JuezLTI e o LMS
- Integração de repositórios de exercícios


# Manual de desenvolvimento
JuezLTI será lançado com uma licença Apache 2.0, permitindo a qualquer instituição ou programador expandir as funcionalidades da ferramenta, adaptando-a às particularidades da instituição. É necessário um manual específico para facilitar a tarefa de programação. 

Este manual será desenvolvido principalmente pelo [INESC TEC](http://www.inesctec.pt/), e será constituído pelas secções seguintes:
- [O _standard_ LTI](Development/LTI/README_pt.md)
- [Arquitetura do JuezLTI](Development/Architecture/README_pt.md)
- Desenvolvimento de módulos com TSUGI
- [API Interno](Development/API/README_pt.md)
- Desenvolvimento de clientes JuezLTI
- Desenvolvimento de exercícios com JuezLTI
