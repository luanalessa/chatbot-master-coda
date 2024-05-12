
# <p align = "center"> Jornada Jedi: Chat com o Mestre Coda 🖖 </p>
<p align = "center">
<img src="https://img.shields.io/badge/author-luanalessa-4dae71?style=flat-square" />
 <img src="https://img.shields.io/github/languages/count/luanalessa/chatbot-master-coda?color=4dae71&style=flat-square" />

</br>
<br/>
<p align="center"><img src="https://github.com/luanalessa/chatbot-master-coda/assets/72531277/74718754-8ff9-4f8e-a788-78f477b5b92f"/></p>

</br>

## Descrição
Saudações, jovem Padawan! Este é o Chat com o Mestre Coda, uma ferramenta desenvolvida na galáxia do Google Colab, utilizando a mística biblioteca google-generativeai. Nesta jornada, você poderá interagir com o lendário Mestre Coda, que guiará seus estudos através da Força.

## Como funciona?

Vamos manter uma conversa para construir seu roteiro de estudo Jedi personalizado!

Primeiro, diga-me o que você deseja aprender sobre Python.

- Fundamentos da Força: Domine os conceitos básicos e sinta a sintaxe de alguma linguagem de programação.
- Caminho do Jedi Intermediário: Aprofunde seus conhecimentos e explore estruturas de dados e módulos.
- Lorde Sith Avançado: Domine as técnicas avançadas e torne-se um mestre em Python.

Após escolher seu caminho, prepare-se para receber um roteiro de estudo Jedi completo!

Que a Força te guie durante a sua jornada!

## Instalação e Configuração
Para iniciar sua jornada, primeiro, você precisa instalar as ferramentas necessárias. No terminal da sua nave, execute o comando a seguir:

```bash
!pip install -q -U google-generativeai
```

Em seguida, sincronize sua mente com a Força e configure sua API key Jedi:

```python
import google.generativeai as genai
from google.colab import userdata

GOOGLE_API_KEY = userdata.get('GOOGLE_API_KEY')
genai.configure(api_key=GOOGLE_API_KEY)
```

## Iniciando a Jornada
Agora que suas ferramentas estão prontas, prepare-se para iniciar sua jornada Jedi. Execute o código abaixo para receber as bênçãos do Mestre Coda:

``` python
generation_config = {
    "candidate_count": 1,
    "temperature": 0.75
}

safety_settings = {
    "HARASSMENT": "BLOCK_ONLY_HIGH",
    "HATE": "BLOCK_ONLY_HIGH",
    "SEXUAL": "BLOCK_ONLY_HIGH",
    "DANGEROUS": "BLOCK_ONLY_HIGH"
}

model = genai.GenerativeModel(
    model_name="gemini-1.0-pro",
    generation_config=generation_config,
    safety_settings=safety_settings
)

print("Bem-vindo, Padawan! Eu sou o Mestre Coda, e estou aqui para guiá-lo na jornada de aprendizado. Que a Força esteja com você!")

request = input("Primeiro, diga-me o que você deseja aprender.")
```

## Explorando o Conhecimento
Agora é a sua vez, jovem Padawan. Diga-me qual é o seu desejo de aprendizado, e eu, o Mestre Coda, irei compartilhar com você um roadmap Jedi para o conhecimento desejado:

```python
prompt = f"Desenvolver um guia de estudo Jedi para o tópico: {request}. Este guia deve compreender uma variedade de recursos, tais como cursos, artigos, vídeos gratuitos e exercícios, que ofereçam uma abordagem completa e organizada sobre o assunto. Quanto mais detalhado e diversificado for o guia, melhor! A resposta deve ser dividida em níveis de iniciante, intermediário e avançado, cada um com conteúdos pertinentes ao respectivo nível. Os níveis devem ser nomeados de forma apropriada ao tema."

response = model.generate_content(prompt)
print(response.text)
```

## Considerações Finais
Que a Força esteja com você em sua jornada, jovem Padawan. Que este chat com o Mestre Coda seja uma ferramenta valiosa em sua busca pelo conhecimento Jedi. Lembre-se sempre: o aprendizado é uma jornada eterna, e a sabedoria está dentro de você.

Que tal? Pronto para embarcar em sua jornada Jedi?
