<template>
    <div class="body">
        <PowerBIReportEmbed :embedConfig=config>
        </PowerBIReportEmbed>
    </div>
</template>

<script>
import { PowerBIReportEmbed } from 'powerbi-client-vue-js';
import * as powerbi from 'powerbi-client';

export default
    {
        components: { PowerBIReportEmbed },
        data() {
            const config = {
                type: "report",
                id: 'c68b93ed-6da6-4f61-844c-be97c5887fd7',
                embedUrl: "https://app.powerbi.com/reportEmbed?reportId=0d8607d3-2749-4fdc-84b2-064135e1a233&groupId=49b68d64-e888-49b4-bd4e-6df15473bd22&w=2&config=eyJjbHVzdGVyVXJsIjoiaHR0cHM6Ly9XQUJJLVVLLVNPVVRILUMtUFJJTUFSWS1yZWRpcmVjdC5hbmFseXNpcy53aW5kb3dzLm5ldCIsImVtYmVkRmVhdHVyZXMiOnsidXNhZ2VNZXRyaWNzVk5leHQiOnRydWV9fQ%3d%3d",
                accessToken: "H4sIAAAAAAAEACWUt66EVgBE_-W1WGKJFyy5IC9LzqFjyTlHy__uZ7kfTXE0Z_7-MZO7G5Ps58-fVj5YHzmZMEs5RZKnorYXnH9DNBo7Sy8eHzUuIDy_j52XZtBbcA09QlpakwgsxAWeXLBVJ0K2eq83l1H4ZspCJhAz8QYlUVJDwWoVytvaqnbYzqAIfZpNiGyV6mJioa5vBr_nNdXDiRG-TV0qiClgSD36UbqMtRj4wr0dntWLznZDZsNRM6LLM2Nxjgx_9oZ7XfuFmdtNJgQqYkLB0sd8SPEEDLw0XGygIbJoza0UIeN9vfYMaV8p2t1bPu73gOE164kTuWLRM2e4K-RUAjXAl8LreJaPkVavJQoowxtjQ1nur7OFzPdDPmQTGJQE27JPj2jmg6pYaOMbpQOCfwg9f7STJrkSZIITyYlbfT_O2DsJfgWijTRV2evG20O3lYHzQZ8esURv7LiMtY1HajVO0cBbcxolrfgk9V2NOdfLBNjjoZ_MNhXhNZuWqtWtfduOJ9RXjMEDOXgyztS-0vrhrFRFZM6y7Y5qMvtceG6Lod4vjxIXMnnvNYRSZMXjgrO_aSdS4nSIWzR9NZAilSS5-juBi0B8pN_Srb26kkmcXCVUM-SXLOugMw-xecw09UJu8zGTEbFhZoezC1IDxW8FKtLeKci8r2c97cGtZxKqu7OVZTiZDwiqhZaGTMPd8v3K3TLsUrxgO1IhTSZxWbi7CuUrfiUHFccvglQgH9jmEUUVkHOE8YniEjMd0NAbB0iLLU6mTuEsdQzjb9reEA15Hkaoz9vtnt4nwdVXhF_f21OvolbvSGgWKkkru6XFY-nOWvrdoePMimolmn4UFEzZ9SzPsJFisZWSwSrFqGO5Ff9aoa_VICJGOZ4tOQ7OCFKgHmP688cPt9zTNir5_asTY7iWaAOgKLWyIoLQK4t71pX2SrDbEUlKJkIcpJ067R6_DBNCHKwEhDT05V4nywogmGVn3-xD4sdm0GhwQpHjqFOp-rILzKwir7KzupVdn4UvWJPpDIXLPMLCMaOZu_Z41DbMwrgRqtqzi3dPIZvNhjGoudoiD8AmvimtLtS5d5nPh9MCll91-XAi7Umy1i8iZzUtZHx5Os-x4vEkDHZ5mv0wXEwAxOQXlK9XusKLG8tpXfBFw7zc24ikZu1O_5whb9LmWvbQLJEG-RJLyOdyX6iiGI2Rl4OVEj9M7sQFbZm_IBtD0eIYSxpm-GASZdjo-KPsTU8BvSCOn1MuzILemb_--g_zPVX5Ivu_lIeg50WvToSAoG-OPd9xIQX_p5y6HJJtX_LfGLl5Uozt0Gpr3TvRmSiBX0KfzZh8oYQNFCSwEMn3CCCSXL8YqqvQ03Xr4BzNZfN08OifnILoDzbLeU5YFxccQOKFXdKNc6mJcqm8kXMr8sElS3rijqRc0UNg_erWJLaZuRfxmEjli_sV9fV7OorVRsggwVrHp6dfWLRRsi3-jgGE2qRKF2c-D0O8Z8wQOmBaGc2FvrzXTQTyufF9F3Bvp_YY7LDTwZ_oGhTvGJe2NLdQT26LiOiXn9-9huJ9Ron3uxL09vXObSnVfSW7ovqhHPQEG6FgVYPYLIy9bCmzWMDJ_ts2XOqYiz5cBtZ44uCWhVSZ6EVQLO0NDFXdhJZ8FFsvfzH_8y9NsbVqQgYAAA==.eyJjbHVzdGVyVXJsIjoiaHR0cHM6Ly9XQUJJLVVLLVNPVVRILUMtUFJJTUFSWS1yZWRpcmVjdC5hbmFseXNpcy53aW5kb3dzLm5ldCIsImV4cCI6MTY5NzY5NjY2NSwiYWxsb3dBY2Nlc3NPdmVyUHVibGljSW50ZXJuZXQiOnRydWV9",
                tokenType: powerbi.models.TokenType.Embed,
                settings: {
                    panes: {
                        filters: {
                            expanded: false,
                            visible: true
                        }
                    },
                    background: powerbi.models.BackgroundType.Transparent,
                }
            }
            return { config }
        }
    }
</script>

<style>
#reportContainer {
    height: 100vh;
}
</style>