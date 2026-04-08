# Carrinho Persistente

## Estratégia

- Sessão anónima: carrinho em `express-session` (memória/MySQL store)
- Após login: carrinho migra para DB e persiste entre sessões

## Esquema MySQL

```sql
CREATE TABLE carts (
  id INT PRIMARY KEY AUTO_INCREMENT,
  session_id VARCHAR(255),
  customer_id INT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  FOREIGN KEY (customer_id) REFERENCES customers(id)
);

CREATE TABLE cart_items (
  id INT PRIMARY KEY AUTO_INCREMENT,
  cart_id INT NOT NULL,
  product_id INT NOT NULL,
  quantity INT NOT NULL DEFAULT 1,
  price_at_add DECIMAL(10,2) NOT NULL,
  FOREIGN KEY (cart_id) REFERENCES carts(id),
  FOREIGN KEY (product_id) REFERENCES products(id)
);
```

## A Definir

- [ ] Expiração de carrinhos anónimos (TTL)
- [ ] UI do carrinho (sidebar slide-in ou página dedicada)
- [ ] Integração com checkout Stripe

---

← [Índice](../00-INDEX.md)
