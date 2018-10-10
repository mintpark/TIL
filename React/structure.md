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

component key
react의 모든 component는 key를 필요로 하는데, 그 이유는 key로 렌더 여부를 판단하기 때문이다. 보통 component를 생성하면 key는 자동으로 생성되지만, array에 element를 추가하는 경우에는 개발자가 key를 명시적으로 추가해야 한다. 이 때, idx를 key로 삼는 것은 지양해야 하는데, array를 갱신할 때 key가 꼬일 수 있기 때문이다.
