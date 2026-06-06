<script>
import Icon from '@iconify/css-svelte';
import '../../css/b/br4wb9f0t.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="br4wb9f0t"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:transfer-text-outlined" {...props}></Icon>
