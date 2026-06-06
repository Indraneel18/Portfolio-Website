<script>
import Icon from '@iconify/css-svelte';
import '../../css/f/fxmz9hxtz.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="fxmz9hxtz"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:add2-outlined" {...props}></Icon>
