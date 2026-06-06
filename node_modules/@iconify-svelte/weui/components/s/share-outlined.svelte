<script>
import Icon from '@iconify/css-svelte';
import '../../css/p/pffvj1x9j.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="pffvj1x9j"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:share-outlined" {...props}></Icon>
