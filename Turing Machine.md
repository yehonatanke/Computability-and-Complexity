<h1 align="center"> מכונת טיורינג - הערות </h1>

### בעיית העצירה $A_{TM}$
הניסוח המתמטי של בעיית העצירה $A_{TM}$:

${A_{TM} = \{ \langle M, w \rangle \mid M \text{ is a Turing machine and stops at } w \}}$

### הסבר לסימון
הסימון $\langle M, w \rangle$ מציין זוג מקודד של מכונת טיורינג $M$ וקלט $w$. המשמעות של הקידוד היא שצמד המידע הזה, המכיל גם את התיאור של מכונת הטיורינג $M$ וגם את הקלט $w$, מקודד כמחרוזת אחת שניתן להזין למכונת טיורינג אחרת.

### מרכיבי מכונת טיורינג:
1. **סרט אינסופי**: הסרט מחולק לתאים, שכל אחד מהם יכול להכיל סימן כלשהו מתוך אלפבית סופי.
2. **ראש קריאה/כתיבה**: הראש נע על פני הסרט, תא אחד בכל פעם, והוא יכול לקרוא את הסימן בתא הנוכחי ולכתוב בו סימן חדש.
3. **מצבי מכונה**: למכונת הטיורינג יש סט מוגבל של מצבים שהיא יכולה להיות בהם. אחד מהמצבים הללו הוא מצב התחלתי, ויש גם מצבי קבלה ודחייה.
4. **לוח הוראות**: אוסף של הוראות שמכתיבות את פעולתה של המכונה. כל הוראה מציינת מה לעשות בהתחשב במצב הנוכחי של המכונה ובסימן הנקרא מהסרט.

### איך מכונת טיורינג עובדת?
1. **התחלה**: המכונה מתחילה במצב התחלתי עם ראש הקריאה/כתיבה הממוקם בתא הראשון של הסרט.
2. **קריאה ופעולה**: המכונה קוראת את הסימן בתא הנוכחי של הסרט, בהתאם לסימן ולמצב הנוכחי, היא מבצעת את ההוראה הרלוונטית (כגון כתיבת סימן חדש, מעבר לתא הבא, ושינוי המצב).
3. **חזרה**: התהליך נמשך עד שהמכונה נכנסת למצב קבלה (מפסיקה בהצלחה) או למצב דחייה (מפסיקה בכישלון).

### מהו קלט?
הקלט למכונת הטיורינג הוא סדרת סימנים שמוכנסת בתחילת העבודה של המכונה על הסרט. הקלט מכיל את המידע שהמכונה אמורה לעבד.

### דוגמה פשוטה:
נניח שיש לנו מכונת טיורינג שנועדה לבדוק אם מחרוזת מסוימת מכילה מספר זוגי של אפסים (0s).
1. **הקלט**: המחרוזת "110100".
2. **התחלה**: המכונה מתחילה במצב התחלתי וקוראת את התו הראשון.
3. **תהליך**: המכונה עוברת על המחרוזת ומונה את מספר האפסים.
4. **סיום**: אם היא מוצאת מספר זוגי של אפסים, היא נכנסת למצב קבלה, אחרת למצב דחייה.

### אינטראקציה בין ראש הקריאה/כתיבה לסרט

1. **קריאה**: ראש הקריאה/כתיבה קורא את הסימן בתא הנוכחי שבו הוא נמצא.
2. **ביצוע הוראה**: בהתאם לסימן הנקרא ולמצב הנוכחי של המכונה, המכונה מבצעת את ההוראה המתאימה מתוך לוח ההוראות שלה. הוראה זו כוללת שלושה מרכיבים:
   - **כתיבה**: שינוי הסימן בתא הנוכחי לסימן אחר, כפי שמוגדר בהוראה. הסימן החדש יכול להיות אותו סימן שהיה קודם או סימן שונה.
   - **תזוזה**: הזזת ראש הקריאה/כתיבה לתא הבא, שמאלה או ימינה, או השארתו באותו מקום.
   - **שינוי מצב**: מעבר למצב חדש, כפי שמוגדר בהוראה.

### דוגמה פשוטה:
נניח שיש לנו מכונת טיורינג עם ההוראות הבאות:
- אם המכונה במצב $q_0$ וקוראת '1', היא כותבת '0', זזה ימינה ועוברת למצב $q_1$.
- אם המכונה במצב $q_1$ וקוראת '0', היא כותבת '1', זזה שמאלה ועוברת למצב $q_0$.

### תהליך עבודה:
1. **התחלה**: המכונה מתחילה במצב $q_0$ וראש הקריאה/כתיבה ממוקם בתא הראשון של הסרט, המכיל את המחרוזת "101".
2. **קריאה ראשונית ושינוי**: ראש הקריאה/כתיבה קורא את הסימן '1' בתא הראשון.
   - ההוראה במצב $q_0$ קובעת לכתוב '0' בתא זה, לזוז ימינה לתא הבא ולעבור למצב $q_1$.
3. **מצב חדש וקריאה נוספת**: עכשיו המכונה במצב $q_1$ וראש הקריאה/כתיבה נמצא בתא השני, שקודם הכיל '0'.
   - ההוראה במצב $q_1$ קובעת לכתוב '1' בתא זה, לזוז שמאלה לתא הקודם ולעבור למצב $q_0$.
4. **המשך התהליך**: התהליך ממשיך באופן דומה לפי ההוראות עד שהמכונה מגיעה למצב קבלה או דחייה, או אם היא נכנסת ללולאה אינסופית.

### סיכום
היכולת של מכונת טיורינג לשנות את הסרט היא חיונית לפעולתה. השינויים בסרט נעשים בהתאם להוראות המבוססות על הסימן הנקרא והמצב הנוכחי של המכונה. תהליך זה מאפשר למכונת טיורינג לבצע חישובים מורכבים ולפתור בעיות אלגוריתמיות.
