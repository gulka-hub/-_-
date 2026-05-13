<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Координатный метод · Задача 14 ЕГЭ</title>

<script>
window.MathJax = {
  tex: { inlineMath: [['\\(','\\)']], displayMath: [['\\[','\\]']] },
  svg: { fontCache: 'global' }
};
</script>
<script defer src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js"></script>

<style>
:root{
  --bg:#f0ebe3; --card:#fffaf1; --card2:#fbf4e8;
  --crimson:#7a1c2e; --crimson2:#9e2d42; --pale:#f5e8eb;
  --text:#251f19; --muted:#665b51; --light:#978979;
  --border:#ddcdb3; --gold:#c5913b;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;background:var(--bg);color:var(--text);
  font-family:Georgia,"Times New Roman",serif;font-size:18px;line-height:1.75;
}
nav{
  position:sticky;top:0;z-index:20;height:72px;
  display:flex;align-items:center;padding:0 38px;
  background:rgba(240,235,227,.96);backdrop-filter:blur(12px);
  border-bottom:1px solid var(--border);
}
.logo{display:flex;align-items:center;gap:18px;text-decoration:none;color:var(--text);font-size:28px;font-weight:700}
.badge{font-family:monospace;font-size:13px;letter-spacing:.16em;background:var(--crimson);color:#fff;border-radius:7px;padding:7px 12px}
.links{margin-left:auto;display:flex;gap:38px}
.links a{color:var(--muted);text-decoration:none;font-size:20px}
.links a:hover{color:var(--crimson)}
section{max-width:1320px;margin:0 auto;padding:84px 34px}
.label{font-family:monospace;text-transform:uppercase;letter-spacing:.28em;color:var(--crimson);font-size:12px;display:flex;align-items:center;gap:16px;margin-bottom:18px}
.label:before{content:"";display:block;width:54px;height:2px;background:var(--crimson)}
h1,h2,h3{line-height:1.05;margin:0}
h1{font-size:72px;letter-spacing:-.03em;margin-bottom:28px}
h2{font-size:60px;letter-spacing:-.02em;margin-bottom:18px}
h3{font-size:34px;margin-bottom:14px}
.accent{color:var(--crimson);font-style:italic}
.line{width:72px;height:3px;background:var(--crimson);margin:24px 0 34px}
.hero{display:grid;grid-template-columns:1fr 1fr;gap:54px;align-items:center;min-height:660px}
.lead{font-size:24px;color:var(--muted);max-width:760px}
.btns{display:flex;gap:16px;margin:34px 0}
.btn{display:inline-flex;align-items:center;justify-content:center;border-radius:12px;padding:15px 25px;text-decoration:none;border:1px solid var(--border);background:var(--card);color:var(--text);font-weight:600}
.btn.primary{background:var(--crimson);color:#fff;border-color:var(--crimson)}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:0;margin-top:40px;border:1px solid var(--border);border-radius:20px;background:var(--card);overflow:hidden}
.stat{padding:24px;text-align:center;border-right:1px solid var(--border)}
.stat:last-child{border-right:0}
.stat b{font-size:38px;color:var(--crimson)}
.stat span{display:block;font-family:monospace;font-size:11px;text-transform:uppercase;letter-spacing:.22em;color:var(--light)}
.card{background:var(--card);border:1px solid var(--border);border-radius:24px;box-shadow:0 8px 24px rgba(70,45,20,.06)}
.canvas-card{padding:22px;position:relative}
.canvas-tag{position:absolute;right:28px;top:26px;background:var(--pale);color:var(--crimson);font-family:monospace;font-size:12px;letter-spacing:.22em;text-transform:uppercase;padding:8px 16px;border-radius:999px;z-index:2}
.shape-canvas{width:100%;height:430px;display:block;border-radius:18px;background:#fffdf8;cursor:grab}
.shape-canvas:active{cursor:grabbing}
.hint{text-align:center;color:var(--light);font-family:monospace;font-size:12px;letter-spacing:.18em;margin-top:12px}
.grid4{display:grid;grid-template-columns:repeat(4,1fr);gap:20px}
.why{padding:28px}
.why-num{font-size:38px;color:rgba(122,28,46,.75);font-style:italic;font-weight:700}
.tabs{display:flex;overflow-x:auto;border:1px solid var(--border);border-radius:22px 22px 0 0;background:var(--card);margin-top:34px}
.tab{flex:0 0 auto;border:0;border-right:1px solid var(--border);background:transparent;padding:21px 28px;font:inherit;color:var(--muted);cursor:pointer}
.tab.active{background:var(--crimson);color:#fff;font-weight:700}
.tab span{font-family:monospace;font-size:13px;margin-right:10px}
.theory-wrap{display:grid;grid-template-columns:1fr 1.05fr;gap:38px;margin-top:32px}
.theory-text{padding:34px}
.theory-text h3{font-size:52px}
.theory-text .sub{font-size:26px;color:var(--crimson);line-height:1.55;margin:18px 0 28px}
.formula{
  border-left:5px solid var(--crimson);background:#fff;border-radius:0 14px 14px 0;
  padding:20px 24px;margin:16px 0;box-shadow:0 3px 12px rgba(0,0,0,.05);
  overflow-x:auto;font-size:20px
}
.shape-switch{display:flex;gap:12px;margin-bottom:14px}
.shape-switch button{border:1px solid var(--border);background:var(--card);border-radius:999px;padding:10px 20px;font:inherit;color:var(--muted);cursor:pointer}
.shape-switch button.active{border-color:var(--crimson);background:var(--pale);color:var(--crimson)}
.ege-list{display:grid;gap:38px;margin-top:44px}
.ege-card{overflow:hidden}
.ege-head{display:flex;justify-content:space-between;align-items:center;gap:20px;background:var(--crimson);color:#fff;padding:24px 32px}
.ege-head h3{font-size:28px;margin:0}
.ege-badge{font-family:monospace;text-transform:uppercase;letter-spacing:.22em;border:1px solid rgba(255,255,255,.3);border-radius:7px;padding:8px 13px;font-size:12px}
.ege-body{padding:32px}
.condition{background:var(--card2);border-left:4px solid var(--gold);border-radius:14px;padding:24px 28px;font-size:24px;line-height:1.65;margin-bottom:30px}
.solve-grid{display:grid;grid-template-columns:.9fr 1fr;gap:30px}
.steps{display:grid;gap:16px}
.step{background:var(--card2);border-left:4px solid #d36b42;border-radius:14px;padding:22px}
.step h4{margin:0 0 8px;color:var(--crimson);font-size:21px}
.answer{display:flex;justify-content:space-between;gap:20px;align-items:center;margin-top:30px;background:#f8eee9;border:1px dashed var(--crimson);border-radius:16px;padding:22px 28px;font-size:25px}
.bank-panel{display:grid;grid-template-columns:repeat(4,1fr);border:1px solid var(--border);background:var(--card);border-radius:22px;margin:40px 0 28px;overflow:hidden}
.bank-stat{text-align:center;padding:25px;border-right:1px solid var(--border)}
.bank-stat:last-child{border-right:0}
.bank-stat b{font-size:36px;color:var(--crimson)}
.bank-stat span{display:block;font-family:monospace;letter-spacing:.22em;text-transform:uppercase;font-size:12px;color:var(--light)}
.filters{display:flex;gap:12px;flex-wrap:wrap;margin-bottom:28px}
.filter{border:1px solid var(--border);background:var(--card);border-radius:999px;padding:11px 21px;font:inherit;cursor:pointer}
.filter.active{background:var(--crimson);border-color:var(--crimson);color:#fff}
.bank-list{display:grid;gap:24px}
.task{overflow:hidden;border-color:#d36b42}
.task-head{display:flex;justify-content:space-between;gap:20px;background:var(--card2);border-bottom:1px solid var(--border);padding:22px 28px}
.task-id{font-family:monospace;font-size:20px;letter-spacing:.16em;color:var(--crimson);font-weight:700}
.pill{display:inline-block;background:#e9e0ca;border-radius:7px;padding:5px 10px;font-family:monospace;font-size:12px;margin-left:6px;color:#5b7447}
.task-body{padding:28px}
.task-body p{font-size:23px}
.answer-row{display:grid;grid-template-columns:1fr auto auto;gap:12px;margin-top:18px}
input{border:1px solid var(--border);background:var(--card);border-radius:12px;padding:14px 16px;font:20px monospace;outline:none}
input:focus{border-color:var(--crimson)}
button.main{border:1px solid var(--crimson);background:var(--crimson);color:#fff;border-radius:12px;padding:14px 22px;font:inherit;font-weight:700;cursor:pointer}
button.outline{border:1px solid var(--crimson);background:transparent;color:var(--crimson);border-radius:12px;padding:14px 22px;font:inherit;font-weight:700;cursor:pointer}
.feedback{margin-top:14px;border-radius:12px;padding:13px 16px}
.feedback.ok{background:#e8f5e9;color:#2e7d32}
.feedback.bad{background:#fde4e7;color:#a21d2d}
.solution{display:none;background:var(--card2);border:1px solid var(--border);border-radius:14px;padding:20px;margin-top:18px}
.solution.open{display:block}
footer{border-top:1px solid var(--border);max-width:1320px;margin:0 auto;padding:36px 34px;color:var(--light);display:flex;justify-content:space-between}
@media(max-width:900px){
  .hero,.theory-wrap,.solve-grid{grid-template-columns:1fr}
  .grid4{grid-template-columns:1fr 1fr}
  .links{display:none}
  h1{font-size:52px} h2{font-size:46px}
  .answer-row{grid-template-columns:1fr}
}
@media(max-width:620px){
  section{padding:56px 18px}
  .grid4,.stats,.bank-panel{grid-template-columns:1fr}
  .stat,.bank-stat{border-right:0;border-bottom:1px solid var(--border)}
  .shape-canvas{height:320px}
}
</style>
</head>
<body>
<nav>
  <a class="logo" href="#hero"><span class="badge">XYZ</span>Координатный метод</a>
  <div class="links">
    <a href="#why">Зачем</a><a href="#theory">Теория</a><a href="#ege">Разборы ЕГЭ</a><a href="#bank">Банк задач</a>
  </div>
</nav>

<section id="hero" class="hero">
  <div>
    <div class="label">Профильный ЕГЭ · задача 14 · стереометрия</div>
    <h1>Координатный <span class="accent">метод</span> как язык пространства</h1>
    <p class="lead">Учебно-методический сайт для подготовки к стереометрии ЕГЭ: теория, интерактивные 3D-модели, пошаговые решения и банк задач с проверкой.</p>
    <div class="btns"><a class="btn primary" href="#theory">Начать изучение →</a><a class="btn" href="#bank">К банку задач</a></div>
    <div class="stats"><div class="stat"><b>08</b><span>разделов</span></div><div class="stat"><b>02</b><span>разбора</span></div><div class="stat"><b>08</b><span>задач</span></div></div>
  </div>
  <div class="card canvas-card">
    <span class="canvas-tag">Interactive 3D</span>
    <canvas class="shape-canvas" data-shape="cube"></canvas>
    <div class="hint">↺ мышь — вращение, колесо — масштаб</div>
  </div>
</section>

<section id="why">
  <div class="label">Введение</div><h2>Почему координатный метод</h2><div class="line"></div>
  <p class="lead">Координатный подход превращает пространственную задачу в последовательность вычислений: выбрать систему координат, записать точки, найти векторы, применить формулу.</p>
  <div class="grid4" style="margin-top:36px">
    <div class="card why"><div class="why-num">01</div><h3>Алгоритм</h3><p>Решение строится по понятному плану, а не по догадке на чертеже.</p></div>
    <div class="card why"><div class="why-num">02</div><h3>Меньше риска</h3><p>Ошибки легче найти: отдельно проверяются координаты, векторы и формулы.</p></div>
    <div class="card why"><div class="why-num">03</div><h3>Гибкость</h3><p>Один метод работает для углов между прямыми, плоскостями и расстояний.</p></div>
    <div class="card why"><div class="why-num">04</div><h3>Компактность</h3><p>Решение удобно записывать в формате шагов и вычислительных блоков.</p></div>
  </div>
</section>

<section id="theory">
  <div class="label">Раздел · 01—08</div><h2>Теоретический блок</h2><div class="line"></div>
  <p class="lead">Выберите тему. Справа отображается интерактивная модель, слева — теория и формулы.</p>
  <div class="tabs" id="tabs"></div>
  <div class="theory-wrap">
    <article class="card theory-text">
      <h3 id="theoryTitle"></h3>
      <div class="sub" id="theoryLead"></div>
      <div id="theoryText"></div>
      <div id="theoryFormulas"></div>
    </article>
    <div>
      <div class="shape-switch">
        <button data-shape-btn="cube" class="active">Куб</button>
        <button data-shape-btn="pyramid">Пирамида</button>
        <button data-shape-btn="prism">6-призма</button>
      </div>
      <div class="card canvas-card">
        <span class="canvas-tag">Interactive 3D</span>
        <canvas id="theoryCanvas" class="shape-canvas" data-shape="cube"></canvas>
        <div class="hint">↺ мышь — вращение, колесо — масштаб</div>
      </div>
    </div>
  </div>
</section>

<section id="ege">
  <div class="label">Открытый банк ФИПИ</div><h2>Разборы ЕГЭ</h2><div class="line"></div>
  <p class="lead">Широкий формат: условие, интерактивная модель, шаги решения и аккуратные вычисления.</p>
  <div class="ege-list" id="egeList"></div>
</section>

<section id="bank">
  <div class="label">Самостоятельная работа</div><h2>Банк задач</h2><div class="line"></div>
  <p class="lead">Введите ответ и нажмите «Проверить». При ошибке правильный ответ не показывается.</p>
  <div class="bank-panel">
    <div class="bank-stat"><b id="attempts">0</b><span>попыток</span></div>
    <div class="bank-stat"><b id="right">0</b><span>верно</span></div>
    <div class="bank-stat"><b id="wrong">0</b><span>неверно</span></div>
    <div class="bank-stat"><b id="solved">0/8</b><span>решено</span></div>
  </div>
  <div class="filters" id="filters"></div>
  <div class="bank-list" id="bankList"></div>
</section>

<footer><span>Координатный метод · Задача 14 ЕГЭ</span><span>ПРОФИЛЬНАЯ МАТЕМАТИКА</span></footer>

<script>
const theoryTabs = [
 {n:'01', title:'Система координат', shape:'cube', lead:'Главная идея — выбрать начало и оси так, чтобы координаты вершин получились максимально простыми.', text:['В кубе начало координат обычно помещают в одну из вершин, а оси направляют вдоль трёх рёбер, выходящих из неё.','В правильной пирамиде удобно брать начало в центре основания: ось Oz идёт к вершине, Ox и Oy лежат в основании.'], formulas:['\\[A(0;0;0),\\quad B(a;0;0),\\quad D(0;a;0),\\quad A_1(0;0;a)\\]','\\[S(0;0;h),\\quad A(-\\frac a2;-\\frac a2;0),\\quad B(\\frac a2;-\\frac a2;0)\\]']},
 {n:'02', title:'Векторы', shape:'cube', lead:'Векторы связывают геометрию с алгеброй: прямые, углы и плоскости описываются координатами.', text:['Вектор \\(\\overrightarrow{AB}\\) получают вычитанием координат: из координат конца вычитают координаты начала.','Скалярное произведение используется для углов. Векторное произведение помогает найти нормаль к плоскости.'], formulas:['\\[\\overrightarrow{AB}=(x_B-x_A;\\ y_B-y_A;\\ z_B-z_A)\\]','\\[\\vec a\\cdot\\vec b=a_xb_x+a_yb_y+a_zb_z\\]','\\[|\\vec a|=\\sqrt{a_x^2+a_y^2+a_z^2}\\]']},
 {n:'03', title:'Уравнение плоскости', shape:'plane', lead:'Плоскость задаётся нормальным вектором и точкой, через которую она проходит.', text:['Если \\(\\vec n=(A;B;C)\\) — нормаль к плоскости, а \\(M_0(x_0;y_0;z_0)\\) лежит в плоскости, то уравнение строится напрямую.','Нормаль обычно получают как векторное произведение двух неколлинеарных векторов.'], formulas:['\\[A(x-x_0)+B(y-y_0)+C(z-z_0)=0\\]','\\[\\vec n=\\vec a\\times\\vec b\\]','\\[Ax+By+Cz+D=0\\]']},
 {n:'04', title:'Угол между прямыми', shape:'cube', lead:'Для прямых нужны только их направляющие векторы.', text:['Находим направляющий вектор первой прямой и направляющий вектор второй прямой.','Подставляем их в формулу косинуса угла через скалярное произведение.'], formulas:['\\[\\cos\\varphi=\\frac{|\\vec a\\cdot\\vec b|}{|\\vec a|\\cdot|\\vec b|}\\]','\\[\\varphi=\\arccos(\\cos\\varphi)\\]']},
 {n:'05', title:'Прямая и плоскость', shape:'plane', lead:'Угол между прямой и плоскостью ищется через направляющий вектор прямой и нормаль плоскости.', text:['Сначала находим нормаль \\(\\vec n\\) к плоскости. Затем берём направляющий вектор \\(\\vec d\\) прямой.','Используется синус, потому что угол прямой с плоскостью дополняет угол прямой с нормалью до \\(90^\\circ\\).'], formulas:['\\[\\sin\\alpha=\\frac{|\\vec d\\cdot\\vec n|}{|\\vec d|\\cdot|\\vec n|}\\]','\\[\\alpha=\\arcsin(\\sin\\alpha)\\]']},
 {n:'06', title:'Между плоскостями', shape:'prism', lead:'Угол между плоскостями можно искать через нормали к этим плоскостям.', text:['Для каждой плоскости находим нормальный вектор.','Дальше задача становится задачей на угол между двумя векторами.'], formulas:['\\[\\cos\\varphi=\\frac{|\\vec n_1\\cdot\\vec n_2|}{|\\vec n_1|\\cdot|\\vec n_2|}\\]','\\[\\vec n_1\\cdot\\vec n_2=0\\quad\\Rightarrow\\quad \\Pi_1\\perp\\Pi_2\\]']},
 {n:'07', title:'Расстояния', shape:'pyramid', lead:'Расстояния в координатах считаются по готовым формулам.', text:['Расстояние от точки до плоскости — одна из самых частых формул в задаче 14.','Для расстояния от точки до прямой используется векторное произведение.'], formulas:['\\[d=\\frac{|Ax_0+By_0+Cz_0+D|}{\\sqrt{A^2+B^2+C^2}}\\]','\\[\\operatorname{dist}(M,l)=\\frac{|\\overrightarrow{PM}\\times\\vec d|}{|\\vec d|}\\]']},
 {n:'08', title:'Скрещивающиеся прямые', shape:'cube', lead:'Для скрещивающихся прямых нужна общая нормаль.', text:['Берём направляющие векторы \\(\\vec d_1\\) и \\(\\vec d_2\\) двух прямых.','Их векторное произведение даёт направление общей нормали.'], formulas:['\\[\\vec n=\\vec d_1\\times\\vec d_2\\]','\\[\\operatorname{dist}=\\frac{|\\overrightarrow{AB}\\cdot\\vec n|}{|\\vec n|}\\]']}
];

const egeTasks = [
 {title:'Задача 1 · угол между плоскостями в правильной призме', badge:'ФИПИ · прототип', shape:'prism',
 condition:'В правильной шестиугольной призме \\(ABCDEFA_1B_1C_1D_1E_1F_1\\), все рёбра которой равны 1, найдите косинус угла между плоскостями \\(ABC\\) и \\(DEA_1\\).',
 answer:'\\(\\cos\\varphi=\\frac{\\sqrt3}{2}\\)', hint:'\\(\\varphi=30^\\circ\\)',
 steps:[
  ['Шаг 1. Выбор системы координат','Начало координат — в центре нижнего основания. Ось \\(Oz\\) — вверх, ось \\(Ox\\) — к вершине \\(A\\).','\\[A=(1;0;0),\\quad B=(\\frac12;\\frac{\\sqrt3}{2};0),\\quad D=(-1;0;0),\\quad A_1=(1;0;1)\\]'],
  ['Шаг 2. Нормаль к плоскости ABC','Плоскость \\(ABC\\) совпадает с нижним основанием, то есть \\(z=0\\).','\\[\\vec n_1=(0;0;1)\\]'],
  ['Шаг 3. Нормаль к плоскости DEA₁','Берём два вектора в плоскости и находим их векторное произведение.','\\[\\vec n_2=(\\sqrt3;1;-2\\sqrt3)\\]'],
  ['Шаг 4. Косинус угла','Подставляем нормали в формулу угла между плоскостями.','\\[\\cos\\varphi=\\frac{|\\vec n_1\\cdot\\vec n_2|}{|\\vec n_1|\\cdot|\\vec n_2|}=\\frac{\\sqrt3}{2}\\]']
 ]},
 {title:'Задача 2 · расстояние от точки до плоскости в пирамиде', badge:'ФИПИ · прототип', shape:'pyramid',
 condition:'В правильной четырёхугольной пирамиде \\(SABCD\\) сторона основания \\(AB=2\\), боковое ребро \\(SA=3\\). Найдите расстояние от точки \\(A\\) до плоскости \\(SBC\\).',
 answer:'\\(d=\\frac{2\\sqrt7}{7}\\)', hint:'через формулу расстояния',
 steps:[
  ['Шаг 1. Координаты','Начало — в центре основания. Ось \\(Oz\\) направлена к вершине \\(S\\).','\\[A=(1;-1;0),\\quad B=(1;1;0),\\quad C=(-1;1;0),\\quad S=(0;0;\\sqrt7)\\]'],
  ['Шаг 2. Плоскость SBC','Строим уравнение плоскости через три точки \\(S,B,C\\).','\\[\\sqrt7y+2z-\\sqrt7=0\\]'],
  ['Шаг 3. Расстояние','Подставляем координаты точки \\(A\\).','\\[d=\\frac{|\\sqrt7\\cdot(-1)+2\\cdot0-\\sqrt7|}{\\sqrt{7+4}}=\\frac{2\\sqrt7}{7}\\]']
 ]}
];

const bank = [
 {id:'01', title:'Угол между диагональю и ребром', type:'Угол между прямыми', level:'Легко', shape:'cube', mode:'cube-angle-lines', condition:'В единичном кубе \\(ABCDA_1B_1C_1D_1\\) найдите косинус угла между прямыми \\(AC_1\\) и \\(BB_1\\). Ответ округлите до сотых.', answer:'0.58', sol:'\\[\\vec{AC_1}=(1;1;1),\\quad \\vec{BB_1}=(0;0;1),\\quad \\cos\\varphi=\\frac{1}{\\sqrt3}\\approx0.58\\]'},
 {id:'02', title:'Угол между плоскостями', type:'Между плоскостями', level:'Легко', shape:'cube', mode:'cube-plane-angle', condition:'В единичном кубе найдите косинус угла между плоскостями \\(ABC_1\\) и \\(ABCD\\).', answer:'0.71', sol:'\\[\\cos\\varphi=\\frac{1}{\\sqrt2}\\approx0.71\\]'},
 {id:'03', title:'Расстояние до плоскости', type:'Расстояния', level:'Сложно', shape:'cube', mode:'cube-distance-plane', condition:'В кубе со стороной 2 найдите расстояние от вершины \\(A\\) до плоскости \\(B_1DC_1\\).', answer:'1.15', sol:'\\[d=\\frac{2}{\\sqrt3}=\\frac{2\\sqrt3}{3}\\approx1.15\\]'},
 {id:'04', title:'Боковая грань пирамиды', type:'Между плоскостями', level:'Легко', shape:'pyramid', mode:'pyramid-face', condition:'В правильной четырёхугольной пирамиде найдите угол между боковой гранью и основанием.', answer:'60', sol:'\\[\\varphi=60^\\circ\\]'},
 {id:'05', title:'Прямая и основание', type:'Смешанные', level:'Легко', shape:'pyramid', mode:'pyramid-line-plane', condition:'Найдите угол между боковым ребром правильной пирамиды и плоскостью основания.', answer:'45', sol:'\\[\\alpha=45^\\circ\\]'},
 {id:'06', title:'Скрещивающиеся рёбра', type:'Расстояния', level:'Сложно', shape:'cube', mode:'cube-skew', condition:'В кубе найдите расстояние между двумя скрещивающимися рёбрами. Ответ округлите до сотых.', answer:'0.71', sol:'\\[d=\\frac{\\sqrt2}{2}\\approx0.71\\]'},
 {id:'07', title:'Прямая призма', type:'Угол между прямыми', level:'Легко', shape:'prism', mode:'prism-vertical', condition:'В прямой призме найдите угол бокового ребра с плоскостью основания.', answer:'90', sol:'\\[\\alpha=90^\\circ\\]'},
 {id:'08', title:'Диагональное сечение', type:'Расстояния', level:'Сложно', shape:'cube', mode:'cube-diagonal-plane', condition:'В кубе найдите расстояние от вершины до диагонального сечения. Ответ округлите до сотых.', answer:'1.63', sol:'\\[d=\\frac{2\\sqrt6}{3}\\approx1.63\\]'}
];

const state = { checks:{}, renderers:[] };

function mj(){ if(window.MathJax?.typesetPromise) MathJax.typesetPromise(); }

function renderTheory(i=0){
  document.querySelectorAll('.tab').forEach((b,k)=>b.classList.toggle('active',k===i));
  const t=theoryTabs[i];
  theoryTitle.textContent=t.title; theoryLead.textContent=t.lead;
  theoryText.innerHTML=t.text.map(p=>`<p>${p}</p>`).join('');
  theoryFormulas.innerHTML=t.formulas.map(f=>`<div class="formula">${f}</div>`).join('');
  const c=document.getElementById('theoryCanvas'); c.dataset.shape=t.shape;
  c.dataset.mode=t.shape;
  const rr=getRenderer(c); rr.shape=t.shape; rr.mode=t.shape;
  document.querySelectorAll('[data-shape-btn]').forEach(b=>b.classList.toggle('active', b.dataset.shapeBtn===t.shape || (t.shape==='plane' && b.dataset.shapeBtn==='cube')));
  mj();
}

function renderTabs(){
  tabs.innerHTML=theoryTabs.map((t,i)=>`<button class="tab ${i===0?'active':''}" data-i="${i}"><span>${t.n}</span>${t.title}</button>`).join('');
  tabs.querySelectorAll('button').forEach(b=>b.onclick=()=>renderTheory(+b.dataset.i));
}

function renderEge(){
  egeList.innerHTML=egeTasks.map((t,idx)=>`
  <article class="card ege-card">
    <div class="ege-head"><h3>${t.title}</h3><span class="ege-badge">${t.badge}</span></div>
    <div class="ege-body">
      <div class="condition">${t.condition}</div>
      <div class="solve-grid">
        <div class="card canvas-card"><canvas class="shape-canvas" data-shape="${t.shape}" data-mode="${t.mode||t.shape}"></canvas><div class="hint">↺ мышь — вращение, колесо — масштаб</div></div>
        <div class="steps">${t.steps.map(s=>`<div class="step"><h4>${s[0]}</h4><p>${s[1]}</p><div class="formula">${s[2]}</div></div>`).join('')}</div>
      </div>
      <div class="answer"><div>Ответ: <b style="color:var(--crimson)">${t.answer}</b></div><span>${t.hint}</span></div>
    </div>
  </article>`).join('');
}

function renderFilters(){
  const fs=['Все','Угол между прямыми','Между плоскостями','Расстояния','Смешанные','Легко','Сложно'];
  filters.innerHTML=fs.map((f,i)=>`<button class="filter ${i===0?'active':''}" data-filter="${f}">${f}</button>`).join('');
  filters.querySelectorAll('button').forEach(b=>b.onclick=()=>{
    filters.querySelectorAll('button').forEach(x=>x.classList.remove('active')); b.classList.add('active'); renderBank(b.dataset.filter);
  });
}

function renderBank(filter='Все'){
  const items=bank.filter(t=>filter==='Все'||t.type===filter||t.level===filter);
  bankList.innerHTML=items.map(t=>`
  <article class="card task">
    <div class="task-head"><div><div class="task-id">Задача ${t.id}</div><h3>${t.title}</h3></div><div><span class="pill">${t.level}</span><span class="pill">${t.type}</span></div></div>
    <div class="task-body">
      <p>${t.condition}</p>
      <div class="card canvas-card"><canvas class="shape-canvas" data-shape="${t.shape}" data-mode="${t.mode||t.shape}"></canvas><div class="hint">↺ мышь — вращение, колесо — масштаб</div></div>
      <div class="answer-row"><input id="inp-${t.id}" placeholder="Введите ответ..." /><button class="main" data-check="${t.id}">Проверить</button><button class="outline" data-sol="${t.id}">Разбор</button></div>
      <div id="fb-${t.id}"></div>
      <div class="solution" id="sol-${t.id}"><b style="color:var(--crimson)">Идея решения:</b> выбираем систему координат, находим нужные векторы/нормали и применяем формулу.<div class="formula">${t.sol}</div></div>
    </div>
  </article>`).join('');
  bankList.querySelectorAll('[data-check]').forEach(b=>b.onclick=()=>checkTask(b.dataset.check));
  bankList.querySelectorAll('[data-sol]').forEach(b=>b.onclick=()=>document.getElementById('sol-'+b.dataset.sol).classList.toggle('open'));
  initCanvases();
  mj();
}

function checkTask(id){
  const task=bank.find(t=>t.id===id);
  const raw=document.getElementById('inp-'+id).value.replace(',','.').trim();
  const ok=raw===task.answer;
  state.checks[id]=ok;
  document.getElementById('fb-'+id).innerHTML=`<div class="feedback ${ok?'ok':'bad'}">${ok?'Верно!':'Неверно. Попробуйте ещё раз.'}</div>`;
  const vals=Object.values(state.checks); attempts.textContent=vals.length; right.textContent=vals.filter(Boolean).length; wrong.textContent=vals.filter(x=>x===false).length; solved.textContent=`${vals.filter(Boolean).length}/${bank.length}`;
}

function getRenderer(canvas){
  let r=state.renderers.find(x=>x.canvas===canvas);
  if(!r){ r=new Renderer(canvas); state.renderers.push(r); }
  return r;
}
function initCanvases(){ document.querySelectorAll('.shape-canvas').forEach(c=>getRenderer(c)); }

class Renderer{
  constructor(canvas){
    this.canvas=canvas; this.ctx=canvas.getContext('2d'); this.shape=canvas.dataset.shape||'cube';
    this.mode=canvas.dataset.mode||this.shape; this.rx=-0.45; this.ry=0.75; this.scale=1; this.drag=false; this.last=null;
    canvas.addEventListener('pointerdown',e=>{this.drag=true; this.last=[e.clientX,e.clientY]; canvas.setPointerCapture(e.pointerId);});
    canvas.addEventListener('pointerup',()=>this.drag=false);
    canvas.addEventListener('pointermove',e=>{if(!this.drag)return; const [x,y]=this.last; this.ry+=(e.clientX-x)*0.01; this.rx+=(e.clientY-y)*0.01; this.last=[e.clientX,e.clientY]; this.draw();});
    canvas.addEventListener('wheel',e=>{e.preventDefault(); this.scale=Math.max(.65,Math.min(1.8,this.scale-e.deltaY*0.001)); this.draw();},{passive:false});
    new ResizeObserver(()=>this.draw()).observe(canvas); this.draw();
  }
  points(){
    if(this.shape==='pyramid') {
      const base = {
        pts:[[-1.2,-1.2,0],[1.2,-1.2,0],[1.2,1.2,0],[-1.2,1.2,0],[0,0,2.1]],
        edges:[[0,1],[1,2],[2,3],[3,0],[0,4],[1,4],[2,4],[3,4]],
        hi:[[0,4],[1,4],[0,1]], faces:[], labels:['A','B','C','D','S']
      };
      if(this.mode==='pyramid-face') { base.hi=[[0,1],[1,4],[0,4]]; base.faces=[[0,1,4]]; }
      if(this.mode==='pyramid-line-plane') { base.hi=[[0,4]]; base.faces=[[0,1,2,3]]; }
      return base;
    }
    if(this.shape==='prism') {
      const pts=[]; for(let z of [-1,1]) for(let i=0;i<6;i++){let a=Math.PI/6+i*Math.PI/3; pts.push([Math.cos(a)*1.35,Math.sin(a)*1.35,z]);}
      const edges=[]; for(let i=0;i<6;i++){edges.push([i,(i+1)%6],[i+6,((i+1)%6)+6],[i,i+6]);}
      const base={pts,edges,hi:[[0,6]],faces:[],labels:['A','B','C','D','E','F','A₁','B₁','C₁','D₁','E₁','F₁']};
      if(this.mode==='prism-vertical') base.hi=[[0,6],[1,7],[2,8],[3,9],[4,10],[5,11]];
      return base;
    }
    const base = {
      pts:[[-1,-1,-1],[1,-1,-1],[1,1,-1],[-1,1,-1],[-1,-1,1],[1,-1,1],[1,1,1],[-1,1,1]],
      edges:[[0,1],[1,2],[2,3],[3,0],[4,5],[5,6],[6,7],[7,4],[0,4],[1,5],[2,6],[3,7]],
      hi:[[0,6],[1,5]], faces:[], labels:['A','B','C','D','A₁','B₁','C₁','D₁']
    };
    if(this.shape==='plane') { base.hi=[[0,6],[1,5],[0,1],[5,6]]; base.faces=[[0,1,5,6]]; }
    if(this.mode==='cube-angle-lines') { base.hi=[[0,6],[1,5]]; base.faces=[]; }
    if(this.mode==='cube-plane-angle') { base.hi=[[0,1],[1,6],[6,0],[0,1],[1,2],[2,3],[3,0]]; base.faces=[[0,1,6],[0,1,2,3]]; }
    if(this.mode==='cube-distance-plane') { base.hi=[[5,3],[3,6],[6,5]]; base.faces=[[5,3,6]]; base.specialPoint=0; }
    if(this.mode==='cube-skew') { base.hi=[[0,1],[2,6]]; base.faces=[]; }
    if(this.mode==='cube-diagonal-plane') { base.hi=[[0,2],[2,6],[6,4],[4,0]]; base.faces=[[0,2,6,4]]; base.specialPoint=1; }
    return base;
  }
  project(p){
    let [x,y,z]=p; const cx=Math.cos(this.rx),sx=Math.sin(this.rx),cy=Math.cos(this.ry),sy=Math.sin(this.ry);
    let x1=x*cy-z*sy, z1=x*sy+z*cy, y1=y*cx-z1*sx; z1=y*sx+z1*cx;
    const w=this.canvas.width,h=this.canvas.height,s=Math.min(w,h)*0.17*this.scale, persp=4/(4+z1);
    return [w/2+x1*s*persp, h/2-y1*s*persp, z1];
  }
  line(a,b,color='#2d2924',lw=2.4){
    const ctx=this.ctx; ctx.beginPath(); ctx.moveTo(a[0],a[1]); ctx.lineTo(b[0],b[1]); ctx.strokeStyle=color; ctx.lineWidth=lw; ctx.stroke();
  }
  draw(){
    const dpr=devicePixelRatio||1, rect=this.canvas.getBoundingClientRect(); this.canvas.width=rect.width*dpr; this.canvas.height=rect.height*dpr; this.ctx.setTransform(dpr,0,0,dpr,0,0); this.canvas.width=rect.width*dpr; this.canvas.height=rect.height*dpr; this.ctx.setTransform(dpr,0,0,dpr,0,0);
    const ctx=this.ctx,w=rect.width,h=rect.height; ctx.clearRect(0,0,w,h);
    ctx.fillStyle='#fffdf8'; ctx.fillRect(0,0,w,h);
    this.mode=this.canvas.dataset.mode||this.mode; const model=this.points(); const P=model.pts.map(p=>this.project(p));
    if(model.faces){ model.faces.forEach(face=>{ctx.beginPath(); face.forEach((idx,i)=>{i?ctx.lineTo(P[idx][0],P[idx][1]):ctx.moveTo(P[idx][0],P[idx][1]);}); ctx.closePath(); ctx.fillStyle='rgba(122,28,46,.12)'; ctx.fill(); ctx.strokeStyle='rgba(122,28,46,.65)'; ctx.lineWidth=2; ctx.stroke();}); }
    model.edges.forEach(e=>this.line(P[e[0]],P[e[1]],'#2d2924',2.2));
    model.hi.forEach(e=>this.line(P[e[0]],P[e[1]],'#8a1f31',4));
    P.forEach((p,i)=>{ctx.beginPath();ctx.arc(p[0],p[1], i===model.specialPoint?7:4.5,0,Math.PI*2);ctx.fillStyle=i===model.specialPoint?'#d36b42':'#8a1f31';ctx.fill(); if(model.labels[i]){ctx.fillStyle='#2d2924';ctx.font='bold 15px Georgia';ctx.fillText(model.labels[i],p[0]+8,p[1]-8);}});
    this.line([34,h-36],[104,h-36],'#547255',2.2); this.line([34,h-36],[34,h-106],'#547255',2.2); this.line([34,h-36],[74,h-76],'#547255',2.2);
    ctx.fillStyle='#547255';ctx.font='14px Georgia';ctx.fillText('x',110,h-31);ctx.fillText('z',27,h-111);ctx.fillText('y',78,h-78);
    ctx.fillStyle='#7a1c2e';ctx.font='12px monospace';ctx.fillText('INTERACTIVE 3D',w-150,32);
  }
}

document.addEventListener('DOMContentLoaded',()=>{
  renderTabs(); renderTheory(0); renderEge(); renderFilters(); renderBank('Все'); initCanvases();
  setInterval(()=>{state.renderers.forEach(r=>{if(!r.drag){r.ry+=0.004;r.draw();}})},30);
  document.querySelectorAll('[data-shape-btn]').forEach(b=>b.onclick=()=>{document.querySelectorAll('[data-shape-btn]').forEach(x=>x.classList.remove('active')); b.classList.add('active'); const c=document.getElementById('theoryCanvas'); c.dataset.shape=b.dataset.shapeBtn; c.dataset.mode=b.dataset.shapeBtn; const r=getRenderer(c); r.shape=b.dataset.shapeBtn; r.mode=b.dataset.shapeBtn; r.draw();});
});
</script>
</body>
</html>
