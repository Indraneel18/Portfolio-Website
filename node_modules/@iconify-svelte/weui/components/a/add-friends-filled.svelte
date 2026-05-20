<script>
import Icon from '@iconify/css-svelte';
import '../../css/s/sw_83acpv.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="sw_83acpv"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:add-friends-filled" {...props}></Icon>
