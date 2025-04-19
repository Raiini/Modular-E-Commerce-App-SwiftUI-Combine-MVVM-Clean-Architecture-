# 🛍️ Modular E-Commerce App

A fully modular, production-ready **SwiftUI-based E-Commerce application** built with **MVVM + Clean Architecture**, CI/CD automation, REST API integration, and offline caching. Designed to demonstrate real-world iOS development patterns for senior-level engineers.

---

## 🔧 Tech Stack

| Layer            | Tech/Tool                        |
|------------------|----------------------------------|
| UI               | SwiftUI                          |
| State Management | Combine                          |
| Architecture     | MVVM + Clean Architecture        |
| API Integration  | REST API                         |
| Offline Caching  | Realm (or CoreData)              |
| Auth             | Sign In with Apple               |
| Testing          | XCTest, XCUITest                 |
| CI/CD            | Fastlane + GitHub Actions        |
| Package Manager  | Swift Package Manager (SPM)      |

---

## 📱 Features

- 🛒 Product List with dynamic categories
- 🧺 Add to Cart and Wishlist functionality
- 🔍 Search, filter, and sort products
- 📦 Product Details with image zoom
- 💳 Checkout Flow (In-App Purchase ready)
- 🕵️ Secure Authentication (Sign In with Apple)
- 🌐 API-driven with offline caching
- 🧪 Unit and UI Test coverage
- 🚀 CI/CD: GitHub Actions + Fastlane for TestFlight

---

## 🧱 Project Structure

```
ModularECommerceApp/
├── App/                     # App entry point
├── Presentation/            # SwiftUI Views and ViewModels
│   └── ProductList/
├── Domain/                  # Business models
│   └── Models/
├── Data/                    # API and data layer
│   └── Services/
├── Resources/               # Assets and localization
├── Tests/                   # Unit and UI tests
├── Fastlane/                # CI/CD lanes
├── .github/workflows/       # GitHub Actions workflow
```

---

## 📷 Screenshots

> *(Add actual screenshots or GIF previews here)*

---

## 🧪 Testing

- Unit Tests with `XCTest`
- UI Tests using `XCUITest`
- GitHub Actions workflow runs tests on PRs

Run locally:
```bash
⌘ + U (or) xcodebuild test -scheme ModularECommerceApp
```

---

## 🚀 CI/CD Setup

✅ Integrated with **GitHub Actions** for:
- Unit tests on PRs and pushes
- Build validation

✅ Integrated with **Fastlane** for:
- Building and distributing to TestFlight
- Slack or email notifications (optional)

### GitHub Actions Workflow: `.github/workflows/ios-ci.yml`
```yaml
name: iOS CI
on:
  push:
    branches: [ main ]
jobs:
  build:
    runs-on: macos-latest
    steps:
      - uses: actions/checkout@v3
      - name: Build App
        run: xcodebuild build -scheme ModularECommerceApp
      - name: Run Tests
        run: xcodebuild test -scheme ModularECommerceApp
```

### Fastlane Lane (Fastfile)
```ruby
lane :beta do
  build_app(scheme: "ModularECommerceApp")
  upload_to_testflight
end
```

---

## 🔐 Authentication

Supports Sign In with Apple using `ASAuthorizationController`.

---

## 🛠 Installation

```bash
git clone https://github.com/your-username/modular-ecommerce-app.git
cd modular-ecommerce-app
open ModularECommerceApp.xcodeproj
```

---

## 📦 API Setup

> Use any mock API service like [FakeStoreAPI](https://fakestoreapi.com) or configure your own backend.

To integrate:
1. Replace endpoint in `ProductService.swift`
2. Use `URLSession` or a networking library

---

## 📝 Localization

Supports English by default. You can extend `Localizable.strings` for multi-language support.

---

## 📄 License

This project is licensed under the **MIT License** – see the [LICENSE](./LICENSE) file for details.

---

## 🙌 Contribution

Pull requests are welcome! Please open issues for bugs or features.

---

