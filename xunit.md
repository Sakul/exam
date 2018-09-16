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
dotnet add package Newtonsoft.Json
dotnet add package fluentassertions
```
> ต้องอยู่ใน folder xunit project แล้ว  

---
# [Xunit](https://xunit.github.io/docs/getting-started-dotnet-core)
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
---
# [Fluentassertions](https://fluentassertions.com/examples)
**Example 1**
```
string actual = "ABCDEFGHI";
actual.Should().StartWith("AB").And.EndWith("HI").And.Contain("EF").And.HaveLength(9);
```
**Example 2**
```
IEnumerable numbers = new[] { 1, 2, 3 };
numbers.Should().HaveCount(4, "because we thought we put four items in the collection"))
```
---
# [Moq](https://github.com/Moq/moq4/wiki/Quickstart)
```
public interface ISomething
{
    void DoSomething();
    int GetSomething();
    int GetSomethingById(int id);
}
```
```
using Moq;
```
```
var moq = new MockRepository(MockBehavior.Default);
var somethingMock = moq.Create<ISomething>();

// Setup
somethingMock.Setup(it => it.GetSomething()).Returns(99);
somethingMock.Setup(it => it.GetSomethingById(It.IsAny<int>())).Returns<int>(it => 88);

ISomething obj = somethingMock.Object;
var result = obj.GetSomethingById(7); // result: 88

// Verify
somethingMock.Verify(it => it.DoSomething(), Times.Never(), "Error msg 1");
somethingMock.Verify(it => it.GetSomethingById(It.Is<int>(actual => actual == 7)), Times.Once(), "Error msg 2");
```
