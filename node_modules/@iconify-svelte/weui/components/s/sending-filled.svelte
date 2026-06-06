<script>
import Icon from '@iconify/css-svelte';
import '../../css/v/v-76gx-qr.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="v-76gx-qr"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:sending-filled" {...props}></Icon>
