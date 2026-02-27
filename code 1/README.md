# 🎨 Glassmorphism Card Component

A modern, premium UI component featuring the Glassmorphism design trend with Vue 3 Composition API and pure CSS.

## ✨ Features

- 🔮 **Glassmorphism Effect** - Frosted glass with backdrop blur
- ⚡ **Smooth Animations** - Bounce transitions on hover
- 📱 **Fully Responsive** - CSS Grid with auto-fit
- 🎯 **Vue 3 Composition API** - Reactive state management
- ♿ **Accessible** - Reduced motion support
- 🌙 **Dark Mode Ready** - System preference detection

## 🚀 Quick Start

### Option 1: Pure HTML/CSS (No Build Required)

Simply open `index.html` in your browser!

```bash
# Open directly
open index.html

# Or use a local server
npx serve .
```

### Option 2: Vue 3 Project

1. **Install the component:**
   ```bash
   npm create vue@latest my-app
   cd my-app
   npm install
   ```

2. **Copy `GlassCard.vue` to your components folder**

3. **Import and use:**
   ```vue
   <script setup>
   import GlassCard from './components/GlassCard.vue'
   </script>

   <template>
     <GlassCard />
   </template>
   ```

## 🎨 Customization

### Change Colors

Edit the CSS variables in `styles.css`:

```css
:root {
  --gradient-primary: #667eea;    /* Your color */
  --gradient-secondary: #764ba2;  /* Your color */
  --glass-blur: 20px;             /* Blur intensity */
}
```

### Modify Cards

Update the data in `GlassCard.vue`:

```javascript
const cards = ref([
  {
    id: 1,
    icon: '⚡',           // Any emoji
    title: 'Your Title',
    description: 'Your description',
    likes: '2.4k',
    comments: '142',
    isHovered: false
  },
  // Add more cards...
])
```

## 📁 File Structure

```
code 1/
├── GlassCard.vue       # Vue 3 Component
├── index.html          # Standalone HTML demo
├── styles.css          # Pure CSS version
├── README.md           # This file
└── package.json        # Project metadata
```

## 🎯 Browser Support

- ✅ Chrome 76+
- ✅ Firefox 103+
- ✅ Safari 9+
- ✅ Edge 79+

**Note:** `backdrop-filter` requires modern browsers.

## 🔧 Key Technologies

- **Vue 3** - Progressive JavaScript framework
- **CSS Grid** - Modern 2D layout system
- **Backdrop Filter** - Glassmorphism effect
- **CSS Custom Properties** - Theme variables
- **CSS Transitions** - Smooth animations

## 💡 Pro Tips

1. **Performance:** Use `transform` instead of `position` changes for better FPS
2. **Accessibility:** Always respect `prefers-reduced-motion`
3. **Responsive:** Use `minmax()` in grid for auto-scaling cards
4. **Depth:** Layer multiple glass elements for 3D effect

## 📄 License

MIT License - Free to use in personal and commercial projects.

---

**Built with ❤️ using Vue 3 and modern CSS**
