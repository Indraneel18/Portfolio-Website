<script>
import Icon from '@iconify/css-svelte';
import '../../css/r/r3eodj1_m.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="r3eodj1_m"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:link-filled" {...props}></Icon>
