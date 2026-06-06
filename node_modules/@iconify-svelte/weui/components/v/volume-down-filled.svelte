<script>
import Icon from '@iconify/css-svelte';
import '../../css/b/bw_9acb2g.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="bw_9acb2g"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:volume-down-filled" {...props}></Icon>
