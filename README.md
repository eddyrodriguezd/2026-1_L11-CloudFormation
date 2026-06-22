# AWS CloudFormation Lab - DynamoDB, Lambda y API Gateway

## Objetivo

En este laboratorio aprenderemos a utilizar **AWS CloudFormation** para desplegar la infraestructura necesaria para una aplicación serverless.

La lógica de negocio de la función Lambda ya se encuentra disponible en el archivo: index.py

---

## Documentación de referencia

### CloudFormation - DynamoDB Table

https://docs.aws.amazon.com/AWSCloudFormation/latest/TemplateReference/aws-resource-dynamodb-table.html

### CloudFormation - Lambda Function

https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/TemplateReference/aws-resource-lambda-function.html

### CloudFormation - IAM Role

https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/TemplateReference/aws-resource-iam-role.html

### CloudFormation - API Gateway RestApi

https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/TemplateReference/aws-resource-apigateway-restapi.html

### CloudFormation - API Gateway Resource

https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/TemplateReference/aws-resource-apigateway-resource.html

### CloudFormation - API Gateway Method

https://docs.aws.amazon.com/es_es/AWSCloudFormation/latest/TemplateReference/aws-resource-apigateway-method.html

---

## Despliegue del stack

Documentación oficial:

https://docs.aws.amazon.com/cli/latest/reference/cloudformation/deploy.html

Comando base:

```bash
aws cloudformation deploy --stack-name vote-system-stack-{servicio} --template-file {servicio}.yaml --profile temasD
```

Opciones útiles:

```bash
--no-execute-changeset
```
Permite crear el Change Set sin ejecutarlo inmediatamente, para revisar los cambios antes del despliegue.

```bash
--capabilities CAPABILITY_NAMED_IAM
```
Necesario únicamente cuando la plantilla crea o modifica recursos IAM (por ejemplo, Roles o Policies).

---

## Eliminación del stack

Comando:

```bash
aws cloudformation delete-stack --stack-name vote-system-stack-{servicio} --profile temasD
```
