# PhotoSpaceのER図

## users テーブル
  
email (string型,NOT NULL)
<br>
password  (string型,NOT NULL)
<br>
name (string型,NOT NULL)
<br>
profile (text型,NOT NULL)
<br>
occupation (text型,NOT NULL)
<br>
position (text型,NOT NULL)

### Association

- has_many :prototypes
- has_many :comments

## prototypes テーブル
title (string型,NOT NULL)
<br>
catch_copy (text型,NOT NULL)
<br>
concept (text型,NOT NULL)
<br>
image (ActiveStorageで実践)
<br>
user (references型)

### Association

- belongs to :users
- has_many :comments

## comments テーブル

text (text型,NOT NULL)
<br>
user (references型)
<br>
prototype (references型)

### Association

- belongs_to :users
- belongs_to :prototypes
