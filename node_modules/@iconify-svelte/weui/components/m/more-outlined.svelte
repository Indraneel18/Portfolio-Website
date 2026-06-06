<script>
import Icon from '@iconify/css-svelte';
import '../../css/v/va_msi63q.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="va_msi63q"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:more-outlined" {...props}></Icon>
