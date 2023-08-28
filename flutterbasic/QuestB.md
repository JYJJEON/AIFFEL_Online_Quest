
### 1. Flutter란 무엇인가요?
**답**: Flutter는 Google에서 개발한 오픈 소스 UI 소프트웨어 개발 키트입니다. 이 키트를 사용하면, 하나의 코드베이스로 Android, iOS, Web, Desktop 등 다양한 플랫폼에 대한 앱을 개발할 수 있습니다. Flutter는 선언적 UI 구조를 가지며, Dart라는 언어를 사용합니다.

### 2. Flutter의 장점은 무엇인가요?
**답**: 
- **코드 재사용성**: 하나의 코드베이스로 여러 플랫폼을 지원하므로 개발 시간과 비용을 절약할 수 있습니다.
- **빠른 개발 사이클**: Hot Reload 기능을 통해 코드 변경을 바로 볼 수 있어 빠르게 개발할 수 있습니다.
- **위젯 기반 아키텍처**: 다양한 미리 만들어진 위젯과 높은 커스터마이징 가능성을 제공합니다.
- **뛰어난 성능**: Dart를 사용하고, 네이티브 코드로 컴파일되므로 네이티브 앱에 가까운 성능을 보입니다.

### 3. Dart 언어와의 관계는?
**답**: Flutter는 Dart 언어를 사용하여 개발됩니다. Dart는 객체지향 프로그래밍 언어로, Flutter의 성능을 최적화하고, 풍부한 표준 라이브러리와 함께 제공됩니다. Dart의 강력한 기능과 라이브러리는 Flutter의 다양한 UI와 상태 관리를 지원합니다.

### 4. StatefulWidget과 StatelessWidget의 차이는?
**답**: 
- **StatefulWidget**: 이 위젯은 변할 수 있는 상태를 가집니다. `setState()` 메서드를 통해 상태를 변경하고, UI를 다시 빌드할 수 있습니다.
- **StatelessWidget**: 이 위젯은 일단 그려지면 그 상태가 변경되지 않습니다. 상태가 필요 없는 경우에 주로 사용됩니다.

### 5. pubspec.yaml 파일의 역할은?
**답**: `pubspec.yaml` 파일은 Flutter 프로젝트의 메타데이터와 의존성을 정의합니다. 여기에서 프로젝트 이름, 설명, 버전 정보, 의존하는 패키지 등을 지정할 수 있습니다.

### 6. Navigator란 무엇이며 어떻게 작동하는가?

**답**: Navigator는 Flutter 앱에서 페이지 라우팅을 관리하는 객체입니다. Navigator는 일종의 스택 관리자로, 여러 `Route` 객체를 스택으로 관리합니다. `Navigator.push()` 메서드를 사용하여 새로운 페이지를 스택에 추가하거나 `Navigator.pop()` 메서드를 사용하여 현재 페이지를 스택에서 제거할 수 있습니다.

---

### 7. Route란 무엇인가요?

**답**: Route는 Flutter 앱 내에서 화면 간의 이동 경로를 나타내는 개념입니다. Route는 앱의 한 페이지 또는 화면을 표현하며, Navigator는 이러한 Route들을 관리합니다. 

---

### 8. MaterialPageRoute와 CupertinoPageRoute는 어떻게 다른가요?

**답**: `MaterialPageRoute`와 `CupertinoPageRoute`는 각각 Android와 iOS 스타일의 페이지 전환 애니메이션을 제공합니다. `MaterialPageRoute`는 Material Design에 기반한 애니메이션을, `CupertinoPageRoute`는 iOS 스타일의 애니메이션을 제공합니다.

---

