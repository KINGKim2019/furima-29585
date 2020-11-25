
# README

## usersテーブル
| Column                 | Type   | Options     |
| nickname               | string | null: false |
| email                  | string | null: false |
|encrypted_password      | string | null: false |
|family_name             | string | null: false |
|first_name              | string | null: false | 
|family_name_kana        | string | null: false |
|first_name_kana         | string | null: false |    
|date_of_birth           | date   | null: false | 

### Association
- has_many :items
- has_many :buys



## itemsテーブル

|Column                         |Type      |Options     |
|category_id                    | integer  | null: false |
|name                           | string   | null: false |
|information                    | text     | null: false |
|scheduled_delivery_select_id   | integer  | null: false |
|condition_id                | integer  | null: false |
|fee_id                      | integer  | null: false |
|shopping_date_id            | integer  | null: false |
|price                       | integer  | null: false |
|user                        |references| foreign_key:true|


### Association
- belongs_to :user
- has_one    :buy

## buysテーブル

|Column|Type        |Options|
|user   |references| foreign_key:true|
|item   |references| foreign_key:true|
|address|references| foreign_key:true|


### Association
- belongs_to  :user
- belongs_to  :item
- has_one     :address



### Addressesテーブル
|Column         |Type   |Options|
|address        |string |null:false|
|post_code      |string |null:false|
|prefecture_id  |integer|null: false|
|city           |string |null: false|
|building_number|string |           |
|phone_number   |string |null: false|




### Association
- belongs_to  :buy


