<script>
import Icon from '@iconify/css-svelte';
import '../../css/r/rnt9_cbtg.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="rnt9_cbtg"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:download-filled" {...props}></Icon>
