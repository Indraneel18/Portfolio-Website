<script>
import Icon from '@iconify/css-svelte';
import '../../css/w/wstrnbusn.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="wstrnbusn"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:display-filled" {...props}></Icon>
