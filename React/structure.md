# Structure
### reactJS와 redux를 함께 사용할 때의 프로세스

compose & mapStateToProps
변경된 상태를 store에 전달하려고!
mapStateToProps() 내부에 상태변경 로직. compose에 masStateToProps()를 전달하면 된다.
mapDispatchToProps로 액션을 전달할 수도 있음.

reselect
컴포넌트 중 변경된 부분만 렌더해주려고!
selector와 reselector의 코드적 차이는 createSelector() 거치는 것 밖에 없는 것 같다.
createSelector 이 한 줄을 써주는 것만으로 변경사항만 렌더할 수 있다니.

context
보통 앱 최상단에 Provider를 선언하면 하위 Container들은 다 store를 구독하는 것 같다.
