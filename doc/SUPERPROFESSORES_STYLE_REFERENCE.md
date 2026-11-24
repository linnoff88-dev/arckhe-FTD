# 🎓 SuperProfessores - Guia de Referência de Estilos e Layout

> **Transformando educadores em arquitetos do futuro da aprendizagem**
> Sistema de Design Completo com Modelo Híbrido de Trilhas

**Versão:** 3.0 | **Data:** 2025-11-12 | **Autor:** BMad Orchestrator

---

## 📋 Índice Rápido

- [Visão Geral](#visão-geral)
- [Identidade Visual](#identidade-visual)
- [Sistema de Cores](#sistema-de-cores)
- [Tipografia](#tipografia)
- [Espaçamento e Grid](#espaçamento-e-grid)
- [Componentes](#componentes)
- [Dark Mode](#dark-mode)
- [Responsividade](#responsividade)
- [Código de Exemplo](#código-de-exemplo)

---

## 🎯 Visão Geral

### Sobre o Projeto

**SuperProfessores** é um programa de formação de educadores em IA com estrutura híbrida:
- **Nível 1** (Fundamentos) - Base obrigatória
- **Trilha A** (Professor 2.0) - Usar IA como ferramenta
- **Trilha B** (Educador de IA) - Ensinar IA para alunos

### Princípios de Design

1. ✅ **Resiliência** - Design que suporta atualizações frequentes
2. ✅ **Clareza** - Estrutura híbrida visualmente clara
3. ✅ **Densidade** - Máxima informação com legibilidade
4. ✅ **Dark Mode** - Suporte completo ao modo escuro
5. ✅ **Mobile-First** - Responsivo em todos os dispositivos

### Stack Tecnológico

```
Framework CSS:  Tailwind CSS 3.x (CDN)
JavaScript:     Vanilla JS (app.js)
Fontes:         Google Fonts - Inter
Dark Mode:      Class-based (HTML class="dark")
Build:          HTML puro (sem build process)
```

---

## 🎨 Identidade Visual

### Logo e Marca

```
Nome:     SuperProfessores
Ícone:    🎓
Cor:      Gradiente (Blue → Purple → Green)
Tagline:  "Transformando educadores em arquitetos do futuro da aprendizagem"
```

### Personalidade

- **Tom**: Educacional, inovador, acessível
- **Estilo**: Moderno, profissional, educativo
- **Emoção**: Empoderamento, transformação, futuro

---

## 🌈 Sistema de Cores

### Cores por Nível/Trilha (PRINCIPAL)

```css
/* Estrutura Híbrida */
🔵 Nível 1 (Fundamentos):      #3B82F6  /* Azul - Base comum */
🟣 Trilha A (Professor 2.0):   #9b59b6  /* Roxo - Usar IA */
🟢 Trilha B (Educador de IA):  #10B981  /* Verde - Ensinar IA */
```

### ⚠️ Diferença do FEP

```
FEP usa cores por NÍVEL (linear):
  Verde → Azul → Roxo

SuperProfessores usa cores por TRILHA (bifurcação):
  Azul (base) → Roxo OU Verde
```

### Paleta Completa

```css
/* Cores Principais */
--primary:        #3B82F6;   /* Blue 500 - Azul padrão */
--trilha-a:       #9b59b6;   /* Roxo - Trilha A */
--trilha-b:       #10B981;   /* Verde - Trilha B */
--fundamentos:    #3B82F6;   /* Azul - Nível 1 */
--success:        #22C55E;   /* Verde success */
--warning:        #F59E0B;   /* Amarelo warning */
--error:          #EF4444;   /* Vermelho error */

/* Escala de Neutrals (Light Mode) */
--neutral-50:     #fafafa;
--neutral-100:    #f5f5f5;
--neutral-200:    #e5e5e5;
--neutral-300:    #d4d4d4;
--neutral-400:    #a3a3a3;
--neutral-600:    #525252;
--neutral-700:    #404040;
--neutral-800:    #262626;
--neutral-900:    #171717;

/* Dark Mode (aplicado com dark:) */
dark:bg-neutral-800    /* Fundo de cards */
dark:bg-neutral-900    /* Fundo de página */
dark:text-neutral-100  /* Texto principal */
dark:border-neutral-700 /* Bordas */
```

### Gradientes

```css
/* Hero Multi-cor (Index) */
background: linear-gradient(to right, #3B82F6, #9b59b6, #10B981);
/* Blue → Purple → Green (representa as 3 partes) */

/* Nível 1 (Fundamentos) */
background: linear-gradient(to right, #3B82F6, #2563EB);
/* from-primary to-blue-600 */

/* Trilha A (Roxo) */
background: linear-gradient(to right, #9b59b6, #8e44ad);
/* from-trilha-a to darker purple */

/* Trilha B (Verde) */
background: linear-gradient(to right, #10B981, #059669);
/* from-trilha-b to-green-600 */
```

### Uso por Contexto

| Elemento | Nível 1 | Trilha A | Trilha B |
|----------|---------|----------|----------|
| **Cor Principal** | `#3B82F6` | `#9b59b6` | `#10B981` |
| **Cor Hover** | `#2563EB` | `#8e44ad` | `#059669` |
| **Badge** | `bg-primary` | `bg-trilha-a` | `bg-trilha-b` |
| **Border** | `border-primary` | `border-trilha-a` | `border-trilha-b` |
| **Gradiente Hero** | Blue→DarkBlue | Purple→DarkPurple | Green→DarkGreen |

---

## 📝 Tipografia

### Família de Fontes

```html
<!-- Google Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

```css
body {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;
}
```

### Hierarquia Tipográfica

```css
/* Desktop */
H1 (Hero):      text-4xl lg:text-5xl     (36-48px) | font-weight: 700
H2 (Section):   text-3xl                 (30px)    | font-weight: 700
H3 (Card):      text-2xl                 (24px)    | font-weight: 700
H4 (Subsection): text-xl                 (20px)    | font-weight: 600
Body:           text-base                (16px)    | font-weight: 400
Small:          text-sm                  (14px)    | font-weight: 400

/* Mobile */
H1: text-4xl (36px)
H2: text-3xl (30px)
H3: text-2xl (24px)
```

### Classes Tailwind

```html
<!-- Hero Title -->
<h1 class="text-4xl lg:text-5xl font-bold text-neutral-900 dark:text-neutral-100">
  Título
</h1>

<!-- Section Title -->
<h2 class="text-3xl font-bold text-neutral-900 dark:text-neutral-100 mb-4">
  Seção
</h2>

<!-- Card Title -->
<h3 class="text-2xl font-bold text-neutral-900 dark:text-neutral-100">
  Card
</h3>

<!-- Body Text -->
<p class="text-base text-neutral-600 dark:text-neutral-400">
  Texto
</p>
```

**⚠️ Importante:** Sempre incluir variante `dark:` em textos e backgrounds!

---

## 📏 Espaçamento e Grid

### Sistema de Espaçamento (Base: 1rem = 16px)

```
Padding interno cards:   p-6 ou p-8        (24px ou 32px)
Margin entre seções:     mb-12 ou mb-16    (48px ou 64px)
Gap em grids:            gap-6 ou gap-8    (24px ou 32px)
Padding de container:    px-4 sm:px-6 lg:px-8
Max width container:     max-w-7xl         (1280px)
```

### Container Padrão

```html
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
  <!-- Conteúdo -->
</div>
```

### Grids Responsivos

```html
<!-- 2 colunas (Trilhas A e B) -->
<div class="grid lg:grid-cols-2 gap-8">

<!-- 3 colunas (Módulos) -->
<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-4">

<!-- 4 colunas (Stats) -->
<div class="grid grid-cols-2 lg:grid-cols-4 gap-8">
```

### Breakpoints

```
sm:  640px   - Smartphone landscape
md:  768px   - Tablets
lg:  1024px  - Desktop
xl:  1280px  - Large desktop
```

---

## 🧩 Componentes

### 1. Navegação (Sticky)

```html
<nav class="sticky top-0 z-50 bg-white/90 dark:bg-neutral-800/90 backdrop-blur-sm border-b border-neutral-200 dark:border-neutral-700">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between items-center h-16">

      <!-- Logo -->
      <div class="flex items-center">
        <a href="../index.html" class="text-2xl font-bold bg-gradient-to-r from-primary to-trilha-a bg-clip-text text-transparent">
          🎓 SuperProfessores
        </a>
      </div>

      <!-- Desktop Menu -->
      <div class="hidden md:flex items-center space-x-8">
        <a href="../index.html" class="text-neutral-700 dark:text-neutral-300 hover:text-primary">
          Início
        </a>
        <a href="../index.html#trilhas" class="text-neutral-700 dark:text-neutral-300 hover:text-primary">
          Trilhas
        </a>
        <a href="https://github.com/linnoff88-dev/SuperProf" class="text-neutral-700 dark:text-neutral-300 hover:text-primary">
          GitHub
        </a>

        <!-- Dark Mode Toggle -->
        <button id="theme-toggle" class="p-2 rounded-lg bg-neutral-100 dark:bg-neutral-700 hover:bg-neutral-200 dark:hover:bg-neutral-600">
          <!-- Ícones SVG aqui -->
        </button>
      </div>

      <!-- Mobile Menu Button -->
      <button id="mobile-menu-btn" class="md:hidden">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
      </button>

    </div>
  </div>

  <!-- Mobile Menu -->
  <div id="mobile-menu" class="hidden md:hidden bg-white dark:bg-neutral-800 border-t border-neutral-200 dark:border-neutral-700">
    <div class="px-4 py-2 space-y-1">
      <a href="../index.html" class="block px-3 py-2 rounded-md hover:bg-neutral-100 dark:hover:bg-neutral-700">
        Início
      </a>
      <!-- Mais links -->
    </div>
  </div>
</nav>
```

**Características:**
- Sticky: `sticky top-0 z-50`
- Transparência: `bg-white/90 dark:bg-neutral-800/90`
- Backdrop blur: `backdrop-blur-sm`
- Dark mode completo
- Mobile menu expansível

---

### 2. Breadcrumb

```html
<div class="bg-white dark:bg-neutral-800 border-b border-neutral-200 dark:border-neutral-700">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
    <nav class="flex text-sm" aria-label="Breadcrumb">
      <a href="../index.html" class="text-primary hover:text-blue-700 dark:hover:text-blue-400">
        Início
      </a>
      <span class="mx-2 text-neutral-400">/</span>
      <a href="../niveis/nivel-1.html" class="text-primary hover:text-blue-700 dark:hover:text-blue-400">
        Nível 1
      </a>
      <span class="mx-2 text-neutral-400">/</span>
      <span class="text-neutral-600 dark:text-neutral-400">
        Módulo 1.1
      </span>
    </nav>
  </div>
</div>
```

**Padrões:**
- Módulo: `Início > Nível X > Módulo X.X`
- Nível: `Início > Trilha X > Nível X`
- Trilha: `Início > Trilha X`

---

### 3. Hero Section

```html
<section class="bg-gradient-to-r from-primary to-blue-600 py-16">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-white">

    <!-- Badges -->
    <div class="flex items-center gap-4 mb-4">
      <span class="inline-block px-4 py-2 bg-white/20 rounded-full text-sm font-semibold">
        60 horas
      </span>
      <span class="inline-block px-4 py-2 bg-white/20 rounded-full text-sm font-semibold">
        Obrigatório
      </span>
    </div>

    <!-- Título -->
    <h1 class="text-4xl lg:text-5xl font-bold mb-4">
      Nível 1: Fundamentos de IA
    </h1>

    <!-- Descrição -->
    <p class="text-xl text-white/90 mb-6">
      Base comum para todas as trilhas
    </p>

    <!-- Stats Grid -->
    <div class="grid md:grid-cols-3 gap-4 mt-8">
      <div class="bg-white/10 backdrop-blur p-4 rounded-lg">
        <div class="text-2xl font-bold">5</div>
        <div class="text-sm text-blue-100">Módulos</div>
      </div>
      <!-- Mais stats -->
    </div>

  </div>
</section>
```

**Cores por contexto:**
- Nível 1: `from-primary to-blue-600`
- Trilha A: `from-trilha-a to-purple-700`
- Trilha B: `from-trilha-b to-green-600`

---

### 4. Module Card (Chapter Card)

```html
<div class="chapter-card bg-white dark:bg-neutral-800 rounded-2xl shadow-lg p-8 mb-8 border-2 border-transparent hover:border-primary transition-all">

  <!-- Header -->
  <div class="flex items-start justify-between mb-6">
    <div>
      <span class="inline-block px-3 py-1 bg-primary/10 text-primary rounded-full text-sm font-semibold mb-3">
        12 horas
      </span>
      <h2 class="text-3xl font-bold text-neutral-900 dark:text-neutral-100 mb-2">
        Módulo 1.1: Introdução à IA
      </h2>
      <p class="text-neutral-600 dark:text-neutral-400">
        Fundamentos essenciais de Inteligência Artificial
      </p>
    </div>
  </div>

  <!-- Action Buttons -->
  <div class="flex flex-wrap gap-3 mb-6">
    <!-- Botão 1: Ver em Modal -->
    <button onclick="openModal('modulo-1-1')" class="px-6 py-3 bg-primary text-white rounded-lg font-semibold hover:bg-blue-700 transition-colors flex items-center gap-2">
      <span>📖</span>
      <span>Ver em Modal</span>
    </button>

    <!-- Botão 2: Página Completa -->
    <a href="../modulos/modulo-1-1.html" class="px-6 py-3 bg-transparent border-2 border-primary text-primary rounded-lg font-semibold hover:bg-primary hover:text-white transition-colors flex items-center gap-2">
      <span>📄</span>
      <span>Abrir Página Completa</span>
    </a>

    <!-- Botão 3: Download -->
    <a href="../pdfs/modulo-1-1.md" download class="px-6 py-3 bg-transparent border-2 border-neutral-300 dark:border-neutral-600 text-neutral-700 dark:text-neutral-300 rounded-lg font-semibold hover:bg-neutral-100 dark:hover:bg-neutral-700 transition-colors flex items-center gap-2">
      <span>📥</span>
      <span>Download PDF/MD</span>
    </a>
  </div>

  <!-- Tópicos Expansíveis (ver próxima seção) -->

</div>
```

**Características:**
- Border transparente que fica colorido no hover
- 3 botões padrão (Modal, Página, Download)
- Shadow-lg
- Padding 8 (32px)
- Border radius 2xl

---

### 5. Tópicos Expansíveis - ULTRA COMPACTOS

**⭐ Diferencial SuperProfessores:** Espaçamento **reduzido em 67-75%** vs FEP

```html
<div class="mb-4">
  <h3 class="font-semibold text-neutral-900 dark:text-neutral-100 mb-3 text-lg">
    📚 Tópicos-chave do módulo:
  </h3>

  <ul class="topics-list space-y-0.5">
    <!-- Tópico 1 -->
    <li class="topic-item" data-topic="m1-1-ia-definicao">
      <button class="topic-button w-full text-left px-4 py-1 bg-neutral-50 dark:bg-neutral-700 hover:bg-neutral-100 dark:hover:bg-neutral-600 rounded-lg transition-colors font-medium text-neutral-800 dark:text-neutral-200">
        🎯 O que é Inteligência Artificial
      </button>

      <div class="topic-explanation hidden ml-6 mt-2 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-primary">
        <p class="text-sm mb-1.5 text-neutral-700 dark:text-neutral-300">
          <strong class="text-primary">O que é:</strong> Definição clara e objetiva do conceito
        </p>
        <p class="text-sm mb-1.5 text-neutral-700 dark:text-neutral-300">
          <strong class="text-primary">Por que aprender:</strong> Justificativa pedagógica/prática
        </p>
        <p class="text-sm text-neutral-700 dark:text-neutral-300">
          <strong class="text-primary">Conceitos chave:</strong> Termos relacionados
        </p>
      </div>
    </li>

    <!-- Mais tópicos... -->
  </ul>
</div>
```

**Espaçamento Ultra-Compacto:**

| Elemento | FEP (Original) | SuperProfessores | Redução |
|----------|----------------|------------------|---------|
| Entre botões | `space-y-2` (8px) | `space-y-0.5` (2px) | **-75%** |
| Padding botão | `py-3` (12px) | `py-1` (4px) | **-67%** |
| Entre parágrafos | `mb-2` (8px) | `mb-1.5` (6px) | **-25%** |

**JavaScript (app.js):**

```javascript
/* TOPIC EXPANSION SYSTEM (FEP Pattern - Compact) */
document.addEventListener('click', function(e) {
  const topicButton = e.target.closest('.topic-button');

  if (topicButton) {
    const topicItem = topicButton.closest('.topic-item');
    const explanation = topicItem.querySelector('.topic-explanation');

    if (explanation) {
      const wasHidden = explanation.classList.contains('hidden');

      // Fechar todos os outros tópicos (accordion behavior)
      const chapterCard = topicItem.closest('.chapter-card');
      if (chapterCard) {
        chapterCard.querySelectorAll('.topic-explanation').forEach(exp => {
          exp.classList.add('hidden');
        });
      }

      // Toggle tópico atual
      if (wasHidden) {
        explanation.classList.remove('hidden');
      }
    }
  }
});
```

---

### 6. Modal System

**CSS (incluir no `<style>`):**

```css
.modal {
  display: none;
  position: fixed;
  z-index: 100;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0,0,0,0.6);
  backdrop-filter: blur(4px);
}

.modal.active {
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal-content {
  background-color: white;
  margin: auto;
  padding: 0;
  width: 90%;
  max-width: 1000px;
  max-height: 90vh;
  border-radius: 1rem;
  overflow: hidden;
  box-shadow: 0 20px 25px rgba(0,0,0,0.3);
}

.dark .modal-content {
  background-color: #1f2937;
}

.modal-header {
  padding: 1.5rem 2rem;
  border-bottom: 1px solid #e5e7eb;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.dark .modal-header {
  border-bottom-color: #374151;
}

.modal-body {
  padding: 2rem;
  overflow-y: auto;
  max-height: calc(90vh - 80px);
}

.close-modal {
  color: #9ca3af;
  font-size: 2rem;
  font-weight: 700;
  cursor: pointer;
}

.close-modal:hover {
  color: #ef4444;
}
```

**HTML:**

```html
<div id="modulo-1-1" class="modal">
  <div class="modal-content">
    <div class="modal-header">
      <h2 class="text-2xl font-bold text-neutral-900 dark:text-neutral-100">
        Módulo 1.1: Introdução à IA
      </h2>
      <span class="close-modal">&times;</span>
    </div>
    <div class="modal-body">
      <!-- Conteúdo completo do módulo -->
      <p class="text-neutral-700 dark:text-neutral-300">Conteúdo aqui...</p>
    </div>
  </div>
</div>
```

**JavaScript:**

```javascript
// Abrir modal
function openModal(modalId) {
  const modal = document.getElementById(modalId);
  if (modal) {
    modal.classList.add('active');
    document.body.style.overflow = 'hidden';
  }
}

// Fechar modal
function closeModal(modalId) {
  const modal = document.getElementById(modalId);
  if (modal) {
    modal.classList.remove('active');
    document.body.style.overflow = 'auto';
  }
}

// Event listeners
document.addEventListener('click', function(e) {
  // Fechar ao clicar no X
  if (e.target.classList.contains('close-modal')) {
    const modal = e.target.closest('.modal');
    if (modal) {
      modal.classList.remove('active');
      document.body.style.overflow = 'auto';
    }
  }

  // Fechar ao clicar fora
  if (e.target.classList.contains('modal')) {
    e.target.classList.remove('active');
    document.body.style.overflow = 'auto';
  }
});

// Fechar com ESC
document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') {
    const activeModal = document.querySelector('.modal.active');
    if (activeModal) {
      activeModal.classList.remove('active');
      document.body.style.overflow = 'auto';
    }
  }
});
```

---

### 7. Footer

```html
<footer class="bg-neutral-900 dark:bg-black text-neutral-300 py-12">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid md:grid-cols-3 gap-8">

      <!-- Coluna 1 -->
      <div>
        <h3 class="text-xl font-bold text-white mb-4">SuperProfessores</h3>
        <p class="text-sm">Transformando educadores em arquitetos do futuro da aprendizagem</p>
      </div>

      <!-- Coluna 2 -->
      <div>
        <h4 class="font-semibold text-white mb-4">Links Rápidos</h4>
        <ul class="space-y-2 text-sm">
          <li><a href="#" class="hover:text-white">Início</a></li>
          <li><a href="#" class="hover:text-white">Trilhas</a></li>
          <li><a href="#" class="hover:text-white">GitHub</a></li>
        </ul>
      </div>

      <!-- Coluna 3 -->
      <div>
        <h4 class="font-semibold text-white mb-4">Contato</h4>
        <ul class="space-y-2 text-sm">
          <li><a href="mailto:linnoff88-dev@gmail.com" class="hover:text-white">Email</a></li>
          <li><a href="https://github.com/linnoff88-dev" class="hover:text-white">GitHub</a></li>
        </ul>
      </div>

    </div>

    <div class="border-t border-neutral-800 mt-8 pt-8 text-center text-sm">
      <p>&copy; 2025 SuperProfessores. Licença MIT.</p>
    </div>
  </div>
</footer>
```

---

## 🌙 Dark Mode

### Implementação Completa

**1. HTML Setup:**

```html
<html lang="pt-BR" class="scroll-smooth">
<!-- A classe "dark" é adicionada/removida no <html> -->
```

**2. Tailwind Config:**

```html
<script>
tailwind.config = {
  darkMode: 'class', // ESSENCIAL!
  theme: {
    extend: {
      colors: {
        primary: '#3B82F6',
        'trilha-a': '#9b59b6',
        'trilha-b': '#10B981',
        fundamentos: '#3B82F6',
        success: '#22C55E',
        warning: '#F59E0B',
        error: '#EF4444',
      }
    }
  }
}
</script>
```

**3. CSS Transitions:**

```css
* {
  transition: background-color 200ms ease-in-out,
              border-color 200ms ease-in-out,
              color 200ms ease-in-out;
}

.preload * {
  transition: none !important;
}
```

**4. Padrões de Classes:**

```html
<!-- Backgrounds -->
bg-white dark:bg-neutral-800
bg-neutral-50 dark:bg-neutral-900
bg-neutral-100 dark:bg-neutral-700

<!-- Textos -->
text-neutral-900 dark:text-neutral-100
text-neutral-700 dark:text-neutral-300
text-neutral-600 dark:text-neutral-400

<!-- Bordas -->
border-neutral-200 dark:border-neutral-700
border-neutral-300 dark:border-neutral-600

<!-- Transparências -->
bg-white/90 dark:bg-neutral-800/90

<!-- Overlays -->
bg-blue-50 dark:bg-blue-900/20
bg-success/10 dark:bg-success/20
```

**5. JavaScript (app.js):**

```javascript
const themeToggle = document.getElementById('theme-toggle');
const html = document.documentElement;

// Carregar preferência salva
const currentTheme = localStorage.getItem('theme');

if (currentTheme === 'dark') {
  html.classList.add('dark');
  updateThemeIcon(true);
} else if (currentTheme === 'light') {
  html.classList.remove('dark');
  updateThemeIcon(false);
} else {
  // Detectar preferência do sistema
  if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
    html.classList.add('dark');
    localStorage.setItem('theme', 'dark');
    updateThemeIcon(true);
  }
}

// Toggle ao clicar
themeToggle.addEventListener('click', function() {
  const isDark = html.classList.toggle('dark');
  const newTheme = isDark ? 'dark' : 'light';
  localStorage.setItem('theme', newTheme);
  updateThemeIcon(isDark);
});

function updateThemeIcon(isDark) {
  const darkIcon = document.getElementById('theme-toggle-dark-icon');
  const lightIcon = document.getElementById('theme-toggle-light-icon');

  if (isDark) {
    lightIcon.classList.remove('hidden');
    darkIcon.classList.add('hidden');
  } else {
    darkIcon.classList.remove('hidden');
    lightIcon.classList.add('hidden');
  }
}
```

**6. Botão de Toggle (SVG Icons):**

```html
<button id="theme-toggle" class="p-2 rounded-lg bg-neutral-100 dark:bg-neutral-700 hover:bg-neutral-200 dark:hover:bg-neutral-600">
  <!-- Lua (mostrar quando estiver em light mode) -->
  <svg id="theme-toggle-dark-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
    <path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"></path>
  </svg>

  <!-- Sol (mostrar quando estiver em dark mode) -->
  <svg id="theme-toggle-light-icon" class="hidden w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
    <path d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z" fill-rule="evenodd" clip-rule="evenodd"></path>
  </svg>
</button>
```

---

## 📱 Responsividade

### Estratégia: Mobile-First

```
Base (Mobile):     < 640px
Tablet (sm):       >= 640px
Desktop (md):      >= 768px
Large Desktop (lg): >= 1024px
XL Desktop (xl):   >= 1280px
```

### Padrões Responsivos

```html
<!-- Container Principal -->
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

<!-- Grids Responsivos -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
<div class="grid lg:grid-cols-2 gap-8">
<div class="grid grid-cols-2 lg:grid-cols-4 gap-8">

<!-- Tipografia Responsiva -->
<h1 class="text-4xl lg:text-5xl font-bold">
<h2 class="text-3xl lg:text-4xl font-bold">
<p class="text-base lg:text-lg">

<!-- Flex Direction -->
<div class="flex flex-col sm:flex-row gap-4">

<!-- Visibilidade -->
<div class="hidden md:flex items-center space-x-8">
<button class="md:hidden">

<!-- Espaçamento Responsivo -->
<section class="py-12 lg:py-20">
<div class="mb-8 lg:mb-16">
```

---

## 🎬 Código de Exemplo Completo

```html
<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SuperProfessores | Transformando Educadores</title>
  <meta name="description" content="Programa de formação de educadores em IA">

  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Tailwind Config -->
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            primary: '#3B82F6',
            'trilha-a': '#9b59b6',
            'trilha-b': '#10B981',
            fundamentos: '#3B82F6',
            success: '#22C55E',
            warning: '#F59E0B',
            error: '#EF4444',
          },
          fontFamily: {
            sans: ['Inter', '-apple-system', 'BlinkMacSystemFont', 'Segoe UI', 'Roboto', 'sans-serif'],
          },
        }
      }
    }
  </script>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

  <!-- Custom CSS -->
  <style>
    * {
      transition: background-color 200ms ease-in-out, border-color 200ms ease-in-out, color 200ms ease-in-out;
    }
    .preload * {
      transition: none !important;
    }

    /* Modal CSS */
    .modal {
      display: none;
      position: fixed;
      z-index: 100;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0,0,0,0.6);
      backdrop-filter: blur(4px);
    }
    .modal.active {
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .modal-content {
      background-color: white;
      margin: auto;
      padding: 0;
      width: 90%;
      max-width: 1000px;
      max-height: 90vh;
      border-radius: 1rem;
      overflow: hidden;
      box-shadow: 0 20px 25px rgba(0,0,0,0.3);
    }
    .dark .modal-content {
      background-color: #1f2937;
    }
    .modal-header {
      padding: 1.5rem 2rem;
      border-bottom: 1px solid #e5e7eb;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .dark .modal-header {
      border-bottom-color: #374151;
    }
    .modal-body {
      padding: 2rem;
      overflow-y: auto;
      max-height: calc(90vh - 80px);
    }
    .close-modal {
      color: #9ca3af;
      font-size: 2rem;
      font-weight: 700;
      cursor: pointer;
    }
    .close-modal:hover {
      color: #ef4444;
    }
  </style>
</head>
<body class="preload bg-neutral-50 dark:bg-neutral-900 text-neutral-900 dark:text-neutral-100">

  <!-- Navigation -->
  <nav class="sticky top-0 z-50 bg-white/90 dark:bg-neutral-800/90 backdrop-blur-sm border-b border-neutral-200 dark:border-neutral-700">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <a href="/" class="text-2xl font-bold bg-gradient-to-r from-primary to-trilha-a bg-clip-text text-transparent">
          🎓 SuperProfessores
        </a>
        <div class="hidden md:flex items-center space-x-8">
          <a href="#" class="text-neutral-700 dark:text-neutral-300 hover:text-primary">Início</a>
          <a href="#" class="text-neutral-700 dark:text-neutral-300 hover:text-primary">Trilhas</a>
          <button id="theme-toggle" class="p-2 rounded-lg bg-neutral-100 dark:bg-neutral-700">🌙</button>
        </div>
      </div>
    </div>
  </nav>

  <!-- Hero -->
  <section class="bg-gradient-to-r from-primary via-trilha-a to-trilha-b py-20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center text-white">
      <h1 class="text-4xl lg:text-5xl font-bold mb-6">
        Transforme sua Prática Educacional com IA
      </h1>
      <p class="text-xl mb-8">
        Escolha sua especialização
      </p>
      <button class="bg-white text-primary px-8 py-4 rounded-lg font-bold hover:bg-neutral-100">
        Começar Agora
      </button>
    </div>
  </section>

  <!-- Trilhas -->
  <section class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
    <div class="grid lg:grid-cols-2 gap-8">
      <!-- Trilha A -->
      <div class="bg-white dark:bg-neutral-800 border-2 border-purple-200 dark:border-purple-800 rounded-2xl p-8 hover:-translate-y-2 transition-all shadow-lg">
        <h3 class="text-3xl font-bold text-neutral-900 dark:text-neutral-100 mb-4">
          🟣 Trilha A: Professor 2.0
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400 mb-6">
          Usar IA como ferramenta pedagógica
        </p>
        <button class="w-full bg-trilha-a text-white py-3 rounded-lg font-semibold hover:opacity-90">
          Explorar
        </button>
      </div>

      <!-- Trilha B -->
      <div class="bg-white dark:bg-neutral-800 border-2 border-green-200 dark:border-green-800 rounded-2xl p-8 hover:-translate-y-2 transition-all shadow-lg">
        <h3 class="text-3xl font-bold text-neutral-900 dark:text-neutral-100 mb-4">
          🟢 Trilha B: Educador de IA
        </h3>
        <p class="text-neutral-600 dark:text-neutral-400 mb-6">
          Ensinar IA para alunos
        </p>
        <button class="w-full bg-trilha-b text-white py-3 rounded-lg font-semibold hover:opacity-90">
          Explorar
        </button>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-neutral-900 dark:bg-black text-neutral-300 py-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
      <p>&copy; 2025 SuperProfessores</p>
    </div>
  </footer>

  <!-- JavaScript -->
  <script src="js/app.js"></script>
</body>
</html>
```

---

## 📚 Quick Reference

### Classes Mais Usadas

```css
/* Containers */
.container       → max-w-7xl mx-auto px-4 sm:px-6 lg:px-8

/* Cards */
.card            → bg-white dark:bg-neutral-800 rounded-2xl shadow-lg p-8

/* Buttons */
.btn-primary     → bg-primary text-white px-6 py-3 rounded-lg hover:bg-blue-700
.btn-secondary   → border-2 border-primary text-primary px-6 py-3 rounded-lg hover:bg-primary hover:text-white

/* Badges */
.badge           → inline-block px-3 py-1 bg-primary/10 text-primary rounded-full text-sm font-semibold

/* Text */
.title           → text-4xl lg:text-5xl font-bold text-neutral-900 dark:text-neutral-100
.subtitle        → text-xl text-neutral-600 dark:text-neutral-400

/* Gradients */
.gradient-hero   → bg-gradient-to-r from-primary via-trilha-a to-trilha-b
```

---

## ✅ Checklist de Implementação

### Setup Inicial
- [ ] Incluir Tailwind CSS CDN
- [ ] Incluir Google Fonts (Inter)
- [ ] Configurar Tailwind config com cores customizadas
- [ ] Adicionar CSS de transições
- [ ] Incluir CSS de modais (se necessário)

### Dark Mode
- [ ] Configurar `darkMode: 'class'` no Tailwind
- [ ] Adicionar classe `preload` no body
- [ ] Implementar JavaScript de dark mode toggle
- [ ] Adicionar variante `dark:` em TODOS os backgrounds
- [ ] Adicionar variante `dark:` em TODOS os textos
- [ ] Adicionar variante `dark:` em TODAS as bordas

### Componentes
- [ ] Navegação sticky com backdrop blur
- [ ] Breadcrumb (páginas internas)
- [ ] Hero section com gradiente correto
- [ ] Module cards com 3 botões padrão
- [ ] Tópicos expansíveis ultra-compactos
- [ ] Modais (se página de nível)
- [ ] Footer com 3 colunas

### Responsividade
- [ ] Container com padding responsivo
- [ ] Grids com breakpoints corretos
- [ ] Tipografia responsiva
- [ ] Menu mobile funcional
- [ ] Testar em 3 tamanhos (mobile, tablet, desktop)

### JavaScript
- [ ] Incluir `app.js` antes de `</body>`
- [ ] Dark mode toggle funcional
- [ ] Mobile menu funcional
- [ ] Tópicos expansíveis funcionando
- [ ] Modais abrindo/fechando
- [ ] Remove classe `preload` após load

---

## 🎯 Regras de Ouro

### ✅ SEMPRE FAZER:

1. Incluir Tailwind Config completo em toda página
2. Aplicar variantes `dark:` a TODOS os elementos com cor
3. Usar container: `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`
4. Incluir `app.js` antes de `</body>`
5. Adicionar classe `preload` no body
6. Usar emojis para ícones (consistência)
7. Manter padding/margin múltiplos de 4
8. Testar dark mode em todos os elementos
9. Validar responsividade em 3 breakpoints
10. Usar cores específicas por trilha/nível

### ❌ NUNCA FAZER:

1. Não usar CSS inline (sempre Tailwind)
2. Não esquecer variantes `dark:`
3. Não misturar cores de diferentes níveis/trilhas
4. Não copiar apenas parte do Tailwind config
5. Não usar z-index aleatórios (nav=50, modal=100)
6. Não esquecer transition em elementos hover
7. Não usar espaçamento diferente dos padrões compactos
8. Não esquecer meta tags (charset, viewport)
9. Não deixar console.errors
10. Não confundir FEP com SuperProfessores

---

## 🆚 Diferenças vs FEP

| Aspecto | FEP | SuperProfessores |
|---------|-----|------------------|
| **Estrutura** | 3 níveis lineares | 1 base + 2 trilhas |
| **Cores** | Verde→Azul→Roxo (por nível) | Azul(base)+Roxo/Verde(trilhas) |
| **Espaçamento** | Confortável (8-12px) | Ultra-compacto (2-4px) |
| **Dark Mode** | Não especificado | Completo |
| **Público** | Geral | Educadores |

---

**Última atualização:** 2025-11-12
**Versão:** 3.0 (Modelo Híbrido)
**Autor:** BMad Orchestrator

---

