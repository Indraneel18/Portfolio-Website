<script>
import Icon from '@iconify/css-svelte';
import '../../css/i/ihus6ub9o.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ihus6ub9o"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:qr-code-filled" {...props}></Icon>
