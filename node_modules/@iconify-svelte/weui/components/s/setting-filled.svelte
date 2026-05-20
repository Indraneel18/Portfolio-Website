<script>
import Icon from '@iconify/css-svelte';
import '../../css/l/lpljrfbmf.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="lpljrfbmf"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:setting-filled" {...props}></Icon>
