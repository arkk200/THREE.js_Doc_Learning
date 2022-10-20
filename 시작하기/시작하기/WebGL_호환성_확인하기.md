# WebGL 호환성 확인하기
이 문제는 점점 줄어들곤 있지만, 여전히 몇몇의 디바이스나 브라우저는 WebGL을 지원하지 않습니다.<br>
다음 코드는 WebGL이 지원하는지 확인할 수 있는 코드이고 만약 지원하지 않는다면 메세지를 보여줍니다.<br><br>
렌더링하기 전에 다음 코드 [https://github.com/mrdoob/three.js/blob/master/examples/jsm/capabilities/WebGL.js](https://github.com/mrdoob/three.js/blob/master/examples/jsm/capabilities/WebGL.js) 를 자바스크립트 파일에서 실행해줍니다.
```js
if ( WebGL.isWebGLAvailable() ) {

	// Initiate function or other initializations here
	animate();

} else {

	const warning = WebGL.getWebGLErrorMessage();
	document.getElementById( 'container' ).appendChild( warning );

}
```