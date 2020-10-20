テーブル設計

users テーブル

|  Column    | Type   | Options     |
| ---------- | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

Association
- has_many :comments
- has_many :prototypes


comment テーブル

|  Column    | Type       | Options     |
| ---------- | ---------- | ----------- |
| text       | text       | null: false |
| user       | references | null: false |
| prototype  | references | null: false |

Association

- belongs_to :user
- belongs_to :prototype


prototypes テーブル

|  Column    | Type       | Options     |
| ---------- | ---------- | ----------- |
| title      | string     | null: false |
| catch_copy | text       | null: false |
| concept    | text       | null: false |
| image      |            | null: false |
| user       | references | null: false |

Association

- belongs_to :user
- has_many :comments
