# @jy/awesome-ui

Apple-style React component library with dark mode support, built on Radix UI primitives and styled-components.

## Features

- 60+ production-ready React components
- Apple-inspired design with smooth animations
- Full dark mode support via `isDark` / `$isDark` props
- Accessible (WAI-ARIA) — powered by Radix UI
- Tree-shakeable ESM output
- TypeScript support with full type definitions

## Installation

```bash
npm install @jy/awesome-ui
```

### Peer Dependencies

```bash
npm install react react-dom styled-components lucide-react
```

## Usage

```tsx
import { Button, Input, Card } from '@jy/awesome-ui';
import '@jy/awesome-ui/styles.css'; // CSS custom properties for theming

function App() {
  return (
    <Card $isDark={false}>
      <Input type="text" placeholder="Enter your name" isDark={false} />
      <Button variant="primary" size="medium">
        Submit
      </Button>
    </Card>
  );
}
```

## Components

### Layout & Navigation
Accordion, Breadcrumb, BottomNavigation, Carousel, Collapsible, Layout, Menubar, Navbar, NavigationMenu, Pagination, Sidebar, Stepper, Tabs

### Data Display
Avatar, Badge, Banner, Card, Chart, Chip, Divider, EmptyState, Progress, Separator, Skeleton, StatCard, StatusIndicator, Table, Timeline, Toast

### Form & Input
Button, Calendar, Checkbox, Command, DateTimePicker, Form, Input, InputOTP, Label, RadioGroup, Select, Slider, Switch, Textarea, Toggle, ToggleGroup

### Overlay & Feedback
AlertDialog, Alert, ContextMenu, Dialog, Drawer, DropdownMenu, HoverCard, Loading, Popover, ScrollArea, Sheet, Sonner, Tooltip

## Theming

Import the CSS file to apply theme variables:

```tsx
import '@jy/awesome-ui/styles.css';
```

This provides CSS custom properties for `:root` and `.dark` that control colors, spacing, and more.

## License

MIT
