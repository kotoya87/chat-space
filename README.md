
## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_name|string|null: false|
|chat_member|string|null: false|

### Association
- has_many :groups_users
- belongs_to :messages

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false|

### Association
- has_many :groups_users
- belongs_to :messages

## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text|null: false|

### Association
- belongs_to :group
- belongs_to :user
