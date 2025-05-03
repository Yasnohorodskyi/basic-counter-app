# Basic Counter App

A simple Vue 3 application that simulates a basic counter with two components interacting through a shared state using Pinia.

## ✨ Features

- 📈 Increment and decrement a shared count value.
- 🔄 Real-time count updates across components.
- 📦 Shared state managed via [Pinia](https://pinia.vuejs.org/).
- 💅 Clean UI with animated counter and Material Design–inspired buttons.

## 📁 App Structure

```
src/
├── components/
│   ├── Counter.vue      # Increments/decrements the counter
│   ├── Display.vue      # Displays current counter value
│   ├── Card.vue         # Reusable layout wrapper
│   └── Count.vue        # Animated count display
├── stores/
│   └── counter.js       # Pinia store for shared count state
├── App.vue              # Main app layout, includes both components
├── main.js              # App entry point and Pinia setup
```

## 🚀 Setup & Run Instructions

### 1. Install dependencies

```bash
npm install
```

### 2. Run the development server

```bash
npm run dev
```

Open your browser at: [http://localhost:5173](http://localhost:5173)

### 3. Build for production

```bash
npm run build
```

### 4. Preview production build

```bash
npm run preview
```

### 5. Format source files

```bash
npm run format
```

## 🧰 Tech Stack

- **Vue 3**
- **Pinia** for state management
- **Vite** for fast development
- **Prettier** for code formatting
