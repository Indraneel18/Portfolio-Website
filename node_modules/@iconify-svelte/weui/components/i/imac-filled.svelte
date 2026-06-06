<script>
import Icon from '@iconify/css-svelte';
import '../../css/d/dbiybx0vg.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="dbiybx0vg"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:imac-filled" {...props}></Icon>
