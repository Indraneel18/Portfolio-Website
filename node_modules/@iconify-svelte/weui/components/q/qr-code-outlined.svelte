<script>
import Icon from '@iconify/css-svelte';
import '../../css/x/xmvj3g29q.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="xmvj3g29q"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:qr-code-outlined" {...props}></Icon>
