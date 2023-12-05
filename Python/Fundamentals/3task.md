Después de un duro trimestre en la oficina, decides descansar un poco y tomarte unas vacaciones. 
Así que reservarás un vuelo para ti y tu novia e intentarás dejar todo el desorden atrás.

Necesitará un coche de alquiler para poder desplazarse durante sus vacaciones. 
El responsable del alquiler de coches te hace buenas ofertas.

Cada día que alquilas el auto cuesta $40. Si alquilas el auto por 7 días o más, 
obtienes $50 de descuento en tu total. Alternativamente, si alquilas el auto por 3 días o más, 
obtienes $20 de descuento en tu total.

Escriba un código que proporcione el monto total para diferentes días (d).

### Solucion

```python
def costo_alquiler_auto(dias):
    tarifa_diaria = 40  # Tarifa diaria de alquiler

    # Calcular el costo total sin ningún descuento
    costo_total = dias * tarifa_diaria

    # Aplicar descuentos según el número de días
    if dias >= 7:
        costo_total -= 50  # Descuento de $50 por alquilar 7 días o más
    elif 3 <= dias < 7:
        costo_total -= 20  # Descuento de $20 por alquilar 3 días o más

    return costo_total

# Ejemplo de uso:
num_dias = int(input("Ingrese el número de días que desea alquilar el auto: "))
monto_total = costo_alquiler_auto(num_dias)
print("Costo total por {} días: ${}".format(num_dias, monto_total))
```
