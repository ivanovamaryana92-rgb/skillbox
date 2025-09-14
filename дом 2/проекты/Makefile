.PHONY: show_cases run_tests activate_env install

# Активация корректного окружения
activate_env:
	conda activate test_env_correct

# Показать все тест кейсы
show_cases:
	pytest --collect-only -q

# Запуск тестов
run_tests:
	pytest --reruns 1 --reruns-delay 2 -v --tb=short --no-header

# Установка зависимостей
install:
	conda env create -f environment_correct.yml
	conda activate test_env_correct

# Очистка кэша pytest
clean:
	find . -name "*.pyc" -delete
	find . -name "__pycache__" -delete
	rm -rf .pytest_cache