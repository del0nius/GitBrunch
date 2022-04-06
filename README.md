1. На локальном репозитории сделать ветки для:
- Postman — `git branch Postman`
- Jmeter — `git branch Jmeter`
- CheckLists — `git branch CheckLists`
- Bag Reports — `git branch Bug_Reports`
- SQL — `git branch SQL`
- Charles — `git branch Charles`
- Mobile testing — `git branch Mobile_testing`
2. Запушить все ветки на внешний репозиторий — `git push -u origin --all`
3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта — `git checkout Bug_Reports`
```
cat > bug_report.txt
Bug ID
Bug Name
Summary
Submit Date
Reporter
Operating System
Browser
URL
Description
Steps to reproduce
Expected result
Actual result
Screenshot
Enter (Ctrl+D)
```
4. Запушить структуру багрепорта на внешний репозиторий — `git add bug_report.txt ; git commit -m bug_report.txt ; git push`
5. Вмержить ветку Bag Reports в Main — `git checkout main ; git merge Bug_Reports`
6. Запушить main на внешний репозиторий. — `git push`
7. В ветке CheckLists набросать структуру чек листа. — `git checkout CheckLists`
```
cat > check_list.txt
ID
Product
Tester
Date
Module
Procedure
Expected result
Pass/Fail
Actual result
Comment
Enter (Ctrl+D)
```
8. Запушить структуру на внешний репозиторий — `git add check_list.txt ; git commit -m check_list.txt ; git push`
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main
- go to github.com and log in, open "GitBrunch" repository
- chose "CheckLists" branch
- click "Contribute" and "Open pull request"
- click "Create pull request", after that click "Merge pull request" and "Merge"
10. Синхронизировать Внешнюю и Локальную ветки Main — `git checkout main ; git pull`