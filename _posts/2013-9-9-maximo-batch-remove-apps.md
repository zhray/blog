---
layout: post
title: "maximo批量删除应用"
tagline: "maximo批量删除应用"
description: "maximo批量删除应用"
tags: [maximo]
---
{% include JB/setup %}


    declare
        cursor c_data is
        select * from maxapps
        where description in ('appname1', 'appname2'); -- 这里输入要删除的应用的名称
        
        c_row c_data%rowtype;
    begin
        for c_row in c_data loop
            delete from maxapps where app=c_row.app;
            delete from maxpresentation where app=c_row.app;
            delete from sigoption where app=c_row.app;
            delete from applicationauth where app=c_row.app;
            delete from maxlabels where app=c_row.app;
            delete from maxmenu where moduleapp=c_row.app and menutype !='MODULE';
            delete from maxmenu where moduleapp=c_row.app and elementtype='APP' and keyvalue=c_row.app;
        end loop;
    end;
