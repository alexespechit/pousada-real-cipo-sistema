# Pousada Real Cipó — Sistema de Reservas

Sistema web de gestão interna para uma pousada: cadastro de clientes e unidades, controle de reservas e geração de documento em PDF para o hóspede.

> 🔒 **Código-fonte privado.** Este repositório é uma vitrine do projeto (descrição, tecnologias e funcionalidades). Se quiser saber mais, é só entrar em contato.

## O problema

Controlar reservas, datas de check-in/check-out e valores em anotações e planilhas gera conflitos de datas e retrabalho. O sistema centraliza tudo em um painel único.

## Funcionalidades

- **Login** com autenticação JWT e cookies httpOnly, com rotas protegidas por middleware
- **Dashboard** com métricas e próximos check-ins e check-outs
- **Clientes**: cadastro completo e histórico de reservas
- **Unidades**: cadastro com status e valor da diária
- **Reservas**:
  - prevenção de conflito de datas
  - cálculo automático do valor total
  - fluxo de status (Pendente → Confirmada → Concluída / Cancelada)
- **Documento em PDF** da reserva, gerado no sistema, com nome, endereço, regras e rodapé configuráveis
- **Página de impressão** otimizada para o navegador
- **Formulário de hóspedes** e pré-reservas

## Tecnologias

| Camada | Tecnologia |
| --- | --- |
| Framework | Next.js 14 (App Router) |
| Linguagem | TypeScript |
| Estilo | Tailwind CSS |
| Banco de dados | PostgreSQL + Prisma ORM |
| Formulários e validação | React Hook Form + Zod |
| PDF | @react-pdf/renderer |
| Autenticação | JWT (jose) + bcrypt |

## Organização do projeto

Arquitetura em camadas: *services* (acesso a dados com Prisma), *server actions* (mutações), *validations* (schemas Zod) e componentes reutilizáveis separados por domínio (clientes, unidades, reservas, PDF).

## Próximos passos planejados

- Calendário visual de disponibilidade
- Relatórios de ocupação e receita
- Notificações por e-mail de check-in/check-out
- Autenticação multiusuário

---

Feito por [Alexsander Espechit](https://github.com/alexespechit) · [LinkedIn](https://www.linkedin.com/in/alexsanderespechit/)
