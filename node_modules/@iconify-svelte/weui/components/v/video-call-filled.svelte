<script>
import Icon from '@iconify/css-svelte';
import '../../css/t/t9i8o1zkq.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="t9i8o1zkq"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:video-call-filled" {...props}></Icon>
