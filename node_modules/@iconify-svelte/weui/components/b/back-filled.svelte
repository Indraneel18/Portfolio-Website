<script>
import Icon from '@iconify/css-svelte';
import '../../css/c/cfghgstxk.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":12,"height":24};
const content = `<path class="cfghgstxk"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:back-filled" {...props}></Icon>
