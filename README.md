
# README
<<<<<<< Updated upstream
=======
## usersテーブル
| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| nickname | string | null: false |
| name     | string | null: false |
| email    | string | unique:true |
| password | string | null: false |
>>>>>>> Stashed changes

<<<<<<< Updated upstream
=======

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
<<<<<<< Updated upstream
- belongs_to  :buys
1
>>>>>>> Stashed changes
=======
- belongs_to  :buy
>>>>>>> Stashed changes
