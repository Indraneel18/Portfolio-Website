<script>
import Icon from '@iconify/css-svelte';
import '../../css/s/s68wt2biy.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="s68wt2biy"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:music-off-filled" {...props}></Icon>
