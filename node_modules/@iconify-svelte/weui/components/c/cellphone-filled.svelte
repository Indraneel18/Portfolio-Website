<script>
import Icon from '@iconify/css-svelte';
import '../../css/z/zxe-cybdu.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="zxe-cybdu"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:cellphone-filled" {...props}></Icon>
