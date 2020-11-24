
# README

## usersテーブル
| Column                 | Type   | Options     |
| nickname               | string | null: false |
| name                   | string | null: false |
| email                  | string | unique:true |
| password               | string | null: false |
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

|Column       |Type     |Options     |

|name         | string  | null: false |
|category     | integer  | null: false |
|description  | string  | null:false  |
|condition    | integer  | null: false |
|fee          | integer | null: false |
|shipping_date| integer  | null: false |
|price        | integer | null: false |
|seller       | string  | null: false |
|users_id     | integer | foreign_key:true|


### Association
- belongs_to :user
- has_one    :buy

## buysテーブル

|Column|Type        |Options|
|users|references| foreign_key:true|
|items|references| foreign_key:true|


### Association
- belongs_to  :user
- belongs_to  :item
- has_one     :address



### Addressesテーブル
|Column         |Type   |Options|
|address        |string |null:false|
|post_code      |string |null:false|
|prefecture_id  |integer |null: false|
|phone_number   |string |null: false|




### Association
- belongs_to  :buy


