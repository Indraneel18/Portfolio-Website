<script>
import Icon from '@iconify/css-svelte';
import '../../css/q/qrnkw556h.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="qrnkw556h"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:share-filled" {...props}></Icon>
