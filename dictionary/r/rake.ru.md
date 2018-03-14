# Rake
2018-03-12
23:24

[Rake](https://sites.google.com/site/sitsiliyaror/blogs/rake)


[Команды Rake](https://sites.google.com/site/sitsiliyaror/blogs/komandy-rake)

## Команды Rake

`rake about`
Список версий всех rails framework и окружающей среды

`rake db:create`
Создание базы данных из config/database.yml для текущего Rails.env (используйте `db:create:all` чтобы создать все базы данных из конфига)

`rake db:drop` 
	# Drops the database for the current Rails.env (use db:drop:all to drop all databases)

`rake db:fixtures:load`
	# Load fixtures into the current environment's database.

`rake db:migrate`
	Миграция базы данных с помощью сценария в db/migrate (опции: VERSION=x, VERBOSE=false).

`rake db:migrate_plugins RAILS_ENV=production`
	Запуск миграций для production версии

`rake db:migrate:status`  # Display status of migrations
`rake db:rollback`        # Rolls the schema back to the previous version (specify steps w/ STEP=n).
`rake db:schema:dump`     # Create a db/schema.rb file that can be portably used against any DB supported by AR
`rake db:schema:load`     # Load a schema.rb file into the database
rake db:seed            # Load the seed data from db/seeds.rb
rake db:setup           # Create the database, load the schema, and initialize with the seed data (use db:reset to also drop the db first)
rake db:structure:dump  # Dump the database structure to an SQL file
rake db:version         # Retrieves the current schema version number
rake doc:app            # Generate docs for the app -- also availble doc:rails, doc:guides, doc:plugins (options: TEMPLATE=/rdoc-template.rb, TITLE="Cus...
rake log:clear          # Truncates all *.log files in log/ to zero bytes
rake middleware         # Prints out your Rack middleware stack
rake notes              # Enumerate all annotations (use notes:optimize, :fixme, :todo for focus)
rake notes:custom       # Enumerate a custom annotation, specify with ANNOTATION=CUSTOM
rake rails:template     # Applies the template supplied by LOCATION=/path/to/template
rake rails:update       # Update both configs and public/javascripts from Rails (or use just update:javascripts or update:configs)
rake routes             # Print out all defined routes in match order, with names.
rake secret             # Generate a cryptographically secure secret key (this is typically used to generate a secret for cookie sessions).
rake stats              # Report code statistics (KLOCs, etc) from the application
rake test               # Runs test:units, test:functionals, test:integration together (also available: test:benchmark, test:profile, test:plugins)
rake test:recent        # Run tests for recenttest:prepare / Test recent changes
rake test:uncommitted   # Run tests for uncommittedtest:prepare / Test changes since last checkin (only Subversion and Git)
rake time:zones:all     # Displays all time zones, also available: time:zones:us, time:zones:local -- filter with OFFSET parameter, e.g., OFFSET=-6
rake tmp:clear          # Clear session, cache, and socket files from tmp/ (narrow w/ tmp:sessions:clear, tmp:cache:clear, tmp:sockets:clear)
`rake tmp:create`  # Creates tmp directories for sessions, cache, sockets, and pids
	- `rake db:fixtures:load` - Загрузить fixtures в базу данных текущего окружения(Rails.env). Можно добавить параментр `FIXTURES=` и список определённых fixtures( пример `rake db:fixtures:load FIXTURES=user,post` )
	- `rake db:drop` - Удалить(дропнуть) текущую БД
	- `rake db:drop:all` - Удалить(дропнуть) все БД указаные в настройках config/database.yml
		`rake db:create` - Создать БД
		rake db:create:all - Создаёт все БД из настроек в файле config/database.yml
		rake db:migrate - Выполняет миграции используя скрипты из папки db/migrate. Можно указать версию миграции добавив ключ VERSION=
		rake db:migrate:down - Выполняет откат миграции до версии указаной в ключе VERSION
		rake db:migrate:up - Выполняет миграцию до версии указаной в ключе VERSION ( последовательность - от более старой, текущей, до более новой, указаной в ключе VERSION )
		rake db:migrate:redo - Откатить одну миграцию и выполнить её заново ( эквивалентно rake db:rollback, rake db:migrate ). Если указан ключ VERSION выполнит rake db:migrate:down, rake db:migrate:up
		rake db:migrate:rollback - Откатить схему на одну миграцию назад
		rake db:migrate:status - Отображает статус миграций
		rake db:migrate:reset - Сбрасывает БД, создаёт и выполняет все миграции ( на деле - rake db:drop, rake db:create, rake db:migrate )
		rake db:forward - Переводит схему на следующую версию ( определить шаги можно ключем STEP=n )
		rake db:charset - Возвращает кодировку БД
		rake db:collation - Возвращает способ сравнения слов и букв( collation ) для БД из текущего окружения
		rake db:version - Возвращает текущую версию схемы
		rake db:abort_if_pending_migrations - Вызывает исключение ( exception ) если имеются миграции, ожидающие выполнения
		rake db:seed - Выполняет файл db/seeds.rb в который обычно ложат скрипт заполнения БД тестовыми данными
		rake db:setup - Эквивалентно выполнению следующей цепочки комманд: rake db:create, rake db:schema:load, rake db:seed
		rake db:schema:dump - Создаёт db/schema.rb файл из текущей схемы базы данных
		rake db:schema:load - Загрузить db/schema.rb в базу данных
		rake db:sessions:clear - Очистить таблицу сессий ( в том случае, когда для хранения сессии используется база данных )
		rake db:sessions:create - Создаёт таблицу в базе данных, где будут храниться сессии ( в том случае, когда для хранения сессии используется база данных )
		rake db:structure:dump - Сохраняет структуру БД в sql файл
		rake db:test:clone - Пересоздаёт тестовую БД из схемы БД текущего окружения
		rake db:test:clone_structure - Пересоздаёт тестовую БД из схемы БД development окружения
		rake db:test:prepare - Подготовить тестовую БД, перезалив туда схему
		rake db:test:load - Пересоздать тестовую БД из текущей schema.rb
		rake db:test:clone - Выполняет поочерёдно rake db:schema:dump, rake db:test:load
		rake db:test:purge - Очистить тестовую БД
		rake db:test:clone_structure - Пересоздатьтестовую БД из структуры development БД
		rake doc:app - Создать HTML-версию документации вашего приложения
		rake doc:clobber_app - Удалить документацию, сгенерированную rdoc
		rake doc:clobber_rails - Удалить документацию, сгенерированную rdoc
		rake doc:clobber_plugins - Удалить документацию плагинов
		rake doc:plugins - Сгенерировать HTML-версию документации для всех установленых плагинов
		rake doc:rails - Создать HTML-версию документации по rails
		rake doc:reapp - Принудительно пересоздать файлы rdoc
		rake doc:rerails - Принудительно пересоздать файлы rdoc
		rake log:clear - Урезать размер всех файлов *.log в папке log/ до 0 байт.
		rake stats - Выводит отчёт по статистике кода вашего приложения
		rake test - Запустить все тесты ( functional, unit, performance и integration ) из папки test/
		rake test:functionals - Запустить все functional тесты ( тесты контроллеров )
		rake test:integration - Запустить все integration тесты ( тесты вьюх )
		rake test:units - Запустить все unit тесты ( тесты моделей )
		rake test:plugins - Запустить тесты установленных плагинов
		rake tmp:cache:clear - Удалить все файлы и папки в папке tmp/cache/
		rake tmp:clear - Очистить папки session, cache, и socket в папке tmp/
		rake tmp:create - Создать папки session, cache, и socket в папке tmp/
		rake tmp:sessions:clear - Очистить все файлы в папке tmp/sessions/
		rake tmp:sockets:clear - Очистить все файлы ruby_sess.* в папке tmp/sessions/