foobar2
=======

foobar

http://css-tricks.com/examples/WebKitScrollbars/
https://wrapbootstrap.com/


angular.element('html').scope() (then child head and controller)
angular.element('html').scope().$$childHead.controller.delegateController._showGlossary = true

force digest

angular.element('html').scope().$apply()

function given(desc, givenFn) {
	var whenMonad = Object.create(null);
	whenMonad.when = function when(desc, whenFn) {
		var thenMonad = Object.create(null);
		thenMonad.when = function then(desc, thenFn) {
			run(givenFn);
			run(whenFn);
			run(thenFn);
		};
	};

	function run(given, when, then) {
		given();
		when();
		then();
	}
}
