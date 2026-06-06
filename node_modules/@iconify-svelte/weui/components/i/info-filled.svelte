<script>
import Icon from '@iconify/css-svelte';
import '../../css/o/o09qunfod.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="o09qunfod"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:info-filled" {...props}></Icon>
