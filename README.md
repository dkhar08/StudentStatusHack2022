# StudentStatusHack2022
Цифровой прорыв 2022. Алтайский край. 3rd place private leaderboard solution.

The challenge of this competition was to predict students' status after a year of education. Altai State University provided data. There are three types of statuses: ok, expelled, and got a sabbatical. Data contained information about something around 13k students from different years.

Let's look at the pictures.

1st of them depicts how status depends on the number of a group. 2nd - from a number of people who have the same group.

These two fields look like data leaks. It looks like organizers tried to balance classes by adding only expelled students from some groups. Or of course, it could be just unfortunate directions of study. Anyway, those two features were allowed to distinguish ok and expelled students with high quality.

To distinguish got-a-sabbatical students from others took a great deal of work. It was a small class containing only 614 students. A metric of the competition was f1 macro. That 2 notices led to the fact that small disturbances in get-a-sabbatical predictions engendered high changes in the final metric. As a result cross validation had a vast variance. The public leader board also had:). To tackle the variance problem I used some ideas from the Mercedez Bentz competition. For my validation, I used 5 fixed 5-fold splits(25 fixed folds in total). It allowed me to correctly select features and hyperparameters. As other participants suffered from reshuffle, I just slipped from 2nd public to 3rd private and got one of the main prizes.
