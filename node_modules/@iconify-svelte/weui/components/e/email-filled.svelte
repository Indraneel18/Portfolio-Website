<script>
import Icon from '@iconify/css-svelte';
import '../../css/x/xn32-xxqh.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="xn32-xxqh"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:email-filled" {...props}></Icon>
