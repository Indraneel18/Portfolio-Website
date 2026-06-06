<script>
import Icon from '@iconify/css-svelte';
import '../../css/q/qsqmarbtx.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="qsqmarbtx"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:add2-filled" {...props}></Icon>
