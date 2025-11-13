# Misión imposible

## Misión 1: OPERACIÓN "INSULIN RESCUE"

Esta misión consiste en dar la bienvenida oficial al agente secreto y analizar la secuencia de insulina alterada por el Dr. Chaos. El script deberá revelar la secuencia completa, su longitud, la posible región comprometida (primeros 10 aminoácidos) y los últimos 10 aminoácidos.
Agente… el tiempo es limitado: tienes 7 días para completar esta operación.

```bash
#!/bin/bash

secuencia="MALWMRLLPLLALLALWGPDPAAAFVNQHLCGSHLVEALYLVCGERGFFYTPKTRREAEDLQVGQVELGGGPGAGSLQPLALEGSLQKRGIVEQCCTSICSLYQLENYCN"

echo ""
echo "Bienvenido agente u20231g864"
echo ""
echo "Tu identidad ha sido verificada."
echo "La misión comienza ahora."
echo ""

echo "=== INICIANDO ANÁLISIS DE SECUENCIA COMPROMETIDA...  ==="
echo "Secuencia Completa: $secuencia"
echo "Longitud total de la secuencia: ${#secuencia}" 
echo "Posible región comprometida: ${secuencia:0:10}"
echo "Últimos 10 aminoácidos: ${secuencia: -10}"
```

## Misión 2: OPERACIÓN "DNA TO RNA CONVERSION

El Dr. Chaos ha mezclado ADN con ARN para sabotear las investigaciones del Centro de Genética. Tu misión es crear un programa capaz de convertir la secuencia comprometida de ADN en su versión de ARN y verificar que la transformación sea correcta.
Agente… solo con una conversión precisa podremos recuperar las secuencias originales.

```bash
#!/bin/bash

adn="AAACGCGGCCTTTCCAACGGC"
echo ""

echo "INICIANDO PROTOCOLO DE CONVERSIÓN..."
echo ""
echo "Analizando secuencia de ADN infiltrada..."
echo "Secuencia de ADN original: $adn"
echo ""

echo "Ejecutando conversión molecular..."
echo "ADN → ARN"
arn="${adn//T/U}"
echo "Secuencia de ARN resultante: $arn" 
echo ""

echo "MISIÓN COMPLETADA - ARN RECUPERADO"
echo "" 
conteo_adn=$(echo "AAACGCGGCCTTTCCAACGGC" |grep -o "T"|wc -l)
echo "Cant. de T en ADN resultante: $conteo_adn"
conteo_arn=$(echo "$arn" |grep -o "U"|wc -l) 
echo "Cant. de U en ARN resultante: $conteo_arn"
```

## Misión 3: OPERACIÓN "DNA TO RNA CONVERSION

El villano ha ocultado un mensaje dentro de una secuencia de codones y tu tarea es descifrarlo. En el Departamento de Traducción Genética esperan que identifiques el codón de inicio, el de final y reveles el mensaje oculto.
Agente… esta vez, cada codón es una pista clave.

```bash
#!/bin/bash

codones="AUG UAC GCU UAA GCA UAG"
echo ""
echo "DESENCRIPTANDO MENSAJE MOLECULAR..."
echo ""
echo "Secuencia de codones: $codones"
echo ""

echo "Separando codones de la secuencia..."
echo "Primer codón: ${codones:0:3}"
echo "Último codones: ${codones: -3}"
echo ""

echo "MENSAJE DECODIFICACO EXITOSAMENTE"
codones="${codones/AUG/INICIO}"
codones="${codones/UAG/FIN}"
echo "Mensaje decodificado: $codones"
```



