# GNU-Netcat cheatsheet
<table>
  <thead>
    <tr>
      <th>Comando o Flag</th>
      <th>Descripción</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>nc &lt;host&gt; &lt;port&gt;</code></td>
      <td>Conexión a <code>&lt;host&gt;:&lt;port&gt;</code></td>
    </tr>
    <tr>
      <td><code>nc -l -p &lt;port&gt;</code></td>
      <td>Escucha en el puerto <code>&lt;port&gt;</code></td>
    </tr>
    <tr>
      <td><code>nc -nlvp &lt;port&gt;</code></td>
      <td>Escucha de todo tipo de conexiones</td>
    </tr>
    <tr>
      <td><code>-u</code></td>
      <td>UDP</td>
    </tr>
    <tr>
      <td><code>-v</code></td>
      <td>Verbose</td>
    </tr>
    <tr>
      <td><code>-n</code></td>
      <td>Sin resolución DNS</td>
    </tr>
    <tr>
      <td><code>-w &lt;num&gt;</code></td>
      <td>Tiempo de espera</td>
    </tr>
    <tr>
      <td><code>-i &lt;num&gt;</code></td>
      <td>Intervalo de tiempo</td>
    </tr>
    <tr>
      <td><code>nc -e /bin/sh</code></td>
      <td>Ejecuta una shell después de la conexión</td>
    </tr>
    <tr>
      <td><code>nc -c &lt;command&gt;</code></td>
      <td>Ejecuta un comando después de la conexión (al cerrar)</td>
    </tr>
    <tr>
      <td><code>-k</code></td>
      <td>Acepta múltiples conexiones</td>
    </tr>
  </tbody>
</table>

