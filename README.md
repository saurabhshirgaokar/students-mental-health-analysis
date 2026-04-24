# 📊 Analyzing Students' Mental Health

## 📖 Overview

This project analyzes how the **length of stay** impacts the mental health of international students using diagnostic scores.

## 🎯 Objective

To evaluate trends in:

* Depression (PHQ-9)
* Social Connectedness (SCS)
* Acculturative Stress (ASISS)

## 📊 Dataset

* Source: DataCamp
* Filter: International students only

## 🛠️ Tools

* SQL

## 🧾 Analysis Query

```sql
SELECT stay,
       COUNT(*) AS count_int,
       ROUND(AVG(todep),2) AS average_phq,
       ROUND(AVG(tosc),2) AS average_scs,
       ROUND(AVG(toas),2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;
```

## 📈 Key Insights

* Shorter stays show higher depression scores
* Social connectedness improves with time
* Stress levels decrease as students adapt

## 📌 Conclusion

Length of stay plays a significant role in mental health outcomes of international students.

