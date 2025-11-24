# 📦 Guia Completo de Build - Aesthetic Filter

Este documento fornece instruções detalhadas para compilar e distribuir o app Aesthetic Filter.

## 🚀 Opções de Build

### 1. Desenvolvimento Local (Recomendado para Testes)

```bash
npm run dev
```

O app será executado no Expo Go via QR code, sem necessidade de build.

### 2. APK para Android

#### Opção A: Build via EAS (Recomendado)

```bash
# Executar o script de build interativo
chmod +x build-release.sh
./build-release.sh
```

Ou manualmente:

```bash
# Instalar EAS CLI globalmente
npm install -g eas-cli

# Fazer login na sua conta Expo
eas login

# Build para produção
eas build --platform android --profile production

# Build para preview (APK interno)
eas build --platform android --profile preview
```

**Vantagens:**
- Build gerenciado pela Expo
- Builds criptografados
- Histórico de versões
- Updates OTA (Over-The-Air)

#### Opção B: Build Local (Requer Android SDK)

Para compilar localmente, você precisa do Android SDK instalado:

```bash
# Instalar ferramentas Expo
npm install -g expo-cli

# Gerar o APK localmente (requer Android SDK)
eas build --platform android --local
```

### 3. IPA para iOS

```bash
# Build para App Store
eas build --platform ios --profile production

# Build para TestFlight
eas build --platform ios --profile preview
```

## 📋 Pré-requisitos

### Para builds via EAS (Recomendado)

1. **Conta Expo** - Crie em [expo.dev](https://expo.dev)
2. **EAS CLI** - `npm install -g eas-cli`
3. **Credenciais** - Autentique com `eas login`

### Para builds locais

1. **Android Studio** - Download em [developer.android.com](https://developer.android.com/studio)
2. **Android SDK** - API level 31+
3. **Java Development Kit** - JDK 11+

## 📱 Versões Suportadas

- **Android**: API 31+ (Android 12+)
- **iOS**: iOS 13.4+

## 🔧 Configuração de Build

Os perfis de build estão definidos em `eas.json`:

- **development** - Para testes locais com Development Client
- **preview** - Para distribuição interna (APK)
- **production** - Para publicação em stores (AAB para Android, IPA para iOS)

## 📥 Distribuição

### Play Store (Android)

```bash
# Fazer build AAB para Play Store
eas build --platform android --profile production

# Enviar para Play Store
eas submit --platform android
```

### App Store (iOS)

```bash
# Fazer build para App Store
eas build --platform ios --profile production

# Enviar para App Store
eas submit --platform ios
```

### Distribuição Direta (APK)

O APK pode ser distribuído diretamente através de:

1. **GitHub Releases** - Anexar o APK ao release
2. **Direct Link** - Hospedar em servidor e compartilhar link
3. **Stores Alternativos** - F-Droid, APKMirror, etc.

## ✅ Checklist Pre-Release

- [ ] Versão atualizada em `app.json`
- [ ] CHANGELOG.md atualizado
- [ ] Testes em dispositivo físico
- [ ] Screenshots capturadas
- [ ] Descrição/Changelog preparados
- [ ] Privacy Policy (se necessário)
- [ ] Credentials e certificados válidos

## 🐛 Troubleshooting

### Erro: "Build não iniciou"

```bash
# Limpar cache e tentar novamente
rm -rf node_modules package-lock.json
npm install
eas build --platform android --profile production --clear-cache
```

### Erro: "Credenciais inválidas"

```bash
# Fazer logout e login novamente
eas logout
eas login
```

### Build leva muito tempo

- Normal para primeiro build (10-20 minutos)
- Builds subsequentes são mais rápidos
- Verifique sua conexão de internet

## 📚 Recursos Úteis

- [Expo Build Documentation](https://docs.expo.dev/build/introduction/)
- [Expo Submit Documentation](https://docs.expo.dev/submit/introduction/)
- [EAS CLI Reference](https://docs.expo.dev/eas-cli/introduction/)
- [Android App Publishing](https://developer.android.com/studio/publish)
- [iOS App Publishing](https://developer.apple.com/app-store/submissions/)

## 🤝 Suporte

Para problemas com build ou distribuição:

1. Verifique a documentação oficial da Expo
2. Consulte o [Expo Forum](https://forums.expo.dev)
3. Abra uma issue neste repositório

---

**Última atualização**: Novembro 2024
**Versão do App**: 1.0.0
**Suporte Expo**: SDK 54+
