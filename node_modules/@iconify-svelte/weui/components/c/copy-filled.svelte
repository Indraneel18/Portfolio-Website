<script>
import Icon from '@iconify/css-svelte';
import '../../css/k/kvg7ngq4s.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="kvg7ngq4s"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:copy-filled" {...props}></Icon>
