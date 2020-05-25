# README

# NAME: AIRSTAY vacation rental platform

# Description
自身の経歴したAIRBNBホスト時代に運営したプラットフォームに感銘を受け、
現在トレンドでもあるP2Pビジネスの形態の一つとして、
シェアリングエコノミープラットフォームを作ることに試みました。
現在進行中。
https://qiita.com/YANG_LIU

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
|email|string|null: false|
|password|string|null: false|
|fullname|string|null: false|
|phone_number|intger|null: false|
|description|text|null: false|
### Association
- has_many: rooms

## rooms table
|Column|Type|Options|
|------|----|-------|
|home_type|string|null: false|
|room_type|string|null: false|
|accommodate|integer|null: false|
|bed_room|integer|null: false|
|bath_room|integer|null: false|
|listing_name|string|null: false|
|summary|text|null: false|
|address|text|null: false|
|is_tv|boolean|null: false|
|is_kitchen|boolean|null: false|
|is_aircon|boolean|null: false|
|is_heating|boolean|null: false|
|is_internet|boolean|null: false|
|price|integer|null: false|
|active|boolean|null: false|
|latitude|float|null: false|
|longitude|float|null: false|
|user|references|foreign_key: true|
### Association
- belongs_to: user
- has_many: photos

## photo table
|Column|Type|Options|
|------|----|-------|
|room_id|references|null: false|
|images|text|null: false|
### Association
- belongs_to: rooms


