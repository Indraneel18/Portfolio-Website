<script>
import Icon from '@iconify/css-svelte';
import '../../css/d/duz0nmbix.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="duz0nmbix"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:max-window-filled" {...props}></Icon>
