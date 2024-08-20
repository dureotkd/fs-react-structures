# Grouping by Features/Modules

더 큰 프로젝트의 경우 Domain Separation 구조는 각 모듈 내에서 애플리케이션의 다양한 측면에 대한 명확한

경계를 정의하는 매우 모듈화된 접근 방식을 제공합니다.

## Module 구성요소

- apis : 서버와 통신하는 로직을 위한 것입니다

- components : 공유 컴포넌트를 위한 것입니다

- helpers : 매우 간단한 1~3줄 짜리 논리를 위한것입니다 예를 들어

```typescript
export const isAdmin = (user: User) => user.role === UserRole.ADMIN;
```

- hooks : 공유 로직을 위한 사용자 정의 React Hooks

- pages : 해당 폴더의 page정의를 위한 것입니다

- services : 폴더 는 주로 더 복잡한 로직을 포함하고 있으며, /helpers 폴더의 로직을 사용할 가능성이 높습니다. FE 측에서 직원 검색 기능을 구현하고 싶다고 가정해 보겠습니다. 필드가 많을 수 있으며, 필드는 서로 다른 매칭 로직을 가질 수 있으며, 일부 퍼지 검색도 필요할 수 있습니다. 이는 이미 복잡한 로직으로 간주될 수 있으며, /services에 있어야 합니다

- states : 글로벌 상태 관리 로직 (Jotai,Zustand,Redux등)

- types : 타입 정의를 위한 것입니다

## Learn More

You can learn more in the [documentation](https://dev.to/itswillt/folder-structures-in-react-projects-3dp8)
