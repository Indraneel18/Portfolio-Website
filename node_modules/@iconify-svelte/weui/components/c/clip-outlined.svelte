<script>
import Icon from '@iconify/css-svelte';
import '../../css/i/i415jqsuv.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="i415jqsuv"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:clip-outlined" {...props}></Icon>
