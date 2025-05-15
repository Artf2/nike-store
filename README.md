<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Магазин кроссовок Nike</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100">
  <!-- Боковая панель -->
  <div class="flex">
    <div id="sidebar" class="w-64 bg-white h-screen p-5 shadow fixed top-0 left-0 transform -translate-x-full transition-transform duration-300">
      <h2 class="text-xl font-bold mb-4">Меню</h2>
      <ul class="space-y-4">
        <li><a href="#" class="block text-gray-700 hover:text-blue-500">Главная</a></li>
        <li><a href="#" class="block text-gray-700 hover:text-blue-500">Каталог</a></li>
        <li><a href="#" class="block text-gray-700 hover:text-blue-500">Корзина</a></li>
        <li><button onclick="openModal('loginModal')" class="block text-gray-700 hover:text-blue-500">Вход</button></li>
        <li><button onclick="openModal('registerModal')" class="block text-gray-700 hover:text-blue-500">Регистрация</button></li>
      </ul>
    </div>

    <div class="flex-1 ml-0 md:ml-0">
      <!-- Верхняя панель -->
      <div class="flex justify-between items-center bg-white p-4 shadow-md">
        <button onclick="toggleSidebar()" class="text-2xl">
          <i class="fas fa-bars"></i>
        </button>
        <div class="flex items-center gap-4">
          <button onclick="openModal('loginModal')" class="text-gray-700 hover:text-blue-500 flex items-center">
            <i class="fas fa-user mr-2"></i> Вход / Регистрация
          </button>
        </div>
      </div>

      <!-- Контент -->
      <div class="p-6">
        <h1 class="text-3xl font-bold">Добро пожаловать в магазин Nike!</h1>
      </div>
    </div>
  </div>

  <!-- Модальные окна -->
  <div id="loginModal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center">
    <div class="bg-white p-6 rounded-lg w-80">
      <h2 class="text-xl font-bold mb-4">Вход</h2>
      <input type="email" placeholder="Email" class="w-full mb-3 p-2 border rounded">
      <input type="password" placeholder="Пароль" class="w-full mb-3 p-2 border rounded">
      <div class="flex justify-between">
        <button class="bg-blue-500 text-white px-4 py-2 rounded">Войти</button>
        <button onclick="closeModal('loginModal')" class="text-gray-500">Отмена</button>
      </div>
    </div>
  </div>

  <div id="registerModal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center">
    <div class="bg-white p-6 rounded-lg w-80">
      <h2 class="text-xl font-bold mb-4">Регистрация</h2>
      <input type="text" placeholder="Имя" class="w-full mb-3 p-2 border rounded">
      <input type="email" placeholder="Email" class="w-full mb-3 p-2 border rounded">
      <input type="password" placeholder="Пароль" class="w-full mb-3 p-2 border rounded">
      <div class="flex justify-between">
        <button class="bg-green-500 text-white px-4 py-2 rounded">Зарегистрироваться</button>
        <button onclick="closeModal('registerModal')" class="text-gray-500">Отмена</button>
      </div>
    </div>
  </div>

  <script>
    function toggleSidebar() {
      const sidebar = document.getElementById('sidebar');
      sidebar.classList.toggle('-translate-x-full');
    }

    function openModal(id) {
      document.getElementById(id).classList.remove('hidden');
    }

    function closeModal(id) {
      document.getElementById(id).classList.add('hidden');
    }
  </script>
</body>
</html>

