# 配置项

```ts
interface RepeatState {
  content: string
  repeated: boolean
  times: number
  users: Record<number, number>
}

type StateCallback = (state: RepeatState, session: Session) => void | string

interface RepeatHandler {
  minTimes: number
  probability?: number
}

interface RepeaterOptions {
  onRepeat?: RepeatHandler | StateCallback
  onInterrupt?: StateCallback
}
```
