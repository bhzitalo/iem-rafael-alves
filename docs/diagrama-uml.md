````md id="umlclass02"
# 📊 Diagrama UML (Classes) - Baseado nos Casos de Uso

## 📌 Descrição
Este diagrama de classes representa a estrutura do sistema com base nas ações do usuário (Visitante), conforme definido no diagrama de casos de uso.

## 🧩 Diagrama (Mermaid)

```mermaid
classDiagram

class Visitante {
  +visualizarPaginaInicial()
  +visualizarSobre()
  +visualizarCursos()
  +entrarEmContato()
  +navegarMenu()
}

class Site {
  -nome: string
  -url: string
  +carregarPagina()
}

class Menu {
  +exibirMenu()
  +redirecionar()
}

class Pagina {
  -titulo: string
  -conteudo: string
  +renderizar()
}

class Home {
  +mostrarApresentacao()
}

class Sobre {
  +mostrarInformacoes()
}

class Cursos {
  +listarCursos()
}

class Contato {
  +exibirFormulario()
  +enviarMensagem()
}

class Curso {
  -nome: string
  -descricao: string
  -nivel: string
}

class Professor {
  -nome: string
  -especialidade: string
  -experiencia: string
}

Visitante --> Menu : utiliza
Visitante --> Site : acessa

Site "1" --> "*" Pagina : contém

Pagina <|-- Home
Pagina <|-- Sobre
Pagina <|-- Cursos
Pagina <|-- Contato

Cursos --> "*" Curso : exibe
Professor --> "*" Curso : ministra

Contato --> Visitante : recebe dados
````

```
```
