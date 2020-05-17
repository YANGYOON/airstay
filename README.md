# README


# Description

# アピールポイント
##1.Gravatarで画像アイコン表示
##2.gemのtoastr-railsでログインや登録時などのnotificationを表示

# DB設計図
## users table
|Column|Type|Options|
|------|----|-------|
### Association
-has_many: rooms

## rooms table
|Column|Type|Options|
|home_type|string|-------|
|room_type|string|-------|
|accommodate|integer|-------|
|bed_room|integer|-------|
|bath_room|integer|-------|
|listing_name|string|-------|
|summary|text|-------|
|is_tv|boolean|-------|
|is_kitchen|boolean|-------|
|is_aircon|boolean|-------|
|is_heating|boolean|-------|
|is_internet|boolean-------|
|price|integer|-------|
|active|boolean|-------|
|user|references|foreign_key: true|
### Association
-belongs_to: user
