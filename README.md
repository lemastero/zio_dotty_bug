```scala
[error] -- [E007] Type Mismatch Error: /Users/piter/learn/zio/broken_console/src/test/scala/com/example/BrokenSpec.scala:15:33 
[error] 15 |      val out = app.provideLayer(env)
[error]    |                                 ^^^
[error]    |Found:    (env : zio.test.mock.Expectation[zio.console.Console])
[error]    |Required: zio.ZLayer[Any, Nothing, zio.Has[zio.console.package.Console.Service]]
[error]    |Constraint(
[error]    | uninstVars = R, E, R, E;
[error]    | constrained types = 
[error]    |  [R, E, T]
[error]    |    (label: String)(specs: zio.test.Spec[R, E, T]*): zio.test.Spec[R, E, T]
[error]    |, 
[error]    |  [R, E]
[error]    |    (label: String)
[error]    |      (assertion: => zio.ZIO[R, E, zio.test.package.TestResult]): 
[error]    |        zio.test.package.ZSpec[R, E]
[error]    |, 
[error]    |  [E1, R0, R1]
[error]    |    (layer: zio.ZLayer[R0, E1, R1])
[error]    |      (implicit ev1: R1 <:< zio.console.package.Console, ev2: 
[error]    |        zio.NeedsEnv[zio.console.package.Console]
[error]    |      ): zio.ZIO[R0, E1, Unit]
[error]    | bounds = 
[error]    |     R
[error]    |     >: zio.ZEnv & zio.test.Annotations & zio.test.environment.TestClock & 
[error]    |      zio.test.environment.TestConsole
[error]    |     & zio.test.environment.Live & zio.test.environment.TestRandom & 
[error]    |      zio.test.Sized
[error]    |     & zio.test.environment.TestSystem
[error]    |     E
[error]    |     >: zio.test.TestFailure[E] <: 
[error]    |      zio.test.TestFailure[com.example.BrokenSpec.Failure]
[error]    |     T := zio.test.TestSuccess
[error]    |     R
[error]    |     >: zio.ZEnv & zio.test.Annotations & zio.test.environment.TestClock & 
[error]    |      zio.test.environment.TestConsole
[error]    |     & zio.test.environment.Live & zio.test.environment.TestRandom & 
[error]    |      zio.test.Sized
[error]    |     & zio.test.environment.TestSystem
[error]    |     E
[error]    |     E1
[error]    |     R0
[error]    |     R1
[error]    | ordering = 
[error]    |     R <: R
[error]    |)
[error]    |Subtype trace:
[error]    |  ==> (env : zio.test.mock.Expectation[zio.console.Console]) <:< zio.ZLayer[Any, Nothing, zio.Has[zio.console.package.Console.Service]]  
[error]    |    ==> (env : zio.test.mock.Expectation[zio.console.Console]) <:< zio.ZLayer[Any, Nothing, zio.Has[zio.console.package.Console.Service]] recur 
[error]    |    <== (env : zio.test.mock.Expectation[zio.console.Console]) <:< zio.ZLayer[Any, Nothing, zio.Has[zio.console.package.Console.Service]] recur  = false
[error]    |  <== (env : zio.test.mock.Expectation[zio.console.Console]) <:< zio.ZLayer[Any, Nothing, zio.Has[zio.console.package.Console.Service]]   = false
[error] one error found
```
