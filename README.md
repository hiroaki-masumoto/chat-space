# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key:true|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|

## Association
- has_many :chats
- has_many :groups

## chatsテーブル

|Column|Type|Options|
|------|----|-------|
|chat_id|integer|null:false, fareign_key:true|
|text|text||
|image|text||
|user_id|integer|null: false, foreign_key:true|

## Association
- belongs_to :user

## groupテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key:true|
|groupname|string|null :false|

## Association
- belongs_to: user

## group_usersテーブル
|Column|Type|Options|
|------|----|-------|
|member_id|integer|null: false, foreign_key:true|
|user_id|integer|null: false, foreign_key:true|

## Association 
- belongs_to: user
- belongs_to: group