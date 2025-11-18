---
name: mobile-gamedev-ecosystem
description: Master mobile development with Swift, Kotlin, and cross-platform frameworks, plus game development with Unity. Use when building iOS/Android apps, creating games, or implementing platform-specific features.
---

# Mobile & Game Development Ecosystem Skill

## Quick Start

Build high-performance mobile applications and engaging games across iOS, Android, and game platforms.

### Essential Mobile Stack

```swift
// Swift with SwiftUI example
import SwiftUI

struct ContentView: View {
    @State private var todos: [String] = []
    @State private var newTodo = ""

    var body: some View {
        VStack {
            HStack {
                TextField("Add a todo", text: $newTodo)
                Button("Add") {
                    if !newTodo.isEmpty {
                        todos.append(newTodo)
                        newTodo = ""
                    }
                }
            }
            .padding()

            List {
                ForEach(todos, id: \.self) { todo in
                    Text(todo)
                        .swipeActions(edge: .trailing) {
                            Button(role: .destructive) {
                                todos.removeAll { $0 == todo }
                            } label: {
                                Label("Delete", systemImage: "trash")
                            }
                        }
                }
            }
        }
    }
}

#Preview {
    ContentView()
}
```

```kotlin
// Kotlin with Jetpack Compose example
import androidx.compose.foundation.layout.*
import androidx.compose.material3.*
import androidx.compose.runtime.*
import androidx.lifecycle.viewmodel.compose.viewModel

@Composable
fun TodoScreen() {
    var todos by remember { mutableStateOf(listOf<String>()) }
    var newTodo by remember { mutableStateOf("") }

    Column(
        modifier = Modifier
            .fillMaxSize()
            .padding(16.dp)
    ) {
        Row(
            modifier = Modifier
                .fillMaxWidth()
                .padding(bottom = 16.dp),
            horizontalArrangement = Arrangement.spacedBy(8.dp)
        ) {
            TextField(
                value = newTodo,
                onValueChange = { newTodo = it },
                modifier = Modifier.weight(1f),
                placeholder = { Text("Add a todo") }
            )
            Button(onClick = {
                if (newTodo.isNotBlank()) {
                    todos = todos + newTodo
                    newTodo = ""
                }
            }) {
                Text("Add")
            }
        }

        LazyColumn {
            items(todos) { todo ->
                Text(
                    text = todo,
                    modifier = Modifier
                        .fillMaxWidth()
                        .padding(8.dp)
                )
            }
        }
    }
}
```

## Learning Domains

### 📱 **iOS Development**

**Swift Language**
- Variables and constants (let, var)
- Optionals and unwrapping
- Functions and closures
- Protocols and extensions
- Memory management (ARC)
- Error handling (try-catch, Result)

**SwiftUI**
- Declarative UI framework
- State management (@State, @StateObject, @EnvironmentObject)
- View composition and containers
- Navigation (NavigationStack, NavigationLink)
- Animations and transitions
- Form handling

**UIKit (Legacy)**
- View controllers
- Auto layout and constraints
- Table views and collection views
- Navigation controller and tab bar
- Delegate and data source patterns

**Core Frameworks**
- Core Data (persistence)
- CloudKit (cloud sync)
- Core Location (GPS)
- HealthKit (health data)
- Combine (reactive programming)
- AVFoundation (media)

**Networking**
- URLSession for HTTP
- Codable for JSON parsing
- REST API integration
- WebSocket connections
- Upload/download tasks

**Testing & Debugging**
- XCTest framework
- UI testing
- Instruments for profiling
- Debugging with Xcode
- Performance optimization

### 🤖 **Android Development**

**Kotlin Language**
- Variables and type inference
- Null safety with Optional
- Extension functions
- Coroutines for async
- Flow for reactive streams
- Data classes and sealed classes

**Jetpack Compose**
- Composable functions
- State and state hoisting
- Layouts (Column, Row, Box)
- Lists (LazyColumn, LazyRow)
- Navigation with NavController
- Modifier system for styling
- Theme and Material Design

**Android Framework**
- Activities and Fragments
- Intent and navigation
- Services for background work
- Content providers for data sharing
- Broadcast receivers

**Architecture**
- Model-View-ViewModel (MVVM)
- Repository pattern
- Dependency injection (Hilt)
- Data binding
- LiveData and ViewModel

**Networking**
- Retrofit for HTTP
- OkHttp client
- REST API integration
- JSON parsing (Gson, Kotlinx.serialization)

**Storage**
- Room Database (SQLite ORM)
- SharedPreferences
- DataStore for encrypted preferences
- File operations

**Testing**
- JUnit for unit testing
- Mockito for mocking
- Espresso for UI testing
- Robolectric for local testing

### 🔄 **Cross-Platform Development**

**React Native**
- JavaScript/TypeScript
- Component-based architecture
- Navigation patterns
- State management (Redux, Context)
- Native modules for platform features
- Performance optimization

**Flutter**
- Dart language fundamentals
- Widget system and composition
- State management (Provider, Riverpod, Bloc)
- Navigation and routing
- Platform channels for native code
- Testing (unit, widget, integration)

### 🎮 **Game Development**

**Game Engines**
- **Unity** - C# scripting, physics, 2D/3D
- **Unreal Engine** - C++, Blueprints, advanced graphics
- **Godot** - GDScript, lightweight, open-source

**Game Design Fundamentals**
- Game mechanics and game loops
- Level design and progression
- User experience in games
- Playtesting and iteration

**Graphics & Animation**
- Sprite management (2D)
- 3D modeling and importing
- Shader programming (GLSL)
- Particle systems
- Animation state machines
- Skeletal animation

**Physics & Collision**
- 2D and 3D physics engines
- Rigidbodies and colliders
- Constraint systems
- Raycast and collision detection

**Audio Systems**
- Sound effects and background music
- Spatial audio
- Audio mixing
- Voice chat integration

**Input & Controls**
- Touch and gesture input
- Gamepad support
- Mobile input handling
- VR/AR controllers

**Networking & Multiplayer**
- Real-time multiplayer (Photon, Netcode)
- Turn-based multiplayer
- Matchmaking and lobbies
- Synchronization and state management

**Game Monetization**
- In-app purchases
- Ad integration
- Subscription models
- Battle pass systems

### 🎨 **Mobile UI/UX**

**User Interface Design**
- Platform design guidelines (iOS HIG, Material Design)
- Navigation patterns
- Responsive layouts
- Accessibility (VoiceOver, TalkBack)
- Dark mode support

**User Experience**
- Gesture design
- Animation and motion
- Performance and responsiveness
- Accessibility standards (WCAG)

### 🚀 **Advanced Features**

**Augmented Reality**
- ARKit (iOS)
- ARCore (Android)
- Real-world object detection
- AR UI overlays

**Machine Learning**
- Core ML (iOS)
- TensorFlow Lite (Android)
- On-device inference
- Model deployment

**Push Notifications**
- Local notifications
- Remote push notifications
- Deep linking
- Rich media notifications

**Security**
- Keychain/Keystore
- Data encryption
- Secure storage
- SSL pinning
- Biometric authentication

## Skill Development Checklist

- [ ] Build complete iOS app with SwiftUI
- [ ] Build complete Android app with Compose
- [ ] Implement API integration with error handling
- [ ] Create local database with persistence
- [ ] Build cross-platform app with React Native or Flutter
- [ ] Implement push notifications
- [ ] Optimize app performance
- [ ] Create simple 2D game with Unity
- [ ] Publish app to App Store and Play Store

## Real-World Scenarios

**E-Commerce Mobile App**
- Product browsing and search
- Shopping cart management
- Payment integration
- Order tracking
- Push notifications for deals
- Multi-platform (iOS & Android)

**Social Media App**
- User authentication
- Photo upload and sharing
- Real-time chat
- Follow/like features
- Push notifications

**Mobile Game**
- Gameplay mechanics
- Scoring system
- Multiple levels
- Sound and graphics
- In-app purchases
- Leaderboards

## Practice Projects

1. **Todo Application**
   - CRUD operations
   - Local persistence
   - UI with platform conventions

2. **Weather App**
   - API integration
   - Location services
   - Graphical representation
   - Geolocation

3. **Fitness Tracker**
   - Health data integration
   - Background tracking
   - Analytics and charts

4. **Simple Game**
   - Game mechanics
   - Scoring system
   - Mobile controls
   - Save/load functionality

## Resources

- **7+ Mobile & Game Development Roadmaps**
- **85+ Content Modules** - iOS, Android, Cross-platform, Game Dev
- **Platform-Specific Guides** - Swift, Kotlin, Jetpack Compose
- **Game Development** - Unity, Unreal, Godot resources
- **UI/UX Patterns** - Mobile design systems
- **Monetization & Publishing** - App stores, IAP, ads

## Assessment Criteria

You've mastered this skill when you can:

✓ Build fully functional iOS apps with SwiftUI
✓ Build fully functional Android apps with Compose
✓ Implement network requests and data persistence
✓ Create responsive, accessible mobile UIs
✓ Optimize app performance and battery usage
✓ Deploy to App Store and Play Store
✓ Create cross-platform apps
✓ Build engaging games with game engines
✓ Implement monetization and analytics
