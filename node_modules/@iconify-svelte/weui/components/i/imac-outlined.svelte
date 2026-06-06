<script>
import Icon from '@iconify/css-svelte';
import '../../css/n/nhz01_o5b.css';
import '../../css/d/d2kvgvbvc.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<defs><path id="SVG8KAPOcZt" class="nhz01_o5b"/></defs><use href="#SVG8KAPOcZt" transform="translate(2 4)" class="d2kvgvbvc"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:imac-outlined" {...props}></Icon>
