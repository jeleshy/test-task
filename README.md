#### Файлы для тестов:

1. conftest.py, в котором определяется браузер и страница;
2. page_objects.py, в котором определяется класс страницы EcoImpact и содержатся методы, необходимые для ее тестирования;
3. test_eco_impact.py, в котором лежат авто-тесты для блока с эко-счетчиками страницы EcoImpact.

#### Для работы со скриптом нужно: 

1. Склонировать этот репозиторий себе на компьютер;
git clone git@github.com:jeleshy/avito-test-task.git
При возникновении ssh-ошибок, нужно добавить публичный ssh-ключ к Вашему gitHub аккаунту. Подробнее про [привязку](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) ssh-ключа и про его [генерацию](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

2. Установить [python](https://www.python.org/about/gettingstarted), [pytest](https://docs.pytest.org/en/8.2.x/getting-started.html) и [playwright](https://playwright.dev/python/docs/intro);

3. В файле conftest.py можно выбрать браузер для тестирования - Chrome (chromium), Mozilla (mozilla) или Safari (webkit). Уберите значок `#` у нужного для тестирования. `Одновременно может использоваться только один браузер, остальные должны быть со значком #, например #browser = p.firefox.launch()`;

4. Запустить `pytest` с помощью команды `pytest` (или `pytest -s test_eco_impact.py`, чтобы видеть принты в терминале - если менять номера эко-счетчиков на несуществующие, к примеру);

5. После этого в терминале появится сообщение о пройденных/непройденных тестах, а в папке `outro` - скриншоты эко-счетчиков.