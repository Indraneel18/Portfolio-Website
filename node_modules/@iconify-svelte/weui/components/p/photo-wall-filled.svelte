<script>
import Icon from '@iconify/css-svelte';
import '../../css/i/iy_u8mb7v.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="iy_u8mb7v"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:photo-wall-filled" {...props}></Icon>
