<script>
import Icon from '@iconify/css-svelte';
import '../../css/v/vdlgrqbmi.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="vdlgrqbmi"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:tv-filled" {...props}></Icon>
