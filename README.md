# MetodosNumericos

## Módulo 1: Introducción a la programación

### Tema 1: Fundamentos de programación

#### 1.1 Datos y operadores en C#

```csharp
int a = 5;
int b = 10;
int suma = a + b;
Console.WriteLine("Suma: " + suma);

bool esMayor = a > b;
Console.WriteLine("Es A mayor que B: " + esMayor);
```

#### 1.2 Variables en C#

```csharp
string nombre = "Juan";
int edad = 25;
double salario = 1500.50;
Console.WriteLine($"Nombre: {nombre}, Edad: {edad}, Salario: {salario}");
```

#### 1.3 Entrada y salida de datos en C#

```csharp
Console.WriteLine("Introduce tu nombre:");
string nombre = Console.ReadLine();
Console.WriteLine("Hola, " + nombre + "!");
```

### Tema 2: Instrucciones de control

#### 2.1 If, else y switch en C#

```csharp
int numero = 10;

if (numero > 0)
{
    Console.WriteLine("El número es positivo.");
}
else if (numero < 0)
{
    Console.WriteLine("El número es negativo.");
}
else
{
    Console.WriteLine("El número es cero.");
}

switch (numero)
{
    case 1:
        Console.WriteLine("El número es uno.");
        break;
    case 2:
        Console.WriteLine("El número es dos.");
        break;
    default:
        Console.WriteLine("El número no es ni uno ni dos.");
        break;
}
```

#### 2.2 For en C#

```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine("Valor de i: " + i);
}
```

#### 2.3 While en C#

```csharp
int j = 0;
while (j < 5)
{
    Console.WriteLine("Valor de j: " + j);
    j++;
}
```

```csharp
int k = 0;
do
{
    Console.WriteLine("Valor de k: " + k);
    k++;
} while (k < 5);
```

### Tema 3: Vectores y matrices

#### 3.1 Arreglos lineales en C#

```csharp
int[] numeros = { 1, 2, 3, 4, 5 };
Console.WriteLine("Primer elemento: " + numeros[0]);
numeros[2] = 10; // Modificar valor
Console.WriteLine("Tercer elemento modificado: " + numeros[2]);
```

#### 3.2 Arreglos en dos dimensiones en C#

```csharp
int[,] matriz = new int[2, 3] { { 1, 2, 3 }, { 4, 5, 6 } };
Console.WriteLine("Elemento en (1,2): " + matriz[1, 2]);
matriz[0, 1] = 10; // Modificar valor
Console.WriteLine("Elemento modificado en (0,1): " + matriz[0, 1]);
```

#### 3.3 Matrices en C#

```csharp
// Definición y operaciones básicas con matrices
int[,] matrizA = { { 1, 2 }, { 3, 4 } };
int[,] matrizB = { { 5, 6 }, { 7, 8 } };
int[,] resultado = new int[2, 2];

for (int i = 0; i < 2; i++)
{
    for (int j = 0; j < 2; j++)
    {
        resultado[i, j] = matrizA[i, j] + matrizB[i, j];
        Console.WriteLine("Resultado en (" + i + "," + j + "): " + resultado[i, j]);
    }
}
```

### Tema 4: Fundamentos de métodos numéricos

#### 4.1 Calculadora de sumas y restas

```csharp
int Sumar(int a, int b)
{
    return a + b;
}

int Restar(int a, int b)
{
    return a - b;
}

Console.WriteLine("Suma: " + Sumar(5, 3));
Console.WriteLine("Resta: " + Restar(5, 3));
```

#### 4.2 Generar números en serie

```csharp
for (int i = 1; i <= 10; i++)
{
    Console.WriteLine(i);
}
```

#### 4.3 Generar números condicionales

```csharp
for (int i = 1; i <= 10; i++)
{
    if (i % 2 == 0)
    {
        Console.WriteLine(i + " es par.");
    }
}
```

### Tema 5: Soluciones por búsqueda exhaustiva

#### 5.1 Solución de una ecuación lineal

```csharp
double x = -10;
double resultado;
do
{
    resultado = 2 * x + 3; // Ejemplo: 2x + 3 = 0
    x += 0.1;
} while (resultado != 0);
Console.WriteLine("Solución: x = " + x);
```

#### 5.2 Solución de una ecuación trigonométrica

```csharp
double angulo = 0;
double precision = 0.0001;
do
{
    if (Math.Abs(Math.Sin(angulo) - 0.5) < precision)
    {
        break;
    }
    angulo += 0.01;
} while (angulo <= Math.PI);
Console.WriteLine("Solución: ángulo = " + angulo);
```

#### 5.3 Solución exhaustiva de sistema de ecuaciones

```csharp
double x = -10, y = -10;
double resultado1, resultado2;
do
{
    resultado1 = 2 * x + y - 1;  // Ejemplo: 2x + y - 1 = 0
    resultado2 = x - y + 3;      // Ejemplo: x - y + 3 = 0
    x += 0.1;
    y += 0.1;
} while (resultado1 != 0 && resultado2 != 0);
Console.WriteLine("Solución: x = " + x + ", y = " + y);
```

## Módulo 2: Solución de sistemas de ecuaciones

### Tema 6: Solución de ecuaciones lineales

#### 6.1 Solución de matrices

```csharp
int[,] matriz = { { 1, 2 }, { 3, 4 } };
int determinante = matriz[0, 0] * matriz[1, 1] - matriz[0, 1] * matriz[1, 0];
Console.WriteLine("Determinante: " + determinante);
```

#### 6.2 Reglas de álgebra lineal

```csharp
// Ejemplo: suma de matrices
int[,] matrizA = { { 1, 2 }, { 3, 4 } };
int[,] matrizB = { { 5, 6 }, { 7, 8 } };
int[,] suma = new int[2, 2];

for (int i = 0; i < 2; i++)
{
    for (int j = 0; j < 2; j++)
    {
        suma[i, j] = matrizA[i, j] + matrizB[i, j];
    }
}

Console.WriteLine("Suma de matrices:");
for (int i = 0; i < 2; i++)
{
    for (int j = 0; j < 2; j++)
    {
        Console.Write(suma[i, j] + " ");
    }
    Console.WriteLine();
}
```

#### 6.3 Eliminación de Gauss

```csharp
// Implementación del método de eliminación de Gauss para resolver sistemas lineales
double[,] a = { { 2, -1, 1 }, { 3, 3, 9 }, { 3, 3, 5 } };
double[] b = { 8, 0, -6 };
int n = 3;

for (int i = 0; i < n; i++)
{
    for (int k = i + 1; k < n; k++)
    {
        double t = a[k, i] / a[i, i];
        for (int j = 0; j < n; j++)
        {
            a[k, j] -= t * a[i, j];
        }
        b[k] -= t * b[i];
    }
}

double[] x = new double[n];
for (int i = n - 1; i >= 0; i--)
{
    x[i] = b[i];
    for (int j = i + 1; j < n; j++)
    {
        x[i] -= a[i, j] * x[j];
    }
    x[i] /= a[i, i];
}

Console.WriteLine("Soluciones:");
for (int i = 0; i < n; i++)
{
    Console.WriteLine("x" + (i + 1) + " = " + x[i]);
}
```

### Tema 7: Raíces de ecuaciones no lineales

#### 7.1 Método de bisección

```csharp
double Biseccion(Func<double, double> f, double a, double b, double tolerancia)
{
    double c;
    while ((b - a) >= tolerancia)
    {
        c = (a + b) / 2;

        if (f(c) == 0.0)
            break;
        else if (f(c) * f(a) < 0)
            b = c;
        else
            a = c;
    }
    return c;
}

double Funcion(double x)
{
    return x * x * x - x - 2;
}

double raiz = Biseccion(Funcion, 1, 2, 0.0001);
Console.WriteLine("Raíz: " + raiz);
```

#### 7.2 Método de secante

```csharp
double Secante(Func<double, double> f, double x0, double x1, double tolerancia, int maxIteraciones)
{
    double x2;
    for (int i = 0; i < maxIteraciones; i++)
    {
        x2 = x1 - (f(x1) * (x1 - x0)) / (f(x1) - f(x0));

        if (Math.Abs(x2 - x1) < tolerancia)
            return x2;

        x0 = x1;
        x1 = x2;
    }
    return x2;
}

double Funcion(double x)
{
    return x * x * x - x - 2;
}

double raiz = Secante(Funcion, 1, 2, 0.0001, 100);
Console.WriteLine("Raíz: " + raiz);
```

#### 7.3 Método de Newton-Raphson

```csharp
double NewtonRaphson(Func<double, double> f, Func<double, double> df, double x0, double tolerancia, int maxIteraciones)
{
    double x1;
    for (int i = 0; i < maxIteraciones; i++)
    {
        x1 = x0 - f(x0) / df(x0);

        if (Math.Abs(x1 - x0) < tolerancia)
            return x1;

        x0 = x1;
    }
    return x1;
}

double Funcion(double x)
{
    return x * x * x - x - 2;
}

double Derivada(double x)
{
    return 3 * x * x - 1;
}

double raiz = NewtonRaphson(Funcion, Derivada, 1, 0.0001, 100);
Console.WriteLine("Raíz: " + raiz);
```

### Tema 8: Sistema de ecuaciones no lineales

#### 8.1 Definición de ecuaciones no lineales

Concepto y ejemplos de ecuaciones no lineales

Características de las ecuaciones no lineales

#### 8.2 Matriz Jacobiana

```csharp
double[,] MatrizJacobiana(double[] x)
{
    double[,] jacobiana = new double[2, 2];
    jacobiana[0, 0] = 2 * x[0];      // Derivada parcial de la primera ecuación respecto a x1
    jacobiana[0, 1] = 2 * x[1];      // Derivada parcial de la primera ecuación respecto a x2
    jacobiana[1, 0] = 1;             // Derivada parcial de la segunda ecuación respecto a x1
    jacobiana[1, 1] = -1;            // Derivada parcial de la segunda ecuación respecto a x2
    return jacobiana;
}
```

#### 8.3 Solución de sistemas no lineales

```csharp
double[] NewtonRaphsonSistema(Func<double[], double[]> f, Func<double[], double[,]> jacobiana, double[] x0, double tolerancia, int maxIteraciones)
{
    int n = x0.Length;
    double[] x1 = new double[n];
    for (int i = 0; i < maxIteraciones; i++)
    {
        double[] fx = f(x0);
        double[,] j = jacobiana(x0);

        // Resolver el sistema J * delta = -f(x)
        double[] delta = ResolverSistemaLineal(j, fx);

        for (int j = 0; j < n; j++)
            x1[j] = x0[j] - delta[j];

        if (Norma(delta) < tolerancia)
            return x1;

        Array.Copy(x1, x0, n);
    }
    return x1;
}
```

### Tema 9: Mínimos cuadrados

#### 9.1 Definición de ajuste de curvas

Concepto y propósito del ajuste de curvas

Aplicaciones del ajuste de curvas en diferentes campos

#### 9.2 Teoría de mínimos cuadrados

```csharp
double[] MinimosCuadrados(double[] x, double[] y)
{
    int n = x.Length;
    double sumX = 0, sumY = 0, sumXY = 0, sumXX = 0;
    for (int i = 0; i < n; i++)
    {
        sumX += x[i];
        sumY += y[i];
        sumXY += x[i] * y[i];
        sumXX += x[i] * x[i];
    }

    double b = (n * sumXY - sumX * sumY) / (n * sumXX - sumX * sumX);
    double a = (sumY - b * sumX) / n;

    return new double[] { a, b };
}
```

#### 9.3 Solución de mínimos cuadrados lineales

```csharp
double[] x = { 1, 2, 3, 4, 5 };
double[] y = { 1, 2, 1.3, 3.75, 2.25 };
double[] coeficientes = MinimosCuadrados(x, y);

Console.WriteLine("a: " + coeficientes[0]);
Console.WriteLine("b: " + coeficientes[1]);
```

### Tema 10: Regresión no lineal

#### 10.1 Modelos de parámetros no lineales

Ejemplos de modelos no lineales

Aplicaciones prácticas de la regresión no lineal

#### 10.2 Estimación de parámetros no lineales

```csharp
// Implementación de un modelo no lineal y estimación de sus parámetros
// Ejemplo simple de regresión exponencial
using MathNet.Numerics.Optimization;

Func<double[], double[], double> ErrorCuadratico = (p, x) =>
{
    double error = 0;
    for (int i = 0; i < x.Length; i++)
    {
        error += Math.Pow(p[0] * Math.Exp(p[1] * x[i]) - y[i], 2);
    }
    return error;
};

double[] EstimacionParametros(double[] x, double[] y)
{
    double[] parametrosIniciales = { 1, 1 };
    var resultado = NelderMeadSolver.Solve(p => ErrorCuadratico(p, x), parametrosIniciales);
    return resultado.Point;
}
```

#### 10.3 Solución de mínimos cuadrados no lineales

```csharp
double[] x = { 1, 2, 3, 4, 5 };
double[] y = { 1.5, 3.5, 8, 18, 38 };
double[] parametros = EstimacionParametros(x, y);

Console.WriteLine("a: " + parametros[0]);
Console.WriteLine("b: " + parametros[1]);
```

## Módulo 3: Métodos de integración

### Tema 11: Interpolación

#### 11.1 Teoría de interpolación

Concepto y fundamentos de la interpolación

Tipos de interpolación y aplicaciones

#### 11.2 Polinomio de Lagrange

```csharp
double PolinomioLagrange(double[] x, double[] y, double xi)
{
    double resultado = 0;
    for (int i = 0; i < x.Length; i++)
    {
        double termino = y[i];
        for (int j = 0; j < x.Length; j++)
        {
            if (j != i)
            {
                termino *= (xi - x[j]) / (x[i] - x[j]);
            }
        }
        resultado += termino;
    }
    return resultado;
}
```

#### 11.3 Polinomio de Newton

```csharp
double PolinomioNewton(double[] x, double[] y, double xi)
{
    double[] coeficientes = DiferenciasDivididas(x, y);
    double resultado = coeficientes[0];
    for (int i = 1; i < x.Length; i++)
    {
        double termino = coeficientes[i];
        for (int j = 0; j < i; j++)
        {
            termino *= (xi - x[j]);
        }
        resultado += termino;
    }
    return resultado;
}

double[] DiferenciasDivididas(double[] x, double[] y)
{
    int n = x.Length;
    double[] coef = new double[n];
    Array.Copy(y, coef, n);

    for (int j = 1; j < n; j++)
    {
        for (int i = n - 1; i >= j; i--)
        {
            coef[i] = (coef[i] - coef[i - j]) / (x[i] - x[i - j]);
        }
    }
    return coef;
}
```

### Tema 12: Integrales numéricas

#### 12.1 Definición de integral

Concepto básico de integral y sus aplicaciones

Diferencias entre integrales definidas e indefinidas

#### 12.2 Integral rectangular

```csharp
double IntegralRectangular(Func<double, double> f, double a, double b, int n)
{
    double h = (b - a) / n;
    double suma = 0;
    for (int i = 0; i < n; i++)
    {
        suma += f(a + i * h);
    }
    return h * suma;
}

double Funcion(double x)
{
    return x * x; // Ejemplo: f(x) = x^2
}

double resultado = IntegralRectangular(Funcion, 0, 1, 100);
Console.WriteLine("Resultado de la integral rectangular: " + resultado);
```

#### 12.3 Integral de trapezoide

```csharp
double IntegralTrapezoide(Func<double, double> f, double a, double b, int n)
{
    double h = (b - a) / n;
    double suma = (f(a) + f(b)) / 2;
    for (int i = 1; i < n; i++)
    {
        suma += f(a + i * h);
    }
    return h * suma;
}

double Funcion(double x)
{
    return x * x; // Ejemplo: f(x) = x^2
}

double resultado = IntegralTrapezoide(Funcion, 0, 1, 100);
Console.WriteLine("Resultado de la integral de trapezoide: " + resultado);
```

### Tema 13: Regla de Simpson

#### 13.1 Regla de Simpson 1/3

Concepto y principios de la regla de Simpson 1/3

Aplicaciones y ventajas de la regla de Simpson

#### 13.2 Código de Regla de Simpson 1/3

```csharp
double ReglaSimpson(Func<double, double> f, double a, double b, int n)
{
    if (n % 2 != 0)
    {
        throw new ArgumentException("El número de intervalos debe ser par");
    }

    double h = (b - a) / n;
    double suma = f(a) + f(b);

    for (int i = 1; i < n; i += 2)
    {
        suma += 4 * f(a + i * h);
    }

    for (int i = 2; i < n - 1; i += 2)
    {
        suma += 2 * f(a + i * h);
    }

    return h * suma / 3;
}

double Funcion(double x)
{
    return x * x; // Ejemplo: f(x) = x^2
}

double resultado = ReglaSimpson(Funcion, 0, 1, 100);
Console.WriteLine("Resultado de la regla de Simpson: " + resultado);
```

#### 13.3 Solución de Regla de Simpson 1/3

Ejemplos prácticos de aplicación de la regla de Simpson

Comparación de resultados con otros métodos de integración

### Tema 14: Solución de ecuaciones diferenciales ordinarias

#### 14.1 Definición de ecuaciones diferenciales ordinarias

Conceptos básicos y ejemplos de ecuaciones diferenciales ordinarias

Aplicaciones de las ecuaciones diferenciales en diversas áreas

#### 14.2 Método de Euler

```csharp
double[] MetodoEuler(Func<double, double, double> f, double x0, double y0, double h, int n)
{
    double[] y = new double[n + 1];
    y[0] = y0;
    for (int i = 0; i < n; i++)
    {
        y[i + 1] = y[i] + h * f(x0 + i * h, y[i]);
    }
    return y;
}

double Funcion(double x, double y)
{
    return y - x * x + 1; // Ejemplo: y' = y - x^2 + 1
}

double[] resultado = MetodoEuler(Funcion, 0, 0.5, 0.1, 10);
for (int i = 0; i <= 10; i++)
{
    Console.WriteLine("y(" + (i * 0.1) + ") = " + resultado[i]);
}
```

#### 14.3 Método de Runge-Kutta

```csharp
double[] MetodoRungeKutta(Func<double, double, double> f, double x0, double y0, double h, int n)
{
    double[] y = new double[n + 1];
    y[0] = y0;
    for (int i = 0; i < n; i++)
    {
        double k1 = h * f(x0 + i * h, y[i]);
        double k2 = h * f(x0 + i * h + 0.5 * h, y[i] + 0.5 * k1);
        double k3 = h * f(x0 + i * h + 0.5 * h, y[i] + 0.5 * k2);
        double k4 = h * f(x0 + (i + 1) * h, y[i] + k3);
        y[i + 1] = y[i] + (k1 + 2 * k2 + 2 * k3 + k4) / 6;
    }
    return y;
}

double Funcion(double x, double y)
{
    return y - x * x + 1; // Ejemplo: y' = y - x^2 + 1
}

double[] resultado = MetodoRungeKutta(Funcion, 0, 0.5, 0.1, 10);
for (int i = 0; i <= 10; i++)
{
    Console.WriteLine("y(" + (i * 0.1) + ") = " + resultado[i]);
}
```

### Tema 15: Solución de ecuaciones diferenciales ordinarias de 2º orden

#### 15.1 Definición de ecuaciones diferenciales de 2º orden

Conceptos y ejemplos de ecuaciones diferenciales de segundo orden

Aplicaciones y métodos de solución

#### 15.2 Solución por Runge-Kutta

Aplicación del método de Runge-Kutta a ecuaciones de segundo orden

#### 15.3 Método de disparo

```csharp
double MetodoDisparo(Func<double, double, double> f, double x0, double y0, double yf, double h, int n)
{
    double[] y = new double[n + 1];
    double[] z = new double[n + 1];
    y[0] = y0;
    z[0] = 1; // Suponiendo una estimación inicial

    for (int i = 0; i < n; i++)
    {
        double k1_y = h * z[i];
        double k1_z = h * f(x0 + i * h, y[i]);

        double k2_y = h * (z[i] + 0.5 * k1_z);
        double k2_z = h * f(x0 + i * h + 0.5 * h, y[i] + 0.5 * k1_y);

        double k3_y = h * (z[i] + 0.5 * k2_z);
        double k3_z = h * f(x0 + i * h + 0.5 * h, y[i] + 0.5 * k2_y);

        double k4_y = h * (z[i] + k3_z);
        double k4_z = h * f(x0 + (i + 1) * h, y[i] + k3_y);

        y[i + 1] = y[i] + (k1_y + 2 * k2_y + 2 * k3_y + k4_y) / 6;
        z[i + 1] = z[i] + (k1_z + 2 * k2_z + 2 * k3_z + k4_z) / 6;
    }
    
    // Ajuste del valor inicial estimado
    double ajuste = (yf - y[n]) / z[n];
    for (int i = 0; i <= n; i++)
    {
        y[i] += ajuste * z[i];
    }
    return y;
}

double Funcion(double x, double y)
{
    return y - x * x + 1; // Ejemplo: y' = y - x^2 + 1
}

double[] resultado = MetodoDisparo(Funcion, 0, 0.5, 1, 0.1, 10);
for (int i = 0; i <= 10; i++)
{
    Console.WriteLine("y(" + (i * 0.1) + ") = " + resultado[i]);
}
```
