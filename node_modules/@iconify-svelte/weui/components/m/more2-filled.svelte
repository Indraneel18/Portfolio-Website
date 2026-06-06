<script>
import Icon from '@iconify/css-svelte';
import '../../css/a/af6obb6it.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="af6obb6it"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:more2-filled" {...props}></Icon>
