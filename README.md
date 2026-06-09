# Dilan-Agrinho
<section class="cartoes">
  <article class="cartao">
    <div class="cartao-interno">
      <div class="cartao-frente">
        <h2>Pergunta</h2>
        <p>Qual é a capital da França?</p>
      </div>
      <div class="cartao-verso">
        <h2>Resposta</h2>
        <p>Paris</p>
      </div>
    </div>
  </article>

  <article class="cartao">
    <div class="cartao-interno">
      <div class="cartao-frente">
        <h2>Pergunta</h2>
        <p>Qual é 5 x 6?</p>
      </div>
      <div class="cartao-verso">
        <h2>Resposta</h2>
        <p>30</p>
      </div>
    </div>
  </article>
</section>
.cartao {
  width: 200px;
  height: 300px;
  perspective: 1000px; /* dá profundidade para o 3D */
}

.cartao-interno { 
  position: relative; 
  width: 100%;
  height: 100%;
  transition: transform 0.8s;
  transform-style: preserve-3d; 
}

.cartao-frente, 
.cartao-verso { 
  position: absolute;
  width: 100%;
  height: 100%;
  border-radius: 12px; 
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15); 
  backface-visibility: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: sans-serif;
  font-size: 1.1rem;
}

.cartao-verso { 
  transform: rotateY(180deg); 
  background-color: #f0f0f0; /* contraste para a resposta */
}

.cartao-frente {
  background-color: #ffffff;
}

.cartao:hover .cartao-interno { 
  transform: rotateY(180deg); 
}
section.cartoes {
  display: flex;
  gap: 16px; /* espaço entre os cards */
  flex-wrap: wrap; /* permite que quebrem linha em telas menores */
  justify-content: center; /* centraliza os cards horizontalmente */
  padding: 16px;
}