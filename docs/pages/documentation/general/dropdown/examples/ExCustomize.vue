<template>
    <b-dropdown v-model="isPublic">
        <button class="button is-primary" type="button" slot="trigger">
            <template v-if="isPublic">
                <b-icon icon="public"></b-icon>
                <span>Public</span>
            </template>
            <template v-else>
                <b-icon icon="people"></b-icon>
                <span>Friends</span>
            </template>
            <b-icon icon="arrow_drop_down"></b-icon>
        </button>

        <b-dropdown-item :value="true">
            <div class="media">
                <b-icon class="media-left" icon="public"></b-icon>
                <div class="media-content">
                    <h3>Public</h3>
                    <small>Everyone can see</small>
                </div>
            </div>
        </b-dropdown-item>

        <b-dropdown-item :value="false">
            <div class="media">
                <b-icon class="media-left" icon="people"></b-icon>
                <div class="media-content">
                    <h3>Friends</h3>
                    <small>Only friends can see</small>
                </div>
            </div>
        </b-dropdown-item>
    </b-dropdown>
</template>

<script>
    export default {
        data() {
            return {
                isPublic: true
            }
        }
    }
</script>
