<script>
import Icon from '@iconify/css-svelte';
import '../../css/d/ddjvgw_uj.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ddjvgw_uj"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:help-filled" {...props}></Icon>
