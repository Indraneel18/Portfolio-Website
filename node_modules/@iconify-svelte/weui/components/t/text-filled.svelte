<script>
import Icon from '@iconify/css-svelte';
import '../../css/l/lawx27b8q.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="lawx27b8q"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:text-filled" {...props}></Icon>
