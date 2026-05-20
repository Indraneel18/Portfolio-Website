<script>
import Icon from '@iconify/css-svelte';
import '../../css/z/zh_g21kfm.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="zh_g21kfm"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:transfer2-filled" {...props}></Icon>
