<script>
import Icon from '@iconify/css-svelte';
import '../../css/a/ahhfo8gsg.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ahhfo8gsg"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:add-friends-outlined" {...props}></Icon>
