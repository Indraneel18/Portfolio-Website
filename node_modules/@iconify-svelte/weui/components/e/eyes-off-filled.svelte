<script>
import Icon from '@iconify/css-svelte';
import '../../css/c/cdngy1b-b.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="cdngy1b-b"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:eyes-off-filled" {...props}></Icon>
