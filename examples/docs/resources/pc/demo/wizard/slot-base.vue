<template>
  <tiny-wizard :data="dataSet" :page-guide="true">
    <template #base="data">
      <div>{{ data.slotScope.name }}</div>
    </template>
  </tiny-wizard>
</template>

<script lang="jsx">
import { Wizard, Modal } from '@opentiny/vue'

export default {
  components: {
    TinyWizard: Wizard
  },
  data() {
    return {
      dataSet: [
        {
          name: '出差信息填写',
          status: 'ready'
        },
        {
          name: '项目信息填写',
          status: 'doing'
        },
        {
          name: '主管审批',
          status: 'wait'
        },
        {
          name: '权签人审批',
          status: 'wait'
        },
        {
          name: '完成申请',
          status: 'wait'
        }
      ]
    }
  },
  methods: {
    btnClick(arg) {
      Modal.message(`步骤${arg}`)
    }
  }
}
</script>
