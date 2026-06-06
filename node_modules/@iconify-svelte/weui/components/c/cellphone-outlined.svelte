<script>
import Icon from '@iconify/css-svelte';
import '../../css/t/ts7a0cbqt.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ts7a0cbqt"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:cellphone-outlined" {...props}></Icon>
