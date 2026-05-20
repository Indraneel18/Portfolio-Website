<script>
import Icon from '@iconify/css-svelte';
import '../../css/y/yc2f8fcca.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="yc2f8fcca"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:refresh-filled" {...props}></Icon>
