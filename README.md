class Produto:
    def __init__(self, nome, preco):
        self.nome = nome
        self.preco = preco

class CarrinhoDeCompras:
    def __init__(self):
        self.itens = []

    def adicionar_item(self, produto, quantidade):
        self.itens.append((produto, quantidade))

    def calcular_total(self):
        total = 0
        for produto, quantidade in self.itens:
            total += produto.preco * quantidade
        return total

    def mostrar_carrinho(self):
        for produto, quantidade in self.itens:
            print(f"{produto.nome} - Quantidade: {quantidade}")

if __name__ == "__main__":
    produto1 = Produto("Esfirra", 20.00)
    produto2 = Produto("Panqueca", 15.00)
    produto3 = Produto("Mini Pizza",20.00)
    

    carrinho = CarrinhoDeCompras()
    carrinho.adicionar_item(produto1, 5)
    carrinho.adicionar_item(produto2, 2)
    carrinho.adicionar_item(produto3 , 5)
    carrinho.mostrar_carrinho()
    print("Total:R$",carrinho.calcular_total())
