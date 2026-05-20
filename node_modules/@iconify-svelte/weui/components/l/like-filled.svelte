<script>
import Icon from '@iconify/css-svelte';
import '../../css/w/wuzkqezjq.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="wuzkqezjq"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:like-filled" {...props}></Icon>
