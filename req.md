# 🎮 Gaming Guide Site

## Project Overview

Gaming Guide Site нь League of Legends тоглоом сонирхогчдод зориулсан REST API веб систем юм.

Энэхүү системээр хэрэглэгчид League of Legends-ийн champion, item, rune, spell болон тоглолтын guide мэдээллийг үзэх боломжтой.

Хэрэглэгчид өөрсдийн guide үүсгэх, засах, устгах боломжтой бөгөөд бусад тоглогчдын guide-г унших боломжтой.

Төслийн гол зорилго нь Authentication, Authorization, CRUD үйлдлүүдийг практик дээр хэрэгжүүлэхэд оршино.

Систем нь MVC архитектур ашигласан монолит бүтэцтэй бөгөөд beginner fullstack хөгжүүлэгчдэд зориулсан.


# Main Features

## User System

Хэрэглэгч:
- Бүртгүүлэх
- Нэвтрэх
- Profile удирдах
- Өөрийн guide үүсгэх
- Guide засах
- Guide устгах
- Guide харах боломжтой.


## League of Legends Content

Системд дараах тоглоомын мэдээллүүд байна.


### Heroes (Champions)

Champion мэдээлэл хадгална.

Мэдээлэл:
- Name
- Image
- Description
- Role
- Difficulty
- Champion type


Role:
- Top
- Jungle
- Mid
- ADC
- Support


### Skills

Champion-ийн чадварууд хадгалагдана.

Мэдээлэл:
- Skill name
- Description
- Damage
- Cooldown
- Mana cost
- Skill type


### Spells

Summoner spell мэдээлэл байна.

Жишээ:
- Flash
- Ignite
- Heal
- Teleport


Мэдээлэл:
- Name
- Description
- Cooldown


### Runes

Rune мэдээлэл хадгална.

Мэдээлэл:
- Rune name
- Type
- Description
- Recommended role


### Items

Item мэдээлэл хадгална.

Мэдээлэл:
- Item name
- Price
- Description
- Stats
- Recommended champion



# User Roles (Authorization)


## Admin

Бүх системийг удирдах эрхтэй.

Эрх:
- User удирдах
- Hero CRUD хийх
- Skill CRUD хийх
- Item CRUD хийх
- Rune CRUD хийх
- Spell CRUD хийх
- System statistics харах


## Editor

Контент засварлах эрхтэй.

Эрх:
- Hero нэмэх
- Skill нэмэх
- Item нэмэх
- Rune нэмэх
- Guide засах


## User

Энгийн хэрэглэгч.

Эрх:
- Guide унших
- Hero харах
- Item харах
- Rune харах
- Comment хийх
- Favorite хадгалах



# Database Structure

Систем дараах үндсэн entity-үүдээс бүрдэнэ.


## Users

Хэрэглэгчийн мэдээлэл хадгална.

Fields:
- id
- username
- email
- password_hash
- role
- created_at
- is_deleted


## Heroes

League of Legends champion мэдээлэл хадгална.

Fields:
- id
- name
- description
- role
- difficulty
- image


## Skills

Hero-ийн skill мэдээлэл хадгална.

Fields:
- id
- hero_id
- name
- description
- cooldown


## Items

Item мэдээлэл хадгална.

Fields:
- id
- name
- price
- description


## Runes

Rune мэдээлэл хадгална.

Fields:
- id
- name
- type
- description


## Spells

Spell мэдээлэл хадгална.

Fields:
- id
- name
- description


## Guides

User-ийн бичсэн guide хадгална.

Fields:
- id
- user_id
- hero_id
- title
- content
- created_at



# Security

Систем JWT Authentication ашиглана.

Нууц үгийг шууд хадгалахгүй.

bcrypt ашиглан hash хэлбэрээр хадгална.

Authorization нь Role-Based Access Control ашиглана.

Role:
- Admin
- Editor
- User


Soft delete ашиглана.

Өгөгдлийг шууд устгахгүй.

is_deleted талбараар тэмдэглэнэ.



# API Modules

Төсөл дараах модулиудаас бүрдэнэ:

- Authentication Module
- Profile Module
- Hero Management Module
- Skill Management Module
- Item Management Module
- Rune Management Module
- Spell Management Module
- Guide Management Module
- Admin Module


Нийт:
20-40 REST API endpoint байна.


# Development Plan

1. Database schema үүсгэх
2. MVC project structure хийх
3. JWT Authentication хийх
4. Role Authorization хийх
5. Hero CRUD хийх
6. Skill CRUD хийх
7. Item CRUD хийх
8. Rune CRUD хийх
9. Spell CRUD хийх
10. Guide CRUD хийх
11. Admin хэсэг хийх
12. API testing хийх


# Conclusion

Gaming Guide Site нь REST API, MVC архитектур, JWT Authentication, Role-Based Authorization болон CRUD ажиллагааг сурахад тохиромжтой beginner түвшний төсөл юм.

Ирээдүйд:
- Comment system
- Tier List
- Champion Build
- Match History
- Ranking system

зэрэг нэмэлт боломжууд хөгжүүлэх боломжтой.