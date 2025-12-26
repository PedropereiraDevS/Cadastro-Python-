pyhton 

cadastros = []

def cadastrar_pessoa():
    nome = input("Digite seu nome: ")
    email = input("Digite seu email: ")
    senha = input("Digite sua senha: ")

    pessoa = { "nome": nome,
               "email": email,
               "senha": senha }
    
    cadastro.append(pessoa)
    print("Cadastro Efetuado com Sucesso✅")

def listar_Cadastro():
    if not cadastros:
       print("Nenhum Cadastro.⚠️\n")
       return

   print("Lista de cadastros: ")
   for i, Cadastro in enumerate (cadastros, start=1): 
   print(f"{i}. Nome: {pessoa['nome']}| Senha: {pessoa['senha']} | Email: {pessoa['email']}")
   print()
def buscar_pessoa():
    nome_busca = input("Digite o nome para busca: ")

    for pessoa in cadastros:
        if pessoa["nome"].lower() == nome_busca.lower():
            print("🔍 Pessoa encontrada:")
            print(f"Nome: {pessoa['nome']}")
            print(f"Idade: {pessoa['idade']}")
            print(f"Email: {pessoa['email']}\n")
            return

    print("❌ Pessoa não encontrada.\n")


def menu():
    while True:
        print("===== MENU =====")
        print("1 - Cadastrar pessoa")
        print("2 - Listar pessoas")
        print("3 - Buscar pessoa")
        print("4 - Sair")

        opcao = input("Escolha uma opção: ")

        if opcao == "1":
            cadastrar_pessoa()
        elif opcao == "2":
            listar_pessoas()
        elif opcao == "3":
            buscar_pessoa()
        elif opcao == "4":
            print("👋 Encerrando o programa...")
            break
        else:
            print("⚠️ Opção inválida. Tente novamente.\n")


menu() 
       
