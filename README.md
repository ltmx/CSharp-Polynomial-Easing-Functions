# C# Polynomial Easing Functions
C# cubic (smoothstep), Quintic (degree 5), Heptic (degree 7), Nonic (degree 9), Hendecic (degree 11)
Easing Math Functions

<img src="Unity%20Polynomial%20Easing%20Functions.png" alt="C# Polynomial Easing Functions" >


# Code

Functions and their derivatives

```csharp
public static class Easing
{
    static float smoothstep(float x) => x * x * (3 - 2 * x);
    static float smoothstepD(float x) => 6 * x * (1 - x); // Derivative

    static float smoothstep5(float x) => x * x * x * (x * (6 * x - 15) + 10);
    static float smoothstep5D(float x) => 30 * x * x * (x * (x - 2) + 1); // Derivative


    static float smoothstep7(float x) => x * x * x * x * (x * (x * (-20 * x + 70) - 84) + 35);
    static float smootherstep7D(float x) => 140 * x * x * x * (x * (x * (-x + 3) - 3) + 1); // Derivative


    static float smoothstep9(float x) => x * x * x * x * x * (x * (x * (x * (70 * x - 315) + 540) - 420) + 126);
    static float smoothstep9D(float x) => 630 * x * x * x * x * (x * (x * (x * (x - 4) + 6) - 4) + 1); // Derivative

    static float smoothstep11(float x) => x * x * x * x * x * x * (x * (x * (x * (x * (-252 * x + 1386) - 3080) + 3465) - 1980) + 462);
    static float smoothstep11D(float x) => 2772 * x * x * x * x * x * (x * (x * (x * (x * (-x + 5) - 10) + 10) - 5) + 1); // Derivative
}
```
