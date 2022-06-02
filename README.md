**1. На локальном репозитории сделать ветки для:**
- Postman
- Jmeter
- CheckLists
- Bag Reports
- SQL
- Charles
- Mobile testing

```
git branch Postman && git branch Jmeter && git branch CheckLists && git branch Bag_Reports && git branch SQL && git branch Charles && git branch Mobile_testing
```

**2. Запушить все ветки на внешний репозиторий**
```
git push -u origin Postman && git push -u origin Jmeter && git push -u origin CheckLists && git push -u origin Bag_Reports && git push -u origin SQL && git push -u origin Charles && git push -u origin Mobile_testing
```

**3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта**
```
git checkout Bag_Reports
```
```
echo -e "Title: GUI вылетает при переходе на вкладку о программе\nStep1: Открываем GUI через терминал или иконку\nStep2: Вызываем основное меню переводом курсора мыши в верхнюю часть окна GUI\nStep3: Выбираем пункт меню о программе\nActualResult: GUI закрывается без предупреждеия, процессы из памяти удаляются\nExpectedResult: Открывается окно о программе с корректным содержимым" > bug_report.txt
```

**4. Запушить структуру багрепорта на внешний репозиторий**
```
git add bug_report.txt
```
```
git commit -m "new bug report"
```
```
git push
```

**5. Вмержить ветку Bag Reports в Main**
```
git merge Bag_Reports -m "merge big report"
```

**6. Запушить main на внешний репозиторий.**
```
git push
```

**7. В ветке CheckLists набросать структуру чек листа.**
```
git checkout CheckLists
```
```
nano checklist.txt
```
Вбиваем текст:

Приложение открывается.  
Окно приложения перемещается при помощи мыши.  
Окно приложения меняет размер при помощи мыши.  
Окно приложения увеличивается на полный экран по кнопке "Развернуть на полный экран".  
Окно приложения уменьшается до предыдущего размера по кнопке "Уменшить до размера окна".  
Окно приложения сворачивается на панель задачь по кнопке "Свернуть".  
Окно приложения разворачивается на предыдущее состояние по нажатию иконки приложения в панели задач.  
Все кнопки в окне приложения нажимаются.  

Сохраняем и закрываем.

**8. Запушить структуру на внешний репозиторий**
```
git add checklist.txt
```
```
git commit -m "add checklist"
```
```
git push
```

**9. На внешнем репозитории сделать Pull Request ветки CheckLists в main**

Зайти в ветку Checklist на репозитории, нажать Copmare & Pull request  
Вписать коммент и нажать Create pull request  
Merge pull request  
Confirm merge  

**10. Синхронизировать Внешнюю и Локальную ветки Main**
```
git checkout main
```
```
git pull
```
