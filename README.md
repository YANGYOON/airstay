# README


# Description

# アピールポイント
-Gravatarで画像アイコン表示
-gemのtoastr-railsでログインや登録時などのnotificationを表示
-部屋掲載機能(非同期通信画像削除、掲載手順チェックマーク)
-部屋ページ(GoogleMAP)

# TODO LIST
-予約
-レビュー
-検索機能
-ホームページ

# DB設計図
## users table
|Column|Type|Options|
|email|string|-------|
|password|string|-------|
|fullname|string|-------|
|phone_number|intger|-------|
|description|text|-------|
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
-has_many: photos

## photo table
|Column|Type|Options|
|room_id|references|-------|
|images|text|-------|
### Association
-belongs_to: rooms


