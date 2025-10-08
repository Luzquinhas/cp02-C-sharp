# ?? Sistema de Imobiliária - API REST
**RM:** if ([string]::IsNullOrWhiteSpace($rm)) {
## ?? Como executar
### 1. Restaurar pacotes
```bash
dotnet restore
```
### 2. Configurar banco de dados
Edite os arquivos .env em API/ e Data/ com sua senha:
```
DEFAULT_CONNECTION="User Id=rmif ([string]::IsNullOrWhiteSpace($rm)) {;Password=SUA_SENHA;Data Source=oracle.fiap.com.br:1521/orcl;"
```
### 3. Executar Migrations
```bash
cd Data
dotnet ef migrations add Inicial
dotnet ef database update
cd ..
```
### 4. Executar a API
```bash
cd API
dotnet run
```
### 5. Acessar Swagger
```
http://localhost:5002/swagger
```
## ?? Endpoints
- **/api/Imovel** - Gerenciamento de imóveis
- **/api/Cliente** - Gerenciamento de clientes
- **/api/Contrato** - Gerenciamento de contratos
## ? Entidades Implementadas
? Imóvel (com endereço, tipo, área, valores, status, etc)
? Cliente (com CPF/CNPJ único, contatos)
? Contrato (vínculo entre imóvel e cliente)
## ?? Recursos
- CRUD completo para todas as entidades
- Busca de imóveis por status e tipo
- Busca de contratos por cliente ou imóvel
- Validações de dados
- Migrations configuradas
- Swagger documentado
