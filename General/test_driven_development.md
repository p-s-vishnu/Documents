# Test driven development 

- Naming convention :Unlike coding conventions, the test class is usually the elaborated name of Test case.
- Test driven development cycle (Red - Green refactor)
  1. Write test
  2. Test fails, gives confidence test works
  3. Write code
  4. Test pases 
  5. Refactor
- Why TDD ?
  1. First of all, TDD is a proactive apporoach. In reactive test, the tests are delayed 
  2. TDD focussed on early testing
    1. Requirement phase
    2. Established a rapid feedback system, changes incrementally
    3. Easy to pick-up from where you left compared to large complicated file
  3. *Enables collaboration* : Can avoid blockers, instead of depending on large code change small incremental tested component can be easily accomodated.
  4. *Value refactoring* : refactoring often to lower impact and risk. If collaborators tend to use the change early refactor will lead to less impact.
  5. *Design to test* : forces to have good design. Clean design -> low level of coupling between modules
  6. Test will serve as documentation, decisions made and conditions assumed.
