<style src="./annotationLayer.css"></style>
<script>
	import componentFactory from './componentFactory.js'

	const pdfjsWrapper = require('./pdfjsWrapper.js').default;
	// const PDFJS = require('pdfjs-dist/build/pdf.min.js');
	const PDFJS = require('pdfjs-dist/es5/build/pdf.min.js');

	if (typeof window !== 'undefined' && 'Worker' in window && navigator.appVersion.indexOf('MSIE 10') === -1) {
		PDFJS.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.5.207/pdf.worker.min.js';
	}

	var component = componentFactory(pdfjsWrapper(PDFJS));

	export default component;
</script>
