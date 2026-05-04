````md
# 🎭 Diagrama de Casos de Uso - Sistema do Professor Rafael Alves

## 📌 Descrição
Este diagrama representa as interações entre os usuários e o sistema do site institucional do professor de música.

## 👤 Atores

- Visitante (usuário do site)

## 🎯 Casos de Uso

- Visualizar página inicial  
- Visualizar página sobre  
- Visualizar cursos  
- Entrar em contato  
- Navegar pelo menu  

## 🧩 Diagrama (Mermaid)

```mermaid
usecaseDiagram

actor Visitante

Visitante --> (Visualizar Página Inicial)
Visitante --> (Visualizar Página Sobre)
Visitante --> (Visualizar Cursos)
Visitante --> (Entrar em Contato)
Visitante --> (Navegar pelo Menu)

(Navegar pelo Menu) ..> (Visualizar Página Inicial) : <<include>>
(Navegar pelo Menu) ..> (Visualizar Página Sobre) : <<include>>
(Navegar pelo Menu) ..> (Visualizar Cursos) : <<include>>
(Navegar pelo Menu) ..> (Entrar em Contato) : <<include>>
````
