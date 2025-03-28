<h1 align="center">Curriculum</h1>
<p align="center">Repositório para o trabalho de a disciplina de DESENVOLVIMENTO DE APLICAÇÕES PARA DISPOSITIVOS MÓVEIS</p>
<p align="center">
<img loading="lazy" src="https://img.shields.io/static/v1?label=EST%C3%81GIO%20DE%20DESENVOLVIMENTO&message=INICIAL&color=red&style=for-the-badge"/>

<h1>Objetivo do projeto</h1>
O objetivo do projeto consiste na construção de uma plataforma centralizada que facilite o compartilhamento, a hospedagem e a visualização de currículos. A plataforma visa eliminar as dificuldades enfrentadas tanto por empregadores quanto por candidatos, oferecendo uma solução que permite acessar, manusear e compartilhar currículos de forma eficiente.

<h1>Itens que não serão implementados</h1>
<ul>
    <li>Um portal de vagas de emprego completo com sistema de candidaturas complexo.</li>
    <li>Uma ferramenta de Recrutamento e Seleção com funcionalidades avançadas de triagem automática.</li>
    <li>Sistema de contratação automatizada.</li>
    <li>Substituição completa de entrevistas ou processos seletivos.</li>
</ul>

<h1>Público-alvo</h1>
O público-alvo do aplicativo inclui:
<ul>
    <li><strong>Profissionais/Candidatos:</strong> Indivíduos que desejam criar, hospedar, gerenciar e compartilhar seus currículos de modo prático e centralizado.</li>
    <li><strong>Empregadores/Recrutadores:</strong> Empresas e profissionais de RH que buscam uma maneira eficiente de encontrar, visualizar e organizar currículos de potenciais candidatos.</li>
</ul>

<h1>Requisitos funcionais</h1>
<ul>
    <li><strong>Registro e Autenticação de Usuários:</strong> Sistema de cadastro e login diferenciado para Candidatos e Empregadores, permitindo a criação e autenticação.</li>
    <li><strong>Gerenciamento de Perfil:</strong> Permite aos usuários editar suas informações básicas de perfil.</li>
    <li><strong>CRUD de Currículos:</strong></li>
    <ol>
        <li><strong>Criação:</strong> Permitir que candidatos criem seus currículos preenchendo seções como Dados Pessoais, Resumo Profissional, Experiência Profissional, Formação Acadêmica, Habilidades, Projetos, etc. (Possibilidade de adicionar/remover seções customizadas).</li>
        <li><strong>Leitura:</strong> Visualização do próprio currículo.</li>
        <li><strong>Atualização:</strong> Edição das informações do currículo a qualquer momento.</li>
        <li><strong>Deleção:</strong> Exclusão do currículo.</li>
    </ol>
    <li><strong>Compartilhamento de Currículo:</strong> Geração de um link compartilhável e seguro para o currículo hospedado na plataforma. Controle de privacidade (ex: público, privado, apenas com link).</li>
    <li><strong>Busca e Visualização de Currículos:</strong></li>
    <ol>
        <li><strong>Busca:</strong> Permitir que empregadores e recrutadores pesquisem currículos na plataforma utilizando filtros (ex: palavras-chave, habilidades, anos de experiência).</li>
        <li><strong>Visualização:</strong> Apresentação clara e organizada dos currículo​s encontrados.</li>
    </ol>
</ul>

<h1>Requisitos não funcionais</h1>
<ul>
    <li><strong>Desempenho:</strong> O aplicativo deve funcionar de modo fluído, sem travamentos e com tempos de resposta rápidos para criação, busca e visualização de CVs.</li>
    <li><strong>Segurança:</strong> Garantir a proteção dos dados pessoais dos candidatos e das informações das contas dos empregadores. Acesso restrito aos dados conforme os níveis de permissão e privacidade.</li>
    <li><strong>Disponibilidade:</strong> Alta disponibilidade da plataforma para acesso a qualquer momento.</li>
    <li><strong>Escalabilidade:</strong> Capacidade de lidar com um número crescente de usuários e CVs sem degradação do desempenho.</li>
    <li><strong>Compatibilidade:</strong> O aplicativo deve ser desenvolvido preferencialmente para múltiplas plataformas (Android, iOS e/ou Web).</li>
</ul>

<h1>Modelagem do Banco de Dados</h1>
<img src="https://github.com/user-attachments/assets/3f582bce-081c-4353-a3a8-da791ca82ad2" width=50% height=50%>

<h1>Dicionário de Dados</h1>

<h2>Coleção: Usuários</h2>
<ul>
    <li><strong>uid</strong>: atributo do tipo INTEGER.</li>
    <li><strong>email</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>senha</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>fotoURL</strong>: atributo do tipo VARCHAR.</li>
</ul>

<h2>Coleção: Currículos</h2>
<ul>
    <li><strong>cid</strong>: atributo do tipo INTEGER.</li>
    <li><strong>uid</strong>: atributo do tipo INTEGER.</li>
    <li><strong>introdução</strong>: atributo do tipo VARCHAR.</li>
</ul>

<h2>Subcoleção: Informações Pessoais</h2>
<ul>
    <li><strong>id</strong>: atributo do tipo INTEGER.</li>
    <li><strong>cid</strong>: atributo do tipo INTEGER.</li>
    <li><strong>nome</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>idade</strong>: atributo do tipo INTEGER.</li>
    <li><strong>email</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>telefone</strong>: atributo do tipo VARCHAR.</li>
</ul>

<h2>Subcoleção: Experiência Profissional</h2>
<ul>
    <li><strong>id</strong>: atributo do tipo INTEGER.</li>
    <li><strong>cid</strong>: atributo do tipo INTEGER.</li>
    <li><strong>empresa</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>posição</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>data_início</strong>: atributo do tipo TIMESTAMP.</li>
    <li><strong>data_término</strong>: atributo do tipo TIMESTAMP.</li>
    <li><strong>descrição</strong>: atributo do tipo VARCHAR.</li>
</ul>

<h2>Subcoleção: Educação</h2>
<ul>
    <li><strong>id</strong>: atributo do tipo INTEGER.</li>
    <li><strong>cid</strong>: atributo do tipo INTEGER.</li>
    <li><strong>instituição</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>grau</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>área</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>data_início</strong>: atributo do tipo TIMESTAMP.</li>
    <li><strong>data_término</strong>: atributo do tipo TIMESTAMP.</li>
</ul>

<h2>Subcoleção: Projetos</h2>
<ul>
    <li><strong>id</strong>: atributo do tipo INTEGER.</li>
    <li><strong>cid</strong>: atributo do tipo INTEGER.</li>
    <li><strong>título</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>descrição</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>link</strong>: atributo do tipo VARCHAR.</li>
    <li><strong>tecnologias</strong>: atributo do tipo VARCHAR.</li>
</ul>

<h1>Diagramas UML</h1>
<h2>Diagrama de Classes</h2>
<img src="https://github.com/user-attachments/assets/c1bed530-0eb2-4bda-b4bd-1574b944d66e" width=50% height=50%>

<h2>Diagrama de Objetos</h2>
<img src="https://github.com/user-attachments/assets/a050fb79-65be-4779-bcbb-5568090fc034" width=50% height=50%>

<h2>Diagrama de Componentes</h2>
<img src="https://github.com/user-attachments/assets/c3d824ee-30e0-4d60-a85c-41cf5ee623d8" width=50% height=50%>

<h2>Diagrama de Caso de Uso</h2>
<img src="https://github.com/user-attachments/assets/454fa404-17c7-4c6e-a87d-e1786c0370ef" width=50% height=50%>

<h2>Diagrama de Sequência</h2>
<img src="https://github.com/user-attachments/assets/fb1dbb4c-be5a-49b0-9ce5-016131c92e9e" width=50% height=50%>

<h2>Diagrama de Atividade</h2>
<img src="https://github.com/user-attachments/assets/f12a2bbc-fa32-484f-a2fe-4aa25294700d" width=50% height=50%>

<h1>Tecnologias Empregadas</h1>
<img src="https://github.com/user-attachments/assets/a176618e-65a7-4b22-b43d-0afd7546b01d" width=50% height=50%>
