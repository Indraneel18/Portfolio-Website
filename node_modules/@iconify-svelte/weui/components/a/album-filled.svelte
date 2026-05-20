<script>
import Icon from '@iconify/css-svelte';
import '../../css/n/nw1le6i8b.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="nw1le6i8b"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:album-filled" {...props}></Icon>
