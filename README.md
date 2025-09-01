# DMHUB REST API Module

Módulo DMHUB que expõe APIs REST para integração externa com o Foundry VTT.

## Instalação

### Via URL (Recomendado)
```
https://raw.githubusercontent.com/Rufino-BR/dmhub-rest-api/main/module.json
```

### Manual
1. Baixe o arquivo `dmhub-rest-api-v1.0.0.zip`
2. Extraia na pasta `modules` do Foundry VTT
3. Ative o módulo no Foundry VTT

## Configuração

1. Vá em **Configure Settings** → **Manage Modules**
2. Encontre **"DMHUB REST API"** e clique em **Configure**
3. Configure:
   - **Token de API:** (gerado automaticamente)
   - **Habilitar API REST:** ✅ Ativado
   - **Origens Permitidas:** `*` (ou especifique o domínio)

## APIs Disponíveis

### Autenticação
Todas as APIs requerem o token de API como parâmetro `token`.

### Endpoints

#### Atores
- `GET /api/actors` - Lista todos os atores
- `GET /api/actors/{id}` - Ator específico

#### Itens
- `GET /api/items` - Lista todos os itens
- `GET /api/items/{id}` - Item específico

#### Cenas
- `GET /api/scenes` - Lista todas as cenas
- `GET /api/scenes/{id}` - Cena específica

#### Usuários
- `GET /api/users` - Lista todos os usuários
- `GET /api/users/{id}` - Usuário específico

#### Status
- `GET /api/status` - Status do servidor

## Exemplo de Uso

```javascript
// Listar todos os atores
fetch('http://seu-foundry:30000/api/actors?token=SEU_TOKEN')
  .then(response => response.json())
  .then(data => console.log(data));

// Obter ator específico
fetch('http://seu-foundry:30000/api/actors/abc123?token=SEU_TOKEN')
  .then(response => response.json())
  .then(data => console.log(data));
```

## Segurança

- Todas as APIs requerem autenticação via token
- Configure as origens permitidas para CORS
- Use HTTPS em produção

## Suporte

Para suporte, entre em contato com a equipe DMHUB.
