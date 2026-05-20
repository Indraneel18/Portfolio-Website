<script>
import Icon from '@iconify/css-svelte';
import '../../css/a/ay5vrhx8z.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ay5vrhx8z"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:delete-outlined" {...props}></Icon>
