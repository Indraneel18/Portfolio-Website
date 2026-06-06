<script>
import Icon from '@iconify/css-svelte';
import '../../css/e/e3pk9cb7p.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="e3pk9cb7p"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:music-off-outlined" {...props}></Icon>
