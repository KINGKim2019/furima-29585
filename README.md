
# README
## usersテーブル
| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| name     | string | null: false |
| email    | string | unique:true |
| password | string | null: false |


### Association
- has_many :items
- has_many :buys



## itemsテーブル

|Column    |Type    |Options|
|items name| string | null: false |
|category  | string | null: false |
|price     | string | null: false |
|seller    | string | null: false |
|users_id  | references | foreign_key:true|


### Association
- belongs_to :users
- has_one    :buys

## buysテーブル

|Column|Type        |Options|
|buyer | string     | null:false|
|users_id|references| foreign_key:true|
|items_id|references| foreign_key:true|

### Association
- belongs_to  :users
- belongs_to  :items
- has_one     :adresses



### Addressesテーブル
|Column  |Type   |Options|
|adresses|string |null:false|



### Association
- belongs_to  :buys
