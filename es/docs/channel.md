# Channel

Los controladores proveén un método llamado `#channel` que puede ser usado para obtener el status de la conección con el backend. Los métodos de acceso a 'Channel' son reactivos.

| method      | description                                               |
|-------------|-----------------------------------------------------------|
| connected?  | devuelve 'true' si esta conectado con el backend                    |
| status      | posibles valores: :opening, :open, :closed, :reconnecting  |
| error       | el mensaje de error para la última conección fállida          |
| retry_count | el número de intentos de reconección que se han hecho sin una conección exitosa |
| reconnect_interval | el tiempo que ha pasado desde el último intento de reconección (en segundos) |

A veces necesitas correr un código específico cuando el cliente se conecta/desconecta del servidor. En un controlador puedes hacer lo siguiente:

```ruby
channel.on('connect') do
  .. connected ..
end

channel.on('disconnect') do
  .. disconnect ..
end
```
