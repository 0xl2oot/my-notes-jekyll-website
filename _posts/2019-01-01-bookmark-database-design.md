---
layout: post
title:  "收藏夹网站数据库设计"
description: ""
category: "数据库"
tags: ["database", "MySQL", "数据库"]
date:   2019-11-01 15:00:00 +0800
---

```sql

-- 用户表
create table `user` (
    `id` bigint(20) not null auto_increment,
    `email` varchar(255) not null,
    `user_name` varchar(64) not null,
    `password` varchar(255) not null,
    `introduction` text comment '个人介绍',
    `avatar` varchar(255) not null comment '头像地址',
    `create_time` timestamp not null default current_timestamp comment '创建时间',
    `update_time` timestamp not null default current_timestamp on update current_timestamp comment '修改时间',
    primary key (`id`),
    unique key `uk_email` (`email`),
    unique key `uk_user_name` (`user_name`)
);

-- 文件夹表
create table `folder` (
    `id` bigint(20) not null auto_increment,
    `name` varchar(64) not null comment '名称',
    `description` text not null,
    `user_id` bigint(20) not null,
    `is_public` unsigned tinyint not null comment '是否公开，0为否，1为是',
    `create_time` timestamp not null default current_timestamp comment '创建时间',
    `update_time` timestamp not null default current_timestamp on update current_timestamp comment '修改时间',
    `star` unsigned int not null default 0 comment '总点赞数', 
    `follow` unsigned int not null default 0 comment '收藏数',
    primary key (`id`)
);

-- 书签表
create table `bookmark` (
    `id` bigint(20) not null auto_increment,
    `url` varchar(255) not null,
    `title` varchar(255) not null,
    `pic` varchar(255) not null,
    `description` text not null,
    `folder_id` bigint(20) not null,
    `create_time` timestamp not null default current_timestamp comment '创建时间',
    `update_time` timestamp not null default current_timestamp on update current_timestamp comment '修改时间',
    `star` unsigned int not null default 0,
    primary key (`id`)
);

-- 点赞表
create table `praise` (
    `id` bigint(20) not null auto_increment,
    `url_id` bigint(20) not null,
    `user_id` bigint(20) not null,
    `create_time` timestamp not null default current_timestamp comment '创建时间',
    primary key (`id`),
    unique key `uk_url_user_id` (`url_id`, `user_id`)
);

-- follow 表
create table `follow` (
    `id` bigint(20) not null auto_increment,
    `folder_id` bigint(20) not null,
    `user_id` bigint(20) not null,
    `create_time` timestamp not null default current_timestamp comment '创建时间',
    primary key (`id`)
);


```