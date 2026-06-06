<script>
import Icon from '@iconify/css-svelte';
import '../../css/o/or-9nt8zt.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="or-9nt8zt"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:lock-filled" {...props}></Icon>
