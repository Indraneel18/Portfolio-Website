<script>
import Icon from '@iconify/css-svelte';
import '../../css/j/j9ipaj3xt.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="j9ipaj3xt"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:transfer-filled" {...props}></Icon>
