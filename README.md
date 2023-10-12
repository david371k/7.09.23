## задание 1
```
select name from person order by name
```
![Exercise 01](https://github.com/david371k/7.09.23/assets/144510921/d6ea8fa8-3b61-4066-adc1-0e4760afb6ab)

## задание 2
```
create view v_generated_dates as 
select generate_series ('2022-01-01','2022-01-31', interval '1 day')::date
```
![Exercise 02](https://github.com/david371k/7.09.23/assets/144510921/01f6624c-feac-43d2-b749-d8446829f994)

## задание 3
```
SELECT * FROM v_generated_dates
where generate_series not in (select visit_date from person_visits)
order by generate_series
```
![image](https://github.com/david371k/7.09.23/assets/144510921/ff371521-7076-4e69-816f-f1cdfb7acf29)

## задание 4
```
select  person_id from r except all select  person_id from s
union all
(select  person_id from s except all select  person_id from r)
```
![image](https://github.com/david371k/7.09.23/assets/144510921/fb2f0f6f-8a3b-4701-9089-546806e1021d)

## задание 5
```
select m.pizza_name, p.name, m.price,(m.price * 0.9) as discovnt_price from person_order po
join person p on p.id= po.person_id
join menu m on m.id =po.menu_id
```
![image](https://github.com/david371k/7.09.23/assets/144510921/fc834f2c-d0bb-45b5-83e4-b2c0ef146f5c)

## задание 6


