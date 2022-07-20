<template>
    <div class="field-container">
        <div class="field">
            <div class="field-line" :class="{ selected: isSelected }"></div>
            <img alt="" class="field-icon" :src="props.icon" />
            <div class="field-separator"></div>
            <div class="field-control">
                <template v-if="true">
                    <input :type="props.isPassword ? 'password' : 'email'" ref="fieldInput" class="field-input"
                        :class="{ selected: isSelected }" v-model="text" :placeholder="props.placeholder"
                        @keypress.enter="selectField('common')" @focusin="selectField(props.name)"
                        @focusout="selectField('common')" />
                </template>
                <template v-else>
                    <template v-if="props.isPassword">
                        <div class="field-password-dots">
                            <template v-for="i in [...Array(text.length || 8)]">
                                <div class="field-password-dot"></div>
                            </template>
                        </div>
                    </template>
                    <template v-else>
                        <div class="field-placeholder">
                            {{ text || props.placeholder }}
                        </div>
                    </template>
                </template>
            </div>
        </div>
    </div>
</template>

<script setup>
import { inject, ref, watch } from 'vue'

const props = defineProps({
    name: {
        type: String,
        default: "common"
    },
    isSelected: {
        type: Boolean,
        default: false
    },
    isPassword: {
        type: Boolean,
        default: false
    },
    placeholder: {
        type: String,
        default: "jimena_rosas@gmail.com"
    },
    icon: {
        type: String,
        default: "https://static.overlay-tech.com/assets/dae722a5-921d-42ec-927b-063383420c6b.svg"
    }
})

const fieldInput = ref(null)

const text = ref("")

const isSelected = ref(false)

const fieldSelected = inject('field/selected')
const selectField = inject('field/@select')

watch(fieldSelected, name => {
    isSelected.value = name === props.name
    if (isSelected.value) {
        setTimeout(() => {
            console.log(fieldInput)
            fieldInput.value.focus()
        }, 0)
    }
})
</script>

<style lang="scss">
.field-container {
    width: 100%;
    padding-bottom: 12px;
    overflow: hidden;
    position: relative;
}

.field {
    padding: 0 12px;
    display: flex;
    align-items: center;
    position: relative;
}

.field-control {
    width: 100%;
    padding-left: 12px;
    display: flex;
    align-items: center;
}

.field-input {
    width: 100%;
    font-family: "Roboto";
    font-size: 14px;
    font-weight: 500;
    color: rgba(157, 157, 157, 1);
    border: 0px;
    outline: none;
    -webkit-appearance: none;
}

.field-input.selected {
    color: rgba(125, 125, 253, 1);
}

/*.field-input[type='password'] {
    font-size: 34px;
}*/

.field-separator {
    height: 54px;
}

.field-line {
    width: 100%;
    height: 1px;
    background-color: rgba(0, 0, 0, 0.55);
    position: absolute;
    left: 0;
    bottom: 0px;
}

.field-line.selected {
    height: 1px;
    background-color: rgba(125, 125, 253, 1);
}

.field-icon {
    align-self: center;
}

.field-placeholder {
    height: 48px;
    font-family: "Roboto";
    font-size: 14px;
    font-weight: 500;
    line-height: 48px;
    color: rgba(157, 157, 157, 1);
}

.field-password-dots {
    height: 48px;
    display: flex;
    align-items: center;
    line-height: 48px;
}

.field-password-dot {
    width: 8px;
    height: 8px;
    background-color: rgba(138, 138, 138, 1);
    border-radius: 50%;

    &:not(:last-of-type) {
        margin-right: 5px;
    }
}
</style>