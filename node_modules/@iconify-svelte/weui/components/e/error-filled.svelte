<script>
import Icon from '@iconify/css-svelte';
import '../../css/m/mhabiq8ru.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="mhabiq8ru"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:error-filled" {...props}></Icon>
