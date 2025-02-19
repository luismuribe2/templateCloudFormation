# Trabajo Práctico: Desplegando Infraestructura con CloudFormation

## Objetivo
Aplicar lo aprendido sobre **CloudFormation** creando y desplegando una infraestructura básica en AWS mediante una plantilla YAML.

## Instrucciones

### 1. Crear una plantilla de CloudFormation (`template.yaml`)
La plantilla debe desplegar como mínimo:
- Un **bucket S3** con versionamiento activado.
- Un **grupo de seguridad** que permita tráfico HTTP (puerto 80).
- Una **instancia EC2** usando este grupo de seguridad.

### 2. Subir la plantilla a un repositorio Git
Sigue buenas prácticas al trabajar con Git:
- Crear un **repositorio privado** en GitHub.
- Agregar un **archivo `README.md`** explicando qué hace la plantilla.
- Escribir **buenos mensajes de commit**.
- Añadir a **SantiagoLoaiza** como contribuyente.

### 3️. Desplegar la infraestructura usando la AWS CLI
Ejecuta el siguiente comando en Bash:

```bash
aws cloudformation create-stack --stack-name <<StackName>> --template-body file://template.yaml --capabilities CAPABILITY_NAMED_IAM
```

Verifica que el stack se creó correctamente en la consola de AWS.

### 4️. Eliminar la infraestructura después de la prueba
Para limpiar los recursos creados, ejecuta:

```bash
aws cloudformation delete-stack --stack-name <<StackName>>
```

## Entregable
- Enlace al **repositorio Git** con:
  - La plantilla `template.yaml`.
  - El archivo `README.md` con una explicación clara.
- Capturas de pantalla del stack en AWS antes de eliminarlo.

