# Base de Dados — MySQL 8

> Estrutura existente no repo gartnshine — não recriar, documentar.

## Tabelas Conhecidas

| Tabela | Descrição |
|---|---|
| `products` | Catálogo de produtos |
| `product_families` | Famílias (Prata, Latão, Macramé) |
| `users` / `customers` | Clientes (a criar para área cliente) |
| `sessions` | Sessões express-session |
| `cart` / `cart_items` | Carrinho persistente (a criar) |
| `orders` | Encomendas Stripe (a criar) |

## Famílias de Produto

```sql
-- Estrutura esperada
CREATE TABLE product_families (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100) NOT NULL,
  slug VARCHAR(100) UNIQUE NOT NULL,
  banner_image VARCHAR(255),
  description TEXT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Seeds
INSERT INTO product_families (name, slug) VALUES
  ('Prata', 'prata'),
  ('Latão', 'latao'),
  ('Macramé', 'macrame');
```

## A Documentar

- [ ] Schema completo actual (reverse engineer do gartnshine)
- [ ] Índices e foreign keys
- [ ] Estratégia de backup no VPS

---

← [Índice](../00-INDEX.md)
