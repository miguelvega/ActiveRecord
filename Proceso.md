# ActiveRecord
Ejecutamos `bundle` para asegurarse de tener las gemas necesaria

![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/1.png)

Ejecutamos el archivo de prueba con `bundle exec rspec spec/activerecord_practice_spec.rb` y el resultado debe ser `13 ejemplos, 0 fallas, 13 pendientes`, pues 
todas las pruebas se estan ignorando ya que se usa uso de `xspecify` que es una especie de comentario para marcar pruebas como omitidas temporalmente.

![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/2.png)


![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/3.png)

Cambiamos `xspecify` por `specify` y guardamos el archivo. Este cambio hará que esa prueba en particular no se omita en la siguiente ejecución de prueba.
Con lo cual la prueba fallará inmediatamente porque no hemos escrito el código necesario.

![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/4.png)


![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/5.png)

Pasamos la primera prueba cambiando un `xspecify` por `specify` escribiendo el siguiente codigo en `lib/activerecord_practica.rb`:
```

def self.any_candice
    # Tu codigo aqui para devolver todos los clientes cuyo nombre sea Candice
    # probablemente algo asi:  Customer.where(....)
    Customer.where(first: 'Candice')
end
```

![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/6.png)

Seguimos editando el archivo `activerecord_practica.rb` con el objetivo de pasar todas las pruebas y ejecutamos el comando `bundle exec rspec spec/activerecord_practice_spec.rb`.

![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/7.png)

Con lo cual conseguimos pasar todas las pruebas.

Luego, usamos la herramienta guard con lo cual nos muestra lo siguiente:
![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/8.png)

En una ventana del editor, realizamos un cambio trivial en el `specfile` o en `activerecord_practica.rb`, nsertar un espacio  y guardamos el archivo. En uno o dos segundos, la ventana de terminal que ejecuta Guard debería cobrar vida cuando Guard intenta volver a ejecutar las pruebas

![](https://github.com/miguelvega/ActiveRecord/blob/main/Imagenes/9.png)
