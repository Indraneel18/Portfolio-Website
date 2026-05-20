<script>
import Icon from '@iconify/css-svelte';
import '../../css/t/t75_zubnw.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="t75_zubnw"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:mike2-outlined" {...props}></Icon>
