# 💫 About Me
I am a passionate **Flutter Developer** with strong experience in building modern, high-quality mobile applications. 🚀  
I specialize in creating clean, responsive, and visually appealing UI with a focus on user experience. 🎨📱  
I write scalable, maintainable code and follow best practices in state management and app architecture. 🧩  
I have hands-on experience with REST APIs, Firebase, and local storage solutions. 🔗🔥  
I enjoy solving complex problems and turning ideas into reliable mobile solutions. 💡➡️📲  
I confidently work with **Bloc, Cubit, Provider, GetX, Riverpod**, and shared preferences. ⚙️📦  
I stay updated with the latest Flutter technologies and continuously develop my skills. 📚✨  
I collaborate effectively with teams and communicate clearly to deliver high-quality results. 🤝💬  
I approach every project with professionalism, attention to detail, and a drive for excellence. 🎯  
My goal is to build fast, stable, and user-focused apps that create real value. ⭐📈

---

## 🌐 Contact
- **WhatsApp:** [01126050489](https://wa.me/201126050489)  
- **Email:** [mostafaahmed612001@gmail.com](mailto:mostafaahmed612001@gmail.com)  
- **LinkedIn:** https://www.linkedin.com/in/mostafa-ahmed-2a71ab281  
- **GitHub:** https://github.com/mostafacoding2

---

# 💻 Tech Stack & Skills

### Languages
- Dart, C++ (core knowledge), SQL

### Flutter / Frameworks
- Flutter (mobile, web, desktop)
- Widgets, CustomPaint, Responsive Layouts
- Material & Cupertino design systems
- Adaptive & accessible design

### State Management
- Bloc / Cubit, Provider, GetX, Riverpod, MobX

### Networking & APIs
- `dio`, `http`, WebSockets, REST, GraphQL

### Backend & Databases
- Firebase (Auth, Firestore, Realtime DB, Cloud Functions, Cloud Messaging)
- Supabase, RESTful APIs, Node.js / Express (integration)
- Local storage: Hive, SharedPreferences, sembast, SQLite (sqflite)

### Payments & Monetization
- **Stripe** (checkout, payment-intents, Apple/Google Pay integration)
- **PayPal** (webview / REST integrations)
- **Razorpay** (popular in some regions)
- **In-App Purchases** (iOS / Android via `in_app_purchase`)
- **Google Pay** & **Apple Pay** (via platform-specific configs + packages)
- Subscriptions, one-time payments, promo codes & coupon flows

### DevOps / CI-CD / Testing
- CI/CD: GitHub Actions, Bitrise, Codemagic
- Unit tests, Widget tests, Integration tests (flutter_test, integration_test)
- Linting, formatting, and code coverage

### Tools & Design
- Figma, Adobe XD, Canva, Sketch
- Git, GitHub, GitLab
- Analytics: Firebase Analytics, Sentry (error tracking)

### UX / Advanced Topics
- Animations (Implicit & Explicit animations, Rive, Lottie)
- Custom transitions, hero animations
- Accessibility, RTL (Arabic language support), localization (i18n)
- Performance tuning, memory/profile debugging

---

# 🔌 Flutter Packages I Use Often
- `flutter_bloc`, `bloc`, `provider`, `get`, `hooks_riverpod`
- `dio`, `retrofit`, `http`, `graphql_flutter`
- `firebase_core`, `firebase_auth`, `cloud_firestore`, `firebase_messaging`
- `hive`, `sqflite`, `shared_preferences`
- `in_app_purchase`, `stripe_sdk` / `flutter_stripe`, `pay`, `razorpay_flutter`
- `cached_network_image`, `flutter_local_notifications`
- `flutter_secure_storage`, `encrypt`
- `equatable`, `freezed`, `json_serializable`
- `flutter_localizations`

---

# 💳 Payment Integrations — Short Examples & Notes

> **Note:** Real payment integration requires proper server-side handling (secret keys), secure storage, and PCI compliance. Below are short illustrative snippets and common approaches.

### Stripe (recommended approach)
1. Create PaymentIntent on your **server** (using Stripe secret key).
2. Return client secret to the app.
3. Use `flutter_stripe` (or suitable SDK) to confirm payment.

**Example (simplified):**
```dart
// Pseudocode - do NOT store secret keys in app
final clientSecret = await myServer.createPaymentIntent(amount, currency);
await Stripe.instance.initPaymentSheet(paymentSheetParameters: {
  'paymentIntentClientSecret': clientSecret,
  // other config
});
await Stripe.instance.presentPaymentSheet();

