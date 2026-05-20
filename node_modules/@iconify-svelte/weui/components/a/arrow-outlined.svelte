<script>
import Icon from '@iconify/css-svelte';
import '../../css/h/htelenzop.css';
import '../../css/d/d2kvgvbvc.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":12,"height":24};
const content = `<defs><path id="SVG1pzpbdYY" class="htelenzop"/></defs><use href="#SVG1pzpbdYY" transform="rotate(-180 5.02 9.505)" class="d2kvgvbvc"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:arrow-outlined" {...props}></Icon>
