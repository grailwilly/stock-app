# Stock App

## Database Design
==== users ====
role: admin/trade
has_many :transactions
has_many :stocks

==== transactions ====
user_id
action: buy/sell
status: fail/success
amount: 0
created_at
belongs_to :users
has_one :stocks

==== stocks ====
name
price
transaction_id
user_id
belongs_to :users

==== market ====
has_many :stocks

