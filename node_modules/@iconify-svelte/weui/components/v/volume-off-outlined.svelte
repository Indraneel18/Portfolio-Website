<script>
import Icon from '@iconify/css-svelte';
import '../../css/y/yv3xjpb1i.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="yv3xjpb1i"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:volume-off-outlined" {...props}></Icon>
