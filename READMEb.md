# Query con GROUP BY

## QUERY 1

```sql
-- Contare quanti iscritti ci sono stati ogni anno --
SELECT YEAR(enrolment_date) ,COUNT(*) FROM `students` GROUP BY YEAR(enrolment_date);

```

## QUERY 2

```sql
-- Contare gli insegnanti che hanno l'ufficio nello stesso edificio --
SELECT COUNT(`id`) AS `number_address`, `office_address` FROM `teachers` GROUP BY `office_address`;
```

## QUERY 3

```sql
-- 3. Calcolare la media dei voti di ogni appello d'esame --
SELECT `exam_id`,AVG(`vote`) FROM `exam_student` GROUP BY `exam_id`;
```

## QUERY 4

```sql
--Contare quanti corsi di laurea ci sono per ogni dipartimento  --
SELECT `departments`.`name`,COUNT(`degrees`.`id`) AS `total_courses`
FROM `departments`
JOIN `degrees` ON `departments`.`id`=`degrees`.`department_id` GROUP BY `departments`.`name`;
```
