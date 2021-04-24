## Operações com matrizes em Julia

### Cálculo Numérico 2021.1 - UFAL

### Tutores:

- Leonardo Tolêdo
- Paulo Santos
- Ricardo Fernandes

#### Criar matrizes de zeros


```julia
matriz_quadrada = zeros(3, 3)
println("Matriz quadrada 3x3 de zeros: ", matriz_quadrada)

matriz_coluna = zeros(3, 1)
println("Matriz coluna 3x1 de zeros: ", matriz_coluna)

matriz_linha = zeros(1,3)
println("Matriz linha 1x3 de zeros: ", matriz_linha)
```

    Matriz quadrada 3x3 de zeros: [0.0 0.0 0.0; 0.0 0.0 0.0; 0.0 0.0 0.0]
    Matriz coluna 3x1 de zeros: [0.0; 0.0; 0.0]
    Matriz linha 1x3 de zeros: [0.0 0.0 0.0]


#### Criar matriz de uns


```julia
matriz_quadrada = ones(3,3)
```




    3×3 Array{Float64,2}:
     1.0  1.0  1.0
     1.0  1.0  1.0
     1.0  1.0  1.0



#### Preencher as linhas 1 e 2 da coluna 1 com uns


```julia
# Inicializando a matriz A com zeros
A = zeros(3, 3)
println("matriz A (antes da modificação): ", A)

# Alterando uma parte da matriz A
A[1:2, 1] = ones(2,1)
println("matriz A (depois da modificação): ", A)
```

    matriz A (antes da modificação): [0.0 0.0 0.0; 0.0 0.0 0.0; 0.0 0.0 0.0]
    matriz A (depois da modificação): [1.0 0.0 0.0; 1.0 0.0 0.0; 0.0 0.0 0.0]


#### Preencher as colunas 1 e 2 da linha 1 com uns


```julia
# Inicializando a matriz A com zeros
A = ones(3, 3)
println("matriz A (antes da modificação): ", A)

# Alterando uma parte da matriz A
A[1, 1:2] = zeros(1,2)
println("matriz A (depois da modificação): ", A)
```

    matriz A (antes da modificação): [1.0 1.0 1.0; 1.0 1.0 1.0; 1.0 1.0 1.0]
    matriz A (depois da modificação): [0.0 0.0 1.0; 1.0 1.0 1.0; 1.0 1.0 1.0]


#### Preencher as linhas e colunas de 1 a 2 com uns


```julia
# Inicializando a matriz A com zeros
A = ones(3, 3)
println("matriz A (antes da modificação): ", A)

# Alterando uma parte da matriz A
A[1:2, 1:2] = zeros(2,2)
println("matriz A (depois da modificação): ", A)
```

    matriz A (antes da modificação): [1.0 1.0 1.0; 1.0 1.0 1.0; 1.0 1.0 1.0]
    matriz A (depois da modificação): [0.0 0.0 1.0; 0.0 0.0 1.0; 1.0 1.0 1.0]


#### Soma e subtração de matrizes


```julia
A = [1 2; 3 4]
B = [5 6; 7 8]

println("Soma de A e B: ", A+B)

println("Subtração de A e B: ", A-B)
```

    Soma de A e B: [6 8; 10 12]
    Subtração de A e B: [-4 -4; -4 -4]


#### Produto de matrizes


```julia
A = [1 2; 3 4]
B = [5 6; 7 8]

println("Produto de A e B: ", A*B)
```

    Produto de A e B: [19 22; 43 50]


#### Inversa de uma matriz


```julia
A = [1 2; 3 4]

println("Inversa de A: ", inv(A))
```

    Inversa de A: [-1.9999999999999996 0.9999999999999998; 1.4999999999999998 -0.4999999999999999]
    
