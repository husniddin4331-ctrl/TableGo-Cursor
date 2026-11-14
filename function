(function () {
  var STORAGE = "tablego-records";
  var CART_KEY = "tablego-cart";
  var TABLE_KEY = "tablego-table";
  var LANG_KEY = "tablego-lang";
  var NOTE_KEY = "tablego-note";

  var dict = {
    ru: {
      nav_menu: "Меню", nav_records: "Рекорды", cart: "Корзина",
      welcome: "Добро пожаловать за стол. Садитесь поудобнее: плов из казана, шашлык с углей, тёплая лепёшка и чайник чая уже ждут вас. Отметьте блюда — и кухня начнёт готовить. Приятного аппетита",
      hero_kicker: "Электронное меню для ресторана",
      hero_title_1: "Меню на столе.", hero_title_2: "Заказ сразу на кухне.",
      hero_text: "Гость выбирает блюда и отправляет заказ. Сумма считается сама, а каждый чек остаётся в рекордах этого браузера.",
      cta_menu: "Открыть меню", cta_records: "Рекорды",
      hero_ticket_kicker: "На кухню", hero_line_1: "Салат", hero_line_2: "Плов", hero_line_3: "Напиток",
      hero_ticket_note: "Сумма считается сама",
      stat_dishes: "блюд в меню", stat_tables: "столов в зале", stat_best: "рекорд чека", stat_orders: "заказов сегодня",
      table_kicker: "Стол", table_title: "За каким вы столом?",
      table_text: "Номер попадёт в чек вместе с блюдами. Выбор запоминается в этом браузере.",
      table_current: "Сейчас стол", table_free: "свободен", table_busy: "есть чек",
      menu_kicker: "Меню", menu_title: "Выберите блюда", menu_all: "Всё", add: "Добавить",
      cat_salad: "Салаты", cat_hot: "Горячее", cat_grill: "Гриль", cat_soup: "Супы",
      cat_bake: "Выпечка", cat_drink: "Напитки", cat_sweet: "Десерты",
      records_kicker: "Рекорды", records_title: "Чеки этого браузера",
      records_text: "Заказы хранятся локально. Закрытие Cursor и блокировка компьютера их не стирают.",
      rec_count: "всего чеков", rec_pop: "популярное блюдо", rec_clear: "Очистить рекорды",
      rec_empty: "Пока пусто. Отправьте первый заказ — он станет первым рекордом.",
      rec_best: "рекорд", rec_confirm: "Удалить все сохранённые чеки в этом браузере?",
      cart_title: "Ваш заказ", cart_empty: "Пока пусто. Добавьте блюда из меню.",
      comment: "Комментарий к заказу", total: "Итого", send: "Отправить заказ",
      need_table: "Сначала выберите стол.", need_cart: "Корзина пустая.",
      saved: "Чек сохранён в рекорды", cleared: "Рекорды очищены",
      qr_kicker: "Один QR для зала", qr_title: "Гость садится и сканирует код",
      qr_text: "Код открывает это меню в вашей сети. Рекорды у каждого телефона свои: они лежат в локальном хранилище браузера."
    },
    en: {
      nav_menu: "Menu", nav_records: "Records", cart: "Cart",
      welcome: "Welcome to the table. Sit back: plov from the kazan, charcoal shashlik, warm bread and a pot of tea are waiting. Choose your dishes and the kitchen starts cooking. Enjoy your meal",
      hero_kicker: "Electronic menu for restaurants",
      hero_title_1: "The menu stays on the table.", hero_title_2: "The order reaches the kitchen.",
      hero_text: "A guest picks dishes and sends the order. The total adds itself, and every bill stays in this browser’s records.",
      cta_menu: "Open the menu", cta_records: "Records",
      hero_ticket_kicker: "To the kitchen", hero_line_1: "Salad", hero_line_2: "Plov", hero_line_3: "Drink",
      hero_ticket_note: "The total adds itself",
      stat_dishes: "dishes", stat_tables: "tables", stat_best: "record bill", stat_orders: "orders today",
      table_kicker: "Table", table_title: "Which table is this?",
      table_text: "The number is stored with the bill. This browser remembers your choice.",
      table_current: "Current table", table_free: "free", table_busy: "has a bill",
      menu_kicker: "Menu", menu_title: "Choose dishes", menu_all: "All", add: "Add",
      cat_salad: "Salads", cat_hot: "Hot", cat_grill: "Grill", cat_soup: "Soups",
      cat_bake: "Bakery", cat_drink: "Drinks", cat_sweet: "Desserts",
      records_kicker: "Records", records_title: "Bills on this browser",
      records_text: "Orders stay in local storage. Closing Cursor or locking the computer does not erase them.",
      rec_count: "bills saved", rec_pop: "popular dish", rec_clear: "Clear records",
      rec_empty: "Nothing yet. Send the first order and it becomes the first record.",
      rec_best: "record", rec_confirm: "Delete every saved bill in this browser?",
      cart_title: "Your order", cart_empty: "Nothing here yet. Add dishes from the menu.",
      comment: "Note for the kitchen", total: "Total", send: "Send order",
      need_table: "Choose a table first.", need_cart: "The cart is empty.",
      saved: "Bill saved to records", cleared: "Records cleared",
      qr_kicker: "One QR for the room", qr_title: "The guest sits down and scans",
      qr_text: "The code opens this menu on your network. Each phone keeps its own records in local storage."
    },
    uz: {
      nav_menu: "Menyu", nav_records: "Rekordlar", cart: "Savat",
      welcome: "Dasturxonga xush kelibsiz. Qulay o‘tiring: qozonda palov, ko‘mirdagi shashlik, iliq non va choynak choy sizni kutadi. Taomlarni belgilang — oshxona pishirishni boshlaydi. Yoqimli ishtaha",
      hero_kicker: "Restoran uchun elektron menyu",
      hero_title_1: "Menyu stolda.", hero_title_2: "Buyurtma oshxonada.",
      hero_text: "Mehmon taomlarni tanlab buyurtma yuboradi. Summa o‘zi hisoblanadi, har bir chek shu brauzer rekordlarida qoladi.",
      cta_menu: "Menyuni ochish", cta_records: "Rekordlar",
      hero_ticket_kicker: "Oshxonaga", hero_line_1: "Salat", hero_line_2: "Palov", hero_line_3: "Ichimlik",
      hero_ticket_note: "Summa o‘zi hisoblanadi",
      stat_dishes: "taom", stat_tables: "stol", stat_best: "chek rekordi", stat_orders: "bugungi buyurtma",
      table_kicker: "Stol", table_title: "Qaysi stoldasiz?",
      table_text: "Raqam chekka yoziladi. Tanlov shu brauzerda saqlanadi.",
      table_current: "Hozir stol", table_free: "bo‘sh", table_busy: "chek bor",
      menu_kicker: "Menyu", menu_title: "Taomlarni tanlang", menu_all: "Hammasi", add: "Qo‘shish",
      cat_salad: "Salatlar", cat_hot: "Issiq", cat_grill: "Gril", cat_soup: "Sho‘rvalar",
      cat_bake: "Pishiriq", cat_drink: "Ichimlik", cat_sweet: "Shirinlik",
      records_kicker: "Rekordlar", records_title: "Shu brauzerdagi cheklar",
      records_text: "Buyurtmalar lokal saqlanadi. Cursor yopilsa yoki kompyuter qulflansa, ular o‘chmaydi.",
      rec_count: "jami chek", rec_pop: "mashhur taom", rec_clear: "Rekordlarni tozalash",
      rec_empty: "Hali bo‘sh. Birinchi buyurtma birinchi rekord bo‘ladi.",
      rec_best: "rekord", rec_confirm: "Shu brauzerdagi barcha cheklar o‘chirilsinmi?",
      cart_title: "Buyurtmangiz", cart_empty: "Hali bo‘sh. Menyudan taom qo‘shing.",
      comment: "Izoh", total: "Jami", send: "Yuborish",
      need_table: "Avval stolni tanlang.", need_cart: "Savat bo‘sh.",
      saved: "Chek rekordlarga saqlandi", cleared: "Rekordlar tozalandi",
      qr_kicker: "Zal uchun bitta QR", qr_title: "Mehmon o‘tirib kodni skanerlaydi",
      qr_text: "Kod shu menyuni tarmoqda ochadi. Har telefonning rekordlari o‘zida, lokal xotirada turadi."
    }
  };

  var menu = [
    { id: "d_salad", cat: "salad", price: 28000, img: "img/salad.jpg", name: { ru: "Салат", en: "Salad", uz: "Salat" }, text: { ru: "Помидоры, лук и зелень с острым перцем.", en: "Tomatoes, onion and herbs with a little heat.", uz: "Pomidor, piyoz va ko‘kat, ozgina achchiq." } },
    { id: "d_greens", cat: "salad", price: 24000, img: "img/greens.jpg", name: { ru: "Зелёный салат", en: "Green salad", uz: "Yashil salat" }, text: { ru: "Свежие листья, огурец и лимонная заправка.", en: "Leaves, cucumber and a lemon dressing.", uz: "Barglar, bodring va limonli sous." } },
    { id: "d_plov", cat: "hot", price: 45000, img: "img/plov.jpg", name: { ru: "Плов", en: "Plov", uz: "Palov" }, text: { ru: "Рис, мясо и морковь, томлёные в казане.", en: "Rice, meat and carrot cooked in a kazan.", uz: "Qozonda guruch, go‘sht va sabzi." } },
    { id: "d_lagman", cat: "hot", price: 42000, img: "img/lagman.jpg", name: { ru: "Лагман", en: "Lagman", uz: "Lag‘mon" }, text: { ru: "Тянутая лапша с мясом и овощами.", en: "Hand-pulled noodles with meat and vegetables.", uz: "Go‘sht va sabzavotli lag‘mon." } },
    { id: "d_manti", cat: "hot", price: 38000, img: "img/manti.jpg", name: { ru: "Манты", en: "Manti", uz: "Manti" }, text: { ru: "Порция на пару, сметана отдельно.", en: "Steamed dumplings, sour cream on the side.", uz: "Bug‘da pishgan manti, smetana alohida." } },
    { id: "d_shashlik", cat: "grill", price: 52000, img: "img/shashlik.jpg", name: { ru: "Шашлык", en: "Shashlik", uz: "Shashlik" }, text: { ru: "Мясо на углях, лук и лепёшка.", en: "Meat over coals, with onion and bread.", uz: "Ko‘mirdagi go‘sht, piyoz va non." } },
    { id: "d_lula", cat: "grill", price: 44000, img: "img/lula.jpg", name: { ru: "Люля-кебаб", en: "Lula kebab", uz: "Lyulya kabob" }, text: { ru: "Рубленое мясо на шампуре, с лавашом.", en: "Minced meat on a skewer, with flatbread.", uz: "Shampurda qiyma, non bilan." } },
    { id: "d_soup", cat: "soup", price: 32000, img: "img/soup.jpg", name: { ru: "Мастава", en: "Mastava", uz: "Mastava" }, text: { ru: "Густой суп с рисом, мясом и овощами.", en: "A thick soup of rice, meat and vegetables.", uz: "Guruch, go‘sht va sabzavotli quyuq sho‘rva." } },
    { id: "d_samsa", cat: "bake", price: 12000, img: "img/samsa.jpg", name: { ru: "Самса", en: "Samsa", uz: "Somsa" }, text: { ru: "Одна самса из тандыра, с мясом и луком.", en: "One tandoor samsa with meat and onion.", uz: "Tandirdan bitta go‘shtli somsa." } },
    { id: "d_bread", cat: "bake", price: 6000, img: "img/bread.jpg", name: { ru: "Лепёшка", en: "Tandoor bread", uz: "Non" }, text: { ru: "Тёплый тандырный хлеб на стол.", en: "Warm tandoor bread for the table.", uz: "Stol uchun iliq tandir non." } },
    { id: "d_tea", cat: "drink", price: 8000, img: "img/tea.jpg", name: { ru: "Чай", en: "Tea", uz: "Choy" }, text: { ru: "Чайник чёрного чая.", en: "A pot of black tea.", uz: "Qora choy choynagi." } },
    { id: "d_drink", cat: "drink", price: 16000, img: "img/juice.jpg", name: { ru: "Напиток", en: "Drink", uz: "Ichimlik" }, text: { ru: "Холодный лимонад домашнего приготовления.", en: "A cold house lemonade.", uz: "Uy limonadi, sovuq." } },
    { id: "d_compote", cat: "drink", price: 10000, img: "img/compote.jpg", name: { ru: "Компот", en: "Compote", uz: "Kompot" }, text: { ru: "Фруктовый компот, подаётся охлаждённым.", en: "Fruit compote, served cold.", uz: "Mevali kompot, sovutilgan." } },
    { id: "d_cake", cat: "sweet", price: 22000, img: "img/cake.jpg", name: { ru: "Наполеон", en: "Napoleon cake", uz: "Napoleon" }, text: { ru: "Слоёный торт с заварным кремом. Кусок.", en: "A slice of layered cake with custard.", uz: "Zavar kremli tort, bir bo‘lak." } },
    { id: "d_honey", cat: "sweet", price: 20000, img: "img/honey.jpg", name: { ru: "Медовик", en: "Honey cake", uz: "Asal tort" }, text: { ru: "Мягкие коржи с мёдом и сметанным кремом.", en: "Soft honey layers and sour-cream cream.", uz: "Asal qatlamlari va smetana kremi." } }
  ];

  var cats = ["salad", "hot", "grill", "soup", "bake", "drink", "sweet"];
  var lang = localStorage.getItem(LANG_KEY) || "ru";
  if (!dict[lang]) lang = "ru";
  var table = Number(localStorage.getItem(TABLE_KEY)) || 5;
  var category = "all";
  var cart = loadJson(CART_KEY, {});
  var records = loadJson(STORAGE, []);

  function t(key) { return (dict[lang] && dict[lang][key]) || key; }
  function loadJson(key, fallback) {
    try {
      var value = JSON.parse(localStorage.getItem(key));
      return value == null ? fallback : value;
    } catch (err) {
      return fallback;
    }
  }
  function money(value) {
    return String(Math.round(value)).replace(/\B(?=(\d{3})+(?!\d))/g, " ") + " сум";
  }
  function esc(value) {
    return String(value).replace(/[&<>"]/g, function (ch) {
      return { "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;" }[ch];
    });
  }
  function dishById(id) {
    return menu.filter(function (item) { return item.id === id; })[0];
  }
  function qtyOf(id) { return cart[id] || 0; }
  function cartCount() {
    return Object.keys(cart).reduce(function (sum, id) { return sum + (cart[id] || 0); }, 0);
  }
  function cartTotal() {
    return Object.keys(cart).reduce(function (sum, id) {
      var item = dishById(id);
      return sum + (item ? item.price * cart[id] : 0);
    }, 0);
  }
  function todayCount() {
    var start = new Date();
    start.setHours(0, 0, 0, 0);
    return records.filter(function (row) { return row.at >= start.getTime(); }).length;
  }
  function bestRecord() {
    return records.reduce(function (best, row) {
      return !best || row.total > best.total ? row : best;
    }, null);
  }
  function popularName() {
    var counts = {};
    records.forEach(function (row) {
      row.items.forEach(function (item) {
        counts[item.name] = (counts[item.name] || 0) + item.qty;
      });
    });
    var name = "";
    var max = 0;
    Object.keys(counts).forEach(function (key) {
      if (counts[key] > max) { max = counts[key]; name = key; }
    });
    return name;
  }
  function tablesWithBills() {
    var set = {};
    records.forEach(function (row) { set[row.table] = true; });
    return set;
  }

  function applyText() {
    document.querySelectorAll("[data-i18n]").forEach(function (el) {
      el.textContent = t(el.getAttribute("data-i18n"));
    });
    document.documentElement.lang = lang;
    document.querySelectorAll("[data-lang]").forEach(function (btn) {
      btn.classList.toggle("is-active", btn.getAttribute("data-lang") === lang);
    });
    var title = { ru: "TableGo — меню на столе", en: "TableGo — menu at the table", uz: "TableGo — stoldagi menyu" };
    document.title = title[lang];
  }

  function renderTables() {
    var busy = tablesWithBills();
    document.getElementById("tableGrid").innerHTML = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12].map(function (number) {
      var on = number === table ? " is-on" : "";
      var label = busy[number] ? t("table_busy") : t("table_free");
      return '<button type="button" class="table-btn' + on + '" data-table="' + number + '"><b>' + number + '</b><small>' + esc(label) + '</small></button>';
    }).join("");
    document.getElementById("tableNow").textContent = t("table_current") + " №" + table;
  }

  function renderMenu() {
    var buttons = '<button type="button" class="chip' + (category === "all" ? " is-on" : "") + '" data-cat="all">' + esc(t("menu_all")) + "</button>";
    buttons += cats.map(function (id) {
      return '<button type="button" class="chip' + (category === id ? " is-on" : "") + '" data-cat="' + id + '">' + esc(t("cat_" + id)) + "</button>";
    }).join("");
    document.getElementById("cats").innerHTML = buttons;
    var items = menu.filter(function (item) { return category === "all" || item.cat === category; });
    document.getElementById("dishGrid").innerHTML = items.map(function (item) {
      var qty = qtyOf(item.id);
      var control = qty
        ? '<div class="stepper"><button type="button" data-dec="' + item.id + '">−</button><b>' + qty + '</b><button type="button" data-inc="' + item.id + '">+</button></div>'
        : '<button type="button" class="btn btn-small" data-inc="' + item.id + '">' + esc(t("add")) + "</button>";
      return '<article class="dish"><div class="dish-photo"><img src="' + item.img + '" alt="' + esc(item.name[lang] || item.name.ru) + '"></div><div class="dish-body"><h3>' + esc(item.name[lang] || item.name.ru) + "</h3><p>" + esc(item.text[lang] || item.text.ru) + '</p><div class="dish-row"><span class="price">' + esc(money(item.price)) + "</span>" + control + "</div></div></article>";
    }).join("");
  }

  function renderCart() {
    document.getElementById("cartCount").textContent = String(cartCount());
    document.getElementById("cartTotal").textContent = money(cartTotal());
    var lines = Object.keys(cart).filter(function (id) { return cart[id] > 0; }).map(function (id) {
      var item = dishById(id);
      if (!item) return "";
      return '<div class="cart-line"><div><strong>' + esc(item.name[lang] || item.name.ru) + '</strong><div class="lead">' + esc(money(item.price)) + '</div></div><div class="stepper"><button type="button" data-dec="' + id + '">−</button><b>' + cart[id] + '</b><button type="button" data-inc="' + id + '">+</button></div></div>';
    }).join("");
    document.getElementById("cartBody").innerHTML = lines || '<p class="empty">' + esc(t("cart_empty")) + "</p>";
  }

  function renderRecords() {
    var best = bestRecord();
    var pop = popularName();
    document.getElementById("statBest").textContent = best ? money(best.total) : "—";
    document.getElementById("statOrders").textContent = String(todayCount());
    document.getElementById("recBest").textContent = best ? money(best.total) : "—";
    document.getElementById("recCount").textContent = String(records.length);
    document.getElementById("recPop").textContent = pop || "—";
    var list = document.getElementById("recordList");
    if (!records.length) {
      list.innerHTML = '<p class="empty">' + esc(t("rec_empty")) + "</p>";
      return;
    }
    var top = best ? best.total : 0;
    list.innerHTML = records.slice().reverse().map(function (row) {
      var when = new Date(row.at);
      var items = row.items.map(function (item) { return item.name + " ×" + item.qty; }).join(", ");
      var note = row.comment ? " · " + row.comment : "";
      var tag = row.total === top ? '<span class="tag">' + esc(t("rec_best")) + "</span>" : "<span></span>";
      return '<article class="record' + (row.total === top ? " is-best" : "") + '"><div><b>№' + row.table + " · " + esc(money(row.total)) + "</b><p>" + esc(items + note) + '</p><time>' + esc(when.toLocaleString()) + '</time></div>' + tag + "</article>";
    }).join("");
  }

  function render() {
    applyText();
    renderTables();
    renderMenu();
    renderCart();
    renderRecords();
  }

  function setQty(id, next) {
    next = Math.max(0, Math.min(30, next | 0));
    if (next) cart[id] = next;
    else delete cart[id];
    localStorage.setItem(CART_KEY, JSON.stringify(cart));
    renderMenu();
    renderCart();
  }

  function toast(text) {
    var el = document.getElementById("toast");
    el.textContent = text;
    el.classList.add("is-on");
    clearTimeout(toast.timer);
    toast.timer = setTimeout(function () { el.classList.remove("is-on"); }, 2200);
  }

  function openCart() {
    document.getElementById("cart").classList.remove("hidden");
    document.getElementById("cartOverlay").classList.remove("hidden");
  }
  function closeCart() {
    document.getElementById("cart").classList.add("hidden");
    document.getElementById("cartOverlay").classList.add("hidden");
  }

  function sendOrder() {
    if (!table) { toast(t("need_table")); return; }
    var items = Object.keys(cart).filter(function (id) { return cart[id] > 0; }).map(function (id) {
      var item = dishById(id);
      return { id: id, name: item.name[lang] || item.name.ru, qty: cart[id], price: item.price };
    });
    if (!items.length) { toast(t("need_cart")); return; }
    var comment = document.getElementById("comment").value.trim().slice(0, 240);
    records.push({
      id: Date.now().toString(36),
      table: table,
      items: items,
      total: cartTotal(),
      comment: comment,
      at: Date.now()
    });
    localStorage.setItem(STORAGE, JSON.stringify(records));
    cart = {};
    localStorage.setItem(CART_KEY, "{}");
    document.getElementById("comment").value = "";
    localStorage.removeItem(NOTE_KEY);
    closeCart();
    render();
    toast(t("saved"));
    location.hash = "records";
  }

  document.getElementById("comment").value = localStorage.getItem(NOTE_KEY) || "";
  document.getElementById("comment").addEventListener("input", function (event) {
    localStorage.setItem(NOTE_KEY, event.target.value.slice(0, 240));
  });
  document.getElementById("cartBtn").addEventListener("click", openCart);
  document.getElementById("cartClose").addEventListener("click", closeCart);
  document.getElementById("cartOverlay").addEventListener("click", closeCart);
  document.getElementById("sendBtn").addEventListener("click", sendOrder);
  document.getElementById("clearRecords").addEventListener("click", function () {
    if (!records.length || !window.confirm(t("rec_confirm"))) return;
    records = [];
    localStorage.setItem(STORAGE, "[]");
    render();
    toast(t("cleared"));
  });
  document.body.addEventListener("click", function (event) {
    var langBtn = event.target.closest("[data-lang]");
    var tableBtn = event.target.closest("[data-table]");
    var catBtn = event.target.closest("[data-cat]");
    var inc = event.target.closest("[data-inc]");
    var dec = event.target.closest("[data-dec]");
    var go = event.target.closest("[data-go]");
    if (langBtn) {
      lang = langBtn.getAttribute("data-lang");
      localStorage.setItem(LANG_KEY, lang);
      render();
    }
    if (tableBtn) {
      table = Number(tableBtn.getAttribute("data-table"));
      localStorage.setItem(TABLE_KEY, String(table));
      renderTables();
    }
    if (catBtn) {
      category = catBtn.getAttribute("data-cat");
      renderMenu();
    }
    if (inc) setQty(inc.getAttribute("data-inc"), qtyOf(inc.getAttribute("data-inc")) + 1);
    if (dec) setQty(dec.getAttribute("data-dec"), qtyOf(dec.getAttribute("data-dec")) - 1);
    if (go) document.getElementById(go.getAttribute("data-go")).scrollIntoView();
  });
  document.addEventListener("keydown", function (event) {
    if (event.key === "Escape") closeCart();
  });
  window.addEventListener("scroll", function () {
    document.getElementById("nav").classList.toggle("is-solid", window.scrollY > 40);
  }, { passive: true });

  render();
})();