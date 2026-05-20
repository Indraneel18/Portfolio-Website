<script>
import Icon from '@iconify/css-svelte';
import '../../css/p/pxzds_lzk.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="pxzds_lzk"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:add-outlined" {...props}></Icon>
