
# README

## usersテーブル
| Column            | Type   | Options     |
| nickname          | string | null: false |
| name              | string | null: false |
| email             | string | unique:true |
| password          | string | null: false |
|encrypted_password | string | null: false |
|family_name        | string | null: false |
|first_name         | string | null: false |    
|date_of_birth      |integer | null: false | 

### Association
- has_many :items
- has_many :buys



## itemsテーブル

|Column       |Type     |Options     |
|image        | string  |            |
|name         | string  | null: false |
|category     | string  | null: false |
|description  | string  | null:false  |
|condition    | string  | null: false |
|fee          | string  | null: false |
|shipping_date| string  | null: false |
|price        | integer | null: false |
|seller       | string  | null: false |
|users_id     | integer | foreign_key:true|


### Association
- belongs_to :user
- has_one    :buy

## buysテーブル

|Column|Type        |Options|
|users_id|references| foreign_key:true|
|items_id|references| foreign_key:true|


### Association
- belongs_to  :user
- belongs_to  :item
- has_one     :address



### Addressesテーブル
|Column      |Type   |Options|
|address     |string |null:false|
|post_code   |string |null:false|
|prefecture  |string |null: false|
|phone_number|string |null: false|




### Association
- belongs_to  :buy
- belongs_to  :buy

