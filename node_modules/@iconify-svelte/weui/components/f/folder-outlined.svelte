<script>
import Icon from '@iconify/css-svelte';
import '../../css/d/dk5l3_60h.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="dk5l3_60h"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:folder-outlined" {...props}></Icon>
