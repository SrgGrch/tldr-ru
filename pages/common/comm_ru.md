# comm

> Выбирает или отсеивает строки, общие для двух файлов. Оба файла должны быть отсортированы.

- Выводит три колонки, разделенные табуляцией: строки из первого файла, которых нет во втором; строки из второго файла, которых нет в первом; общие строки:

`comm {{file1}} {{file2}}`

- Печатает только общие строки:

`comm -12 {{file1}} {{file2}}`

- Печатает только общие строки, читая один файл из стандартного ввода:

`cat {{file1}} | comm -12 - {{file2}}`

- Получает строки, которые есть только в первом файле, сохраняя результат в третий файл:

`comm -23 {{file1}} {{file2}} > {{file1_only}}`

- Печатает строки, которые есть только во втором файле, когда файлы не отсортированы:

`comm -13 <(sort {{file1}}) <(sort {{file2}})`
