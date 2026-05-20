<script>
import Icon from '@iconify/css-svelte';
import '../../css/t/tn8bdjb3l.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="tn8bdjb3l"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:folder-filled" {...props}></Icon>
