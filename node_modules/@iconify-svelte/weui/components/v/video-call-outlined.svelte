<script>
import Icon from '@iconify/css-svelte';
import '../../css/o/ojvv9rbfs.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ojvv9rbfs"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:video-call-outlined" {...props}></Icon>
