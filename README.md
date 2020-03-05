
## usersテーブル

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false|
|password|string|null: false|


### Association
- has_many :groups_users
- has_many :groups, through: groups_users
- has_many :chats

## chatsテーブル

|Column|Type|Options|
|------|----|-------|
|title|text|null: false|
|text|text|null: false|
|image|text|null: false|
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
- has_many :users,through::group_uses
- has_many:group_users
- has_many:chat 


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group
