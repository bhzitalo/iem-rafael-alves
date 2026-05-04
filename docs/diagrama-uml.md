# 📊 Diagrama UML (Classes)

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

Contato --> Visitante : fornece dados
````
