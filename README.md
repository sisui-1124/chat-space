
<!-- ## usersテーブル

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false|
|password|string|null: false|


### Association
- has_many :groups_users
- has_many :groups, through: group_users
- has_many :chats

## chatsテーブル

|Column|Type|Options|
|------|----|-------|
|text|text||
|image|text||
|user_id|integer|null: false, foreign_key:true| 
|group_id|integer|null: false,foreign_key:true|

### Association
- belongs_to :user
- belongs_to :group


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|

### Assiciation
- has_many :users,through::group_users
- has_many:group_users
- has_many:chats  -->


<!-- ## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group -->

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|nickname|string|null:false|
|email|string|null: false|
|password|string|null: false|
|user_image|string| |
|introduction|texi|
|family_name|string|null: false|
|first_name|string|null: false|
|family_name_kana|string|null: false|
|first_name_kana|string|null: false|
|birth_day|data|null: false|


# Association
- hassmay :products dependent::destroy
- belongs_to:destination dependent::destroy
- belongs_to:card dependent::destroy

## destinationテーブル

|Column|Type|Options|
|------|----|-------|
|       |       |null:false|
|user_id|integer|foreigin_key:|
|       |       |true|
|family_name|string|null: false|
|first_name|string|null: false|
|family_name_kana|string|null: false|
|first_name_kana|string|null: false|
|post_code|string|null: false|
|prefecture|string|null: false|
|city|string|null: false|
|address|string||
|phone_number|string||


# Association
- belongs_to:user

## cardテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|ancestry|string||

 
# Association
- belong_to:user

## categoryテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|ancestry|string||


# Association
- has_many:products

## productテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|price|string|null: false|
|description|string|null: false|
|stattus|string|null: false|
|size|string|null: false|
|shipping_cost|string|null: false|
|shipping_days|string|null: false|
|prefecture_id|string|null: false|
|jufgment|string||
|           |       |null: false|
|category_id|integer|foreign_key:|
|           |       |true|
|        |       |null: false|
|brand_id|integer|foreign_key:|
|        |       |true|
|           |       |null: false|
|shipping_id|integer|foreign_key:|
|           |       |true|
|       |       |null: false|
|user_id|integer|foreign_key:|
|       |       |true|


# Association
- belong_to:user dependent::destroy
- belong_to:category dependent::destroy
- belong_to:brand dependent::destroy
- has_many:images dependent::destroy
- belongs_to_active_hash:prefecture

## imageテーブル

|Column|Type|Options|
|------|----|-------|
|image|string|null: false|
|product_id|integer|null:false|
|       |       |foreign_key:true|


# Association
- belong_to:product

## brandテーブル

|Column|Type|Options|
|------|----|-------|
name|string|index:true|


- has_many:products
