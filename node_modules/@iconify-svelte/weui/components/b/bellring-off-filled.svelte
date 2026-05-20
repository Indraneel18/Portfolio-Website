<script>
import Icon from '@iconify/css-svelte';
import '../../css/q/qapmv16xh.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="qapmv16xh"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:bellring-off-filled" {...props}></Icon>
