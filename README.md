# README

# NAME: AIRSTAY vacation rental platform

# Description
自身の経歴したAIRBNBホスト時代に運営したプラットフォームに感銘を受け、
現在トレンドでもあるP2Pビジネスの形態の一つとして、
シェアリングエコノミープラットフォームを作ることに試みました。
現在進行中。

# アピールポイント
- Gravatarで画像アイコン表示
- gemのtoastr-railsでログインや登録時などのnotificationを表示
[![Image from Gyazo](https://i.gyazo.com/f28d7c5af30cef60fda12c500af66687.png)](https://gyazo.com/f28d7c5af30cef60fda12c500af66687)
- 部屋掲載機能(非同期通信画像削除、掲載手順チェックマーク)
[![Image from Gyazo](https://i.gyazo.com/0aa1072eeaf179c29336f3e34b8c843a.gif)](https://gyazo.com/0aa1072eeaf179c29336f3e34b8c843a)
- 部屋ページ(GoogleMAP)
[![Image from Gyazo](https://i.gyazo.com/37d006d10286c6d2eb18734ff9fc7660.gif)](https://gyazo.com/37d006d10286c6d2eb18734ff9fc7660)


# TODO LIST
- 予約
- レビュー
- 検索機能
- ホームページ

# DB設計図
## users table
|Column|Type|Options|
|------|----|-------|
|email|string|-------|
|password|string|-------|
|fullname|string|-------|
|phone_number|intger|-------|
|description|text|-------|
### Association
- has_many: rooms

## rooms table
|Column|Type|Options|
|------|----|-------|
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
- belongs_to: user
- has_many: photos

## photo table
|Column|Type|Options|
|------|----|-------|
|room_id|references|-------|
|images|text|-------|
### Association
- belongs_to: rooms


