<script>
fluid.def("fluid.demos.ai.colourBox", {
    $layers: "fluid.topLevelWidget",
    preferredSize: {
        w: 240,
        h: 170
    },
    state: {
        $reactiveRoot: {
            colour: "white"
        }
    }
});
</script>

<template>
    <div class="colour-box-widget">
        <div class="colour-box" style="background-color: @{state.colour}"></div>
        <div class="colour-box-buttons">
            <button class="colour-box-button colour-box-red" @onclick="{self}.state.colour = red">Red</button>
            <button class="colour-box-button colour-box-green" @onclick="{self}.state.colour = green">Green</button>
            <button class="colour-box-button colour-box-blue" @onclick="{self}.state.colour = blue">Blue</button>
        </div>
    </div>
</template>

<style>
.colour-box-widget {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 14px;
    padding: 16px;
    box-sizing: border-box;
    font-family: system-ui, sans-serif;
}

.colour-box {
    width: 90px;
    height: 90px;
    border: 1px solid #bbb;
    border-radius: 8px;
    transition: background-color 0.15s;
}

.colour-box-buttons {
    display: flex;
    gap: 8px;
}

.colour-box-button {
    padding: 6px 14px;
    border: 1px solid rgba(0, 0, 0, 0.2);
    border-radius: 4px;
    color: #fff;
    font: inherit;
    cursor: pointer;
}

.colour-box-red {
    background-color: red;
}

.colour-box-green {
    background-color: green;
}

.colour-box-blue {
    background-color: blue;
}
</style>

<provenance>
    <model>greenpt/deepseek-v4.1-flash</model>
    <prompt>Write a widget which contains three buttons, red, green and blue which change the colour of a box</prompt>
    <datestamp>2026-11-26T11:38:52.265Z</datestamp>
</provenance>
