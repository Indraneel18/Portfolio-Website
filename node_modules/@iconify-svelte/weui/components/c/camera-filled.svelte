<script>
import Icon from '@iconify/css-svelte';
import '../../css/j/j9-i_-b7h.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="j9-i_-b7h"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:camera-filled" {...props}></Icon>
