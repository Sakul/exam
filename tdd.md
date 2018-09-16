# Test Driven Development

## สร้างโปรเจค xunit
```
dotnet new xunit -n demoxunit
```
> **demoxunit** คือชื่อโปรเจคและจะได้ folder ชื่อนั้นด้วย *(ไม่เปลี่ยนก็แล้วแต่ - เตือนแล้วนะ)*

## Reference project
```
dotnet add YOUR_XUNIT_PROJECT_PATH.csproj reference YOUR_SUSPECTED_PROJECT_PATH.csproj
```

## Commands
```
dotnet build
dotnet test
```
> ต้องอยู่ใน folder xunit project แล้ว  

## Packages
```
dotnet add package moq
dotnet add package fluentassertions
```
> ต้องอยู่ใน folder xunit project แล้ว  


## [Sample code](https://xunit.github.io/docs/getting-started-dotnet-core)
**Fact**
```
[Fact]
public void PassingTest()
{
    Assert.Equal(4, Add(2, 2));
}

public void Add(int a, int b) => a + b;
```
**Theory**
```
[Theory]
[InlineData(2, 2, 4)]
[InlineData(3, 2, 5)]
public void PassingTest(int input1, int input2, int expectedResult)
{
    Assert.Equal(expectedResult, Add(input1, input2));
}

public int Add(int x, int y) => x + y;
```
