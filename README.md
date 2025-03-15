# Respostas dos Exercícios de Calibração de Câmeras

## Questão 1: Cálculo da Coordenada Observada na Câmera

A projeção de um ponto do mundo para a imagem segue a Transformação em Perspectiva:
p = A · P

Onde:
* A é a Matriz de Transformação em Perspectiva (4x4);
* P é o ponto no mundo (4x1);
* p é o ponto projetado na imagem.

**Matriz A:**
```
    ⎡ 4  1  0  4 ⎤
A = ⎢ 1  0  1  3 ⎥
    ⎢ 2  0  2  4 ⎥
    ⎣ 3  1  0  5 ⎦
```

**Ponto P₇:**
P₇ = (4, 2, 1, 1)

**Cálculo da Multiplicação:**
```
         ⎡ (4×4) + (1×2) + (0×1) + (4×1) ⎤   ⎡ 22 ⎤
p = A·P₇ = ⎢ (1×4) + (0×2) + (1×1) + (3×1) ⎥ = ⎢  8 ⎥
         ⎢ (2×4) + (0×2) + (2×1) + (4×1) ⎥   ⎢ 14 ⎥
         ⎣ (3×4) + (1×2) + (0×1) + (5×1) ⎦   ⎣ 19 ⎦
```

Agora, normalizamos para obter x e y:
x = 22/19 ≈ 1.16,   y = 8/19 ≈ 0.42

**Resposta:** (x, y) ≈ (1.16, 0.42)

## Questão 2: Sequência Correta para Calibração da Câmera

A calibração segue esta ordem lógica:
1. Ler a imagem I (f)
2. Detectar o marcador m₁ em I (i)
3. Detectar as bordas de m₁ (e)
4. Calcular os pontos fiduciais de m₁ (d)
5. Ler os pontos fiduciais do marcador m₀ (g)
6. Calcular a distorção de m₁ em relação a m₀ (b)
7. Aplicar a distorção a m₁ (a)
8. Montar um sistema linear com os pontos fiduciais de m₀ e m₁ (h)
9. Calcular os parâmetros de calibração da câmera (c)

**Resposta:** (f → i → e → d → g → b → a → h → c)

## Questão 3: Cálculo dos Pontos Médios W₁₂ e W₂₃

A equação de estereoscopia:
Z = λ · B / |x₂ - x₁|

**Dados:** λ = 3, B = 3

Pontos conhecidos:
(x₁ᴬ, y₁ᴬ) = (3, 6), (x₁ᴮ, y₁ᴮ) = (1, 6)
(x₂ᴬ, y₂ᴬ) = (4, 6), (x₂ᴮ, y₂ᴮ) = (2, 6)
(x₃ᴮ, y₃ᴮ) = (0, 6), (x₂ᶜ, y₂ᶜ) = (0, 6), (x₃ᶜ, y₃ᶜ) = (-2, 6)

**Cálculo:**
W₁ = 3 × 3/|1 - 3| = 4.5
W₂ = 3 × 3/|0 - 4| = 2.25
W₃ = 3 × 3/|-2 - 0| = 4.5

Pontos médios:
W₁₂ = (W₁ + W₂)/2 = 3.375
W₂₃ = (W₂ + W₃)/2 = 3.375

## Questão 4: Distância entre os pontos k e w

A equação:
d = λ × |x₃ - x₄|/B

Com x₃ = 1, x₄ = -5:
d = 3 × |1 - (-5)|/5 = 3 × 6/5 = 3.6

**Resposta:** d = 3.6 metros.# imageCalc

## Questão 5 e 6: 

![image](https://github.com/user-attachments/assets/cebe9aee-f542-48c5-9e2a-53fcaa4ded4c)
![image](https://github.com/user-attachments/assets/ba4fa9f7-bb6b-4fab-ac26-26075e2a3c06)

![image](https://github.com/user-attachments/assets/fbe6d371-6e31-4d40-a72d-69a1017d5b17)
![image](https://github.com/user-attachments/assets/3d169643-bcf0-4b5c-ba81-733278dee091)

![image](https://github.com/user-attachments/assets/a9219703-94a2-4ca5-92b0-67f1519bf417)
![image](https://github.com/user-attachments/assets/ddd3ec05-f23b-4659-a321-102e77b44a0e)

![image](https://github.com/user-attachments/assets/ec93b484-4f6e-4472-a7a3-a5a0127bca74)
![image](https://github.com/user-attachments/assets/6c99c5dc-e925-4470-9172-628a9b46aa50)

![image](https://github.com/user-attachments/assets/b3635bbb-2399-4f16-bdd9-12f02587bf4c)
![image](https://github.com/user-attachments/assets/6abe0dfb-7e88-4d12-8262-1bd8cb000e5c)

![image](https://github.com/user-attachments/assets/54d18196-cd94-44fb-baf4-a5d5c89236e5)
![image](https://github.com/user-attachments/assets/9a0605a6-0b98-42b9-afb7-0d55e4af787f)

![image](https://github.com/user-attachments/assets/1f213d7b-034c-43b3-bc1a-8081fad7e495)
![image](https://github.com/user-attachments/assets/f62a7408-3e2d-4acc-871f-b873e620f04a)
