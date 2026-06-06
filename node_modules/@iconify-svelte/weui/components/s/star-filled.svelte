<script>
import Icon from '@iconify/css-svelte';
import '../../css/b/bmewq3_yc.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="bmewq3_yc"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:star-filled" {...props}></Icon>
