<script>
import Icon from '@iconify/css-svelte';
import '../../css/d/dbgxo8jma.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="dbgxo8jma"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:star-outlined" {...props}></Icon>
