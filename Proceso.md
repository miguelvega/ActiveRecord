# ActiveRecord

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

