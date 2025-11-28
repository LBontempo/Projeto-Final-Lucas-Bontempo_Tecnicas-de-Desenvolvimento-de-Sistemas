INÍCIO

    // -------------------------------------------
    // 1. ESTABELECER CONEXÃO COM O BANCO
    // -------------------------------------------
    CHAMAR função conectarBanco()
    SE conexão falhar ENTÃO
        EXIBIR "Erro ao conectar ao banco."
        ENCERRAR programa
    FIMSE

    // -------------------------------------------
    // 2. EXIBIR MENU PRINCIPAL
    // -------------------------------------------
    REPITA
        EXIBIR "=== MENU PRINCIPAL ==="
        EXIBIR "1 - Gerenciar Clientes"
        EXIBIR "2 - Gerenciar Funcionários"
        EXIBIR "3 - Gerenciar Serviços"
        EXIBIR "0 - Sair"
        LER opcaoMenu

        ESCOLHA opcaoMenu
            CASO 1:
                CHAMAR menuCliente()
            CASO 2:
                CHAMAR menuFuncionario()
            CASO 3:
                CHAMAR menuServico()
            CASO 0:
                EXIBIR "Encerrando sistema..."
            CASO CONTRÁRIO:
                EXIBIR "Opção inválida!"
        FIMESCOLHA
    ATÉ opcaoMenu = 0

FIM
