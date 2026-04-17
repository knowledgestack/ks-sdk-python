# SubscriptionStatus

Tenant subscription lifecycle state, mirrors Stripe subscription status.  Must include every status value Stripe can send, otherwise webhook handling silently drops updates. See https://stripe.com/docs/api/subscriptions/object#subscription_object-status.

## Enum

* `ACTIVE` (value: `'ACTIVE'`)

* `TRIALING` (value: `'TRIALING'`)

* `PAST_DUE` (value: `'PAST_DUE'`)

* `CANCELED` (value: `'CANCELED'`)

* `INCOMPLETE` (value: `'INCOMPLETE'`)

* `INCOMPLETE_EXPIRED` (value: `'INCOMPLETE_EXPIRED'`)

* `UNPAID` (value: `'UNPAID'`)

* `PAUSED` (value: `'PAUSED'`)

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


