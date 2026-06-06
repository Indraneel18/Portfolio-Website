<script>
import Icon from '@iconify/css-svelte';
import '../../css/i/ifwdv1pih.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ifwdv1pih"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:play-outlined" {...props}></Icon>
