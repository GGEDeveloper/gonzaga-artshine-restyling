# Checkout Stripe

## Fluxo

```
Carrinho → Checkout → Stripe Payment Intent → Confirmação → Ordem criada → Email (Resend)
```

## Integração

```javascript
// Criar Payment Intent
const paymentIntent = await stripe.paymentIntents.create({
  amount: totalCents,       // em cêntimos
  currency: 'eur',
  metadata: { order_id: orderId }
});

res.json({ clientSecret: paymentIntent.client_secret });
```

## Webhook para Confirmação

```javascript
app.post('/stripe/webhook', express.raw({ type: 'application/json' }), (req, res) => {
  const sig = req.headers['stripe-signature'];
  const event = stripe.webhooks.constructEvent(req.body, sig, process.env.STRIPE_WEBHOOK_SECRET);

  if (event.type === 'payment_intent.succeeded') {
    const pi = event.data.object;
    // Marcar ordem como paga + enviar email Resend
  }

  res.json({ received: true });
});
```

## A Definir

- [ ] UI do formulário de pagamento (Stripe Elements)
- [ ] Página de sucesso e de erro
- [ ] Email de confirmação (template Resend)
- [ ] Gestão de stock após pagamento

---

← [Índice](../00-INDEX.md)
