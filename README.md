# 🚗 **Car Rental Service - Testes Automatizados** 🧪

Este é um projeto de estudo focado em **JavaScript** e práticas de **Testes Automatizados** utilizando **Mocha**, **Chai** e **Sinon**.

---

## 🚀 **Objetivo**
Garantir que as principais funcionalidades de um sistema de aluguel de carros estejam funcionando corretamente, com cobertura de testes unitários.

---

## 🛠️ **Tecnologias Utilizadas**
- **Node.js**  
- **Mocha**: Framework de testes.  
- **Chai**: Biblioteca de asserções.  
- **Sinon**: Ferramenta para stubs, spies e mocks.

---

## ✅ **Funcionalidades Testadas**
1. **Seleção Aleatória de Carros**  
2. **Cálculo do Valor do Aluguel**  
   - Considera o número de dias alugados e a idade do cliente.  
3. **Geração de Recibo da Transação**  
   - Inclui cliente, carro, data de devolução e valor final.

---

## 🧪 **Exemplo de Teste**
```javascript
it("given a customer and a car category it should return a transaction receipt", async () => {
    const result = await carService.rent(customer, carCategory, numberOfDays);
    const expected = new Transaction({
        customer,
        car,
        dueDate,
        amount: "R$ 206,80",
    });
    expect(result).to.be.deep.equal(expected);
});
