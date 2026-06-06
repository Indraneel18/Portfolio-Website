<script>
import Icon from '@iconify/css-svelte';
import '../../css/l/l5ekrf_pr.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="l5ekrf_pr"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:bellring-off-outlined" {...props}></Icon>
