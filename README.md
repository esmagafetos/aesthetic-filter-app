# Aesthetic Filter 🎨

Um aplicativo móvel React Native sofisticado para aplicar filtros estéticos inspirados em glitch art e visual VHS a imagens.

![Expo](https://img.shields.io/badge/Expo-54-blue)
![React Native](https://img.shields.io/badge/React%20Native-Latest-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue)

## ✨ Características

- **Interface Sofisticada**: Design moderno com gradientes, efeitos de desfoque e animações suaves
- **Filtros Estéticos**: 8 filtros inspirados no visual do jogo "Milk Inside a Bag of Milk"
  - Glitch
  - VHS
  - Chromatic Aberration
  - Noise
  - Distortion
  - Vintage
  - Neon
  - Dream
- **Controles Interativos**: Ajuste a intensidade dos filtros em tempo real com sliders
- **Feedback Háptico**: Experiência tátil sutil em todas as interações
- **Animações Fluidas**: Transições suaves usando Reanimated
- **Galeria de Edições**: Visualize suas edições recentes em grid elegante
- **Salvar na Galeria**: Exporte imagens editadas diretamente para a galeria do dispositivo

## 📥 Download

### APK para Android

- **[Releases Page](../../releases)** - Baixe a versão mais recente do APK

### Como Instalar

1. Ative "Origem desconhecida" em Configurações > Segurança
2. Baixe o arquivo `.apk`
3. Abra e toque em instalar

## 🚀 Começando

### Pré-requisitos

- Node.js 18+ instalado
- Expo Go app instalado no seu dispositivo móvel ([iOS](https://apps.apple.com/app/expo-go/id982107779) | [Android](https://play.google.com/store/apps/details?id=host.exp.exponent))

### Instalação

```bash
# Clone o repositório
git clone https://github.com/esmagafetos/aesthetic-filter-app.git
cd aesthetic-filter-app

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev
```

### Executando no Dispositivo

1. Escaneie o QR code exibido no terminal com o Expo Go
2. O app será carregado automaticamente no seu dispositivo

## 🏗️ Compilar o APK

Para compilar sua própria versão do APK, veja o [**BUILD_GUIDE.md**](BUILD_GUIDE.md) com instruções completas.

## 🏗️ Arquitetura

```
aesthetic-filter-app/
├── components/          # Componentes reutilizáveis
│   ├── Button.tsx
│   ├── FilterChip.tsx
│   ├── FilterSlider.tsx
│   ├── FloatingActionButton.tsx
│   └── ...
├── screens/            # Telas do app
│   ├── HomeScreen.tsx
│   ├── EditorScreen.tsx
│   └── SettingsScreen.tsx
├── navigation/         # Configuração de navegação
│   └── RootNavigator.tsx
├── constants/          # Temas e constantes
│   └── theme.ts
├── utils/             # Utilitários
│   ├── imageFilters.ts
│   └── storage.ts
└── hooks/             # Custom hooks
    ├── useTheme.ts
    └── useScreenInsets.ts
```

## 🎨 Design System

O app segue um design system consistente com:

- **Paleta de Cores**: Roxo profundo (#6C3FE3) e azul elétrico (#2DD4BF)
- **Tipografia**: San Francisco (iOS) / Roboto (Android)
- **Espaçamento**: Sistema modular de 4px a 48px
- **Animações**: Spring animations com damping de 15 e stiffness de 150

## 📦 Tecnologias

- **React Native** - Framework mobile
- **Expo** - Plataforma de desenvolvimento
- **TypeScript** - Type safety
- **React Navigation** - Navegação
- **Reanimated** - Animações de alta performance
- **Expo Image Picker** - Seleção de imagens
- **Expo Image Manipulator** - Processamento de imagens
- **AsyncStorage** - Armazenamento local

## 🔧 Scripts Disponíveis

```bash
npm run dev          # Inicia o servidor de desenvolvimento
npm run android      # Abre no emulador Android
npm run ios          # Abre no simulador iOS
npm run web          # Abre no navegador
```

## 🐛 Debug

### Modo de Desenvolvimento

O app está configurado com React Compiler e Hot Module Reloading ativados para desenvolvimento rápido.

### Logs

Para ver logs detalhados:

```bash
# Logs do Metro Bundler
npx expo start --verbose

# Logs do dispositivo
npx expo start --dev-client
```

### Depuração com VS Code

Crie `.vscode/launch.json`:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Expo",
      "type": "node",
      "request": "launch",
      "program": "${workspaceFolder}/node_modules/expo/AppEntry.js",
      "cwd": "${workspaceFolder}",
      "console": "integratedTerminal"
    }
  ]
}
```

## 📱 Build para Release

### Android

```bash
# Build APK
eas build --platform android --profile production

# Build AAB (Google Play)
eas build --platform android --profile production --local
```

### iOS

```bash
# Build para TestFlight
eas build --platform ios --profile production
```

## 🤝 Contribuindo

Contribuições são bem-vindas! Por favor:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🙏 Agradecimentos

- Inspirado no visual do jogo "Milk Inside a Bag of Milk"
- Design seguindo as diretrizes do iOS 26 Liquid Glass
- Construído com o poder do Expo e React Native

---

Feito com ❤️ usando React Native & Expo
