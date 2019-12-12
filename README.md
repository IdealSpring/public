# project

> aido敏捷开发云


## 技术栈
- 传说中的VUE全家桶(vue vue-router vuex)
- 打包工具：webpack
- 核心语法库：vue
- 前后端交互：axios
- 前端路由：vue-router
- 前端状态管理：vuex
- 前端样式预编译：stylus
- mock数据：node.js文件服务器（express+formidable+gm）
- 前端样式组件：element-UI
- vue与jQuery混合使用，以便利用jQuery插件，JQ版本1.12
## 2安装运行

``` bash
# install dependencies
cd public/client
npm install

# server with hot reload at localhost:8082
npm run dev

# fileResfulServer as a static data server listening at localhost:8070
node fileResfulServer.js

# build for production with minification
npm run build
```

## 前端发布（npm run build）
- 如果是本机手工部署
- 修改dist/static/js中以app.开头的js文件（eg：app.c41cc4aec93bcb087f1c.js）
- 将其中的baseUrl替换成用户本地实际IP地址和端口
- 如果是服务器自动部署
- npm run build
- nginx 需要设置代理，将aido-web代理到后台gateway上

## 代码目录

``` bash

├─build
│      build.js
│      check-versions.js
│      dev-client.js
│      dev-server.js
│      utils.js
│      vue-loader.conf.js
│      webpack.base.conf.js
│      webpack.dev.conf.js
│      webpack.prod.conf.js
│
├─config
│      dev.env.js
│      index.js
│      prod.env.js
│
├─mock
│      1.json
│      backlog.json
│      backlogEdtor.json
│      backlogLane.json
│      backlogList.json
│      backlogPepole.json
│      backlogTypes.json
│      batchDownload.json
│      cancelBacklog.json
│      cancelSprint.json
│      canDelPerson.json
│      caseColumes.json
│      caseCustomfields.json
│      caseEdtor.json
│      caseList.json
│      changeLane.json
│      changePassword.json
│      checkCanCreateTask.json
│      checkOldPassword.json
│      checkProjectNameRepeat.json
│      checkSprintTime.json
│      chooseProject.json
│      config.json
│      connectSprintStroy.json
│      createdStory.json
│      createProject.json
│      createSprint.json
│      createTask.json
│      dashboardBase.json
│      dashboardThroughout.json
│      dashboardWorkload.json
│      deleteBacklog.json
│      deleteSprint.json
│      deleteStory.json
│      delProject.json
│      dropTask.json
│      editProject.json
│      editTask.json
│      faultColumes.json
│      faultCreated.json
│      faultEdt.json
│      faultLevels.json
│      faultRelSprint.json
│      faultsCreateNames.json
│      faultsfixedNames.json
│      faultsTestNames.json
│      finishSprint.json
│      followProject.json
│      followProject0.json
│      followProject1.json
│      getBacklogByStroyId.json
│      getBurndowns.json
│      getCaseContent.json
│      getCaseScale.json
│      getCurrentProject.json
│      getDefault.json
│      getDefaults.json
│      getDefectByStoryId1.json
│      getDefectByStoryId2.json
│      getExampleByStoryId1.json
│      getExampleByStoryId2.json
│      getIteration.json
│      getLoginUser.json
│      getModule.json
│      getProjectByBacklogId.json
│      getProjectById.json
│      getProjects.json
│      getProjectsByName.json
│      getProjectsByName1.json
│      getProjectsMine.json
│      getProjectsOther.json
│      getProjectsVisible.json
│      getRequirements.json
│      getRequirementsByState1.json
│      getRequirementsByState2.json
│      getRequirementsByState3.json
│      getRequirementsByState4.json
│      getRequirementsByState5.json
│      getSelectedProject.json
│      getSelectedProjectBytoken.json
│      getSprintUsers.json
│      getStory.json
│      getStoryByRqmId1.json
│      getStoryByRqmId2.json
│      getStoryByRqmId3.json
│      getStoryTaskBySpringId.json
│      getStroyTaskBySprintIdForboard.json
│      getTaskById.json
│      getTaskByStoryId1.json
│      getTaskByStoryId2.json
│      getTaskHistoryById.json
│      getTasksBySrpingIdForPage.json
│      getTeam.json
│      getUndoStoryforSprint.json
│      getUndoStoryforSprint2.json
│      getUndoStoryforSprint3.json
│      getUsers.json
│      getWorkload.json
│      isManager.json
│      laneCount.json
│      log.json
│      log1105.json
│      log1107.json
│      login.json
│      logout.json
│      mission.json
│      moduleDelete.json
│      postModule.json
│      putStory.json
│      putStorySprints.json
│      queryBacklog.json
│      reCreateds.json
│      resources.json
│      searchTemplate.json
│      smallStoryList.json
│      sprint.json
│      sprintById.json
│      sprintReview.json
│      sprintReviewAllStory.json
│      sprintReviewPerson.json
│      sprintReviewPersonWorkLoad.json
│      sprintReviewTask.json
│      sprintsAll.json
│      sprintsMembers.json
│      sprintsTeams.json
│      sprintTable.json
│      startProject.json
│      stopProject.json
│      storyCountLane.json
│      storyEdtor.json
│      storyLanes.json
│      storyList.json
│      storyPepole.json
│      storySprints.json
│      subSystems.json
│      taskTypes.json
│      token.json
│      updateUserInfo.json
│      user.json
│      userUpdate.json
│      user_getLoginUser.json
│      workflow_dynamicList.json
│
├─src
│  │  App.vue
│  │  main.js
│  │
│  ├─common
│  │  ├─css
│  │  │  │  color.styl
│  │  │  │  common.styl
│  │  │  │  font.css
│  │  │  │  reset.css
│  │  │  │
│  │  │  ├─jcrop
│  │  │  │      Jcrop.gif
│  │  │  │      jquery.Jcrop.min.css
│  │  │  │
│  │  │  ├─jsmind
│  │  │  │      jsmind-DIY.css
│  │  │  │      jsmind.css
│  │  │  │
│  │  │  ├─progress
│  │  │  │      myProgress.css
│  │  │  │
│  │  │  └─uploadifive
│  │  │          uploadifive-cancel.png
│  │  │          uploadifive.css
│  │  │
│  │  ├─font
│  │  │      iconfont.eot
│  │  │      iconfont.svg
│  │  │      iconfont.ttf
│  │  │      iconfont.woff
│  │  │
│  │  ├─img
│  │  │      bg-line.png
│  │  │      home.png
│  │  │      hu.jpg
│  │  │      upload.png
│  │  │      wavy.jpg
│  │  │
│  │  ├─js
│  │  │      jquery.myProgress.js
│  │  │      jquery.uploadifive.js
│  │  │      jsmind.js
│  │  │      ls.js
│  │  │      multipleWin.js
│  │  │      params.js
│  │  │      publicDesc.js
│  │  │      resfulUrl.js
│  │  │      rightmenu.js
│  │  │
│  │  └─kalendae
│  │          arrows.png
│  │          close.png
│  │          kalendae.css
│  │          kalendae.standalone.js
│  │
│  ├─components
│  │  │  NoPages.vue
│  │  │
│  │  ├─agile
│  │  │      agileCreate.vue
│  │  │      agileCreateMain.vue
│  │  │      agileEdit.vue
│  │  │      agileListMain.vue
│  │  │      agileMain.vue
│  │  │      agileReview.vue
│  │  │      agileReviewMain.vue
│  │  │      agileTaskMain.vue
│  │  │      agileTimeLine.vue
│  │  │      createTask.vue
│  │  │      review.png
│  │  │
│  │  ├─agileCalendar
│  │  │      agileCalendar.vue
│  │  │
│  │  ├─basicSetup
│  │  │  │  basicSetup.vue
│  │  │  │  sideDraw.vue
│  │  │  │
│  │  │  └─components
│  │  │          affairsState.vue
│  │  │          affairsTemplate.vue
│  │  │          aiDialog.vue
│  │  │          fieldsSetting.vue
│  │  │          publicStateSetting.vue
│  │  │          settingTable.vue
│  │  │          tools.js
│  │  │
│  │  ├─compare
│  │  │      codemirror.css
│  │  │      codemirror.js
│  │  │      compare.vue
│  │  │      mergely.css
│  │  │      mergely.js
│  │  │      searchcursor.js
│  │  │
│  │  ├─dashboard
│  │  │  │  main.vue
│  │  │  │
│  │  │  └─subTools
│  │  │      │  agile.vue
│  │  │      │  agileSprint.vue
│  │  │      │  autoTest.vue
│  │  │      │  cicd.vue
│  │  │      │  sonarCodeQuality.vue
│  │  │      │  sonarProductivity.vue
│  │  │      │
│  │  │      ├─autoTestComponent
│  │  │      │      lineChart.vue
│  │  │      │      pieChart.vue
│  │  │      │      tableChart.vue
│  │  │      │
│  │  │      └─cicdComponent
│  │  │              cicdChart.vue
│  │  │              cicdTable.vue
│  │  │              resultTable.vue
│  │  │
│  │  ├─defect
│  │  │      defect.js
│  │  │      defectCreated.vue
│  │  │      defectCreatedMain.vue
│  │  │      defectEdtor.vue
│  │  │      defectList.vue
│  │  │      defectMain.vue
│  │  │
│  │  ├─emailSetting
│  │  │      emailSetting.vue
│  │  │
│  │  ├─fieldSetting
│  │  │      fieldSetting.vue
│  │  │      fieldSettingDetail.vue
│  │  │      fieldSettingList.vue
│  │  │
│  │  ├─globalWebsocket
│  │  │      globalWebsocket.vue
│  │  │
│  │  ├─header
│  │  │      header.vue
│  │  │      logo.png
│  │  │
│  │  ├─home
│  │  │      home.vue
│  │  │
│  │  ├─kanban
│  │  │  │  kanban.vue
│  │  │  │
│  │  │  ├─components
│  │  │  │      boardView.vue
│  │  │  │      card-detail-panel.vue
│  │  │  │      card.vue
│  │  │  │      cardMenu.vue
│  │  │  │      choose-panel.vue
│  │  │  │      horizonLane.vue
│  │  │  │      tableView.vue
│  │  │  │      verticalLane.vue
│  │  │  │
│  │  │  ├─computed
│  │  │  │      kanbanComputed.js
│  │  │  │
│  │  │  ├─data
│  │  │  │      kanbanData.js
│  │  │  │
│  │  │  ├─directives
│  │  │  │      kanbanDirectives.js
│  │  │  │
│  │  │  ├─kanbanCSS
│  │  │  │      kanbanCSS_global.css
│  │  │  │      kanbanCSS_kanban.styl
│  │  │  │
│  │  │  ├─methods
│  │  │  │      boardView.js
│  │  │  │      cardMethods.js
│  │  │  │      common.js
│  │  │  │      dragCard.js
│  │  │  │      horizonLane.js
│  │  │  │      kanbanMethods.js
│  │  │  │      tableView.js
│  │  │  │      verticalLane.js
│  │  │  │
│  │  │  ├─mounted
│  │  │  │      kanbanMounted.js
│  │  │  │
│  │  │  ├─updated
│  │  │  │      kanbanUpdated.js
│  │  │  │
│  │  │  └─watch
│  │  │          kanbanWatch.js
│  │  │
│  │  ├─login
│  │  │      ADMPLogin.vue
│  │  │      JSBOMCLogin.vue
│  │  │      login.vue
│  │  │      resetPwd.vue
│  │  │
│  │  ├─mail
│  │  │      mail.vue
│  │  │
│  │  ├─module
│  │  │      main.vue
│  │  │
│  │  ├─nav
│  │  │      nav.vue
│  │  │
│  │  ├─notice
│  │  │      noticeList.vue
│  │  │      noticePopUp.vue
│  │  │
│  │  ├─panoramicView
│  │  │      mindMap.vue
│  │  │      panoramicView.vue
│  │  │      storyWall.vue
│  │  │
│  │  ├─project
│  │  │      card-view-mine.vue
│  │  │      card-view-other.vue
│  │  │      create-user-panel.vue
│  │  │      edit-project-panel.vue
│  │  │      new_projectSelect.vue
│  │  │      project.vue
│  │  │      projectSelect.vue
│  │  │      table-view.vue
│  │  │
│  │  ├─reportView
│  │  │      chartsContainer.vue
│  │  │      reportView.vue
│  │  │
│  │  ├─requirement
│  │  │      createdReMain.vue
│  │  │      lane.png
│  │  │      reCreated.vue
│  │  │      reEdtor.vue
│  │  │      reLane.vue
│  │  │      requirementListMain.vue
│  │  │      requirementMain.vue
│  │  │
│  │  ├─right
│  │  │      rightSetting.vue
│  │  │
│  │  ├─staff
│  │  │      head_100X100.gif
│  │  │      head_150X150.gif
│  │  │      head_60X60.gif
│  │  │      personalSetting.vue
│  │  │      staffCenter.vue
│  │  │      up_head.jpg
│  │  │
│  │  ├─story
│  │  │  │  lane.png
│  │  │  │  storyCreated.vue
│  │  │  │  storyCreatedMain.vue
│  │  │  │  storyEdtor.vue
│  │  │  │  storyLane.vue
│  │  │  │  storyList.vue
│  │  │  │  storyMain.vue
│  │  │  │
│  │  │  └─split
│  │  │          caseTools.vue
│  │  │          faultTools.vue
│  │  │
│  │  ├─testPlan
│  │  │      create.vue
│  │  │      edit.vue
│  │  │      list.vue
│  │  │      main.vue
│  │  │
│  │  ├─tools
│  │  │  │  atitle.vue
│  │  │  │  back.vue
│  │  │  │  backlogInfoDialog.vue
│  │  │  │  caseListDialog.vue
│  │  │  │  caseRelListDialog.vue
│  │  │  │  changeInfo.vue
│  │  │  │  colorPanel.vue
│  │  │  │  createTaskPage.vue
│  │  │  │  customfieldRenderer.vue
│  │  │  │  customHorizonScrollBar.vue
│  │  │  │  customMenu.vue
│  │  │  │  defectCreateDialog.vue
│  │  │  │  defectDefult.vue
│  │  │  │  histories.vue
│  │  │  │  historyDescDialog.vue
│  │  │  │  Loading4.gif
│  │  │  │  reDetails.vue
│  │  │  │  requirementsList.vue
│  │  │  │  search.vue
│  │  │  │  selectorPanel.vue
│  │  │  │  socketio.vue
│  │  │  │  sockjs.vue
│  │  │  │  sprintListDialog.vue
│  │  │  │  storyInfoAll.vue
│  │  │  │  storyListDialog.vue
│  │  │  │  taskInfoAll.vue
│  │  │  │  timeline.vue
│  │  │  │  useCaseCreate.vue
│  │  │  │  useCaseDefult.vue
│  │  │  │  wangEditor.vue
│  │  │  │
│  │  │  ├─drawer
│  │  │  │      drawer.vue
│  │  │  │      drawer_body.vue
│  │  │  │
│  │  │  └─loading
│  │  │          index.js
│  │  │          loading.vue
│  │  │
│  │  ├─useCase
│  │  │      useCaseCreated.vue
│  │  │      useCaseCreatedMain.vue
│  │  │      useCaseEdtor.vue
│  │  │      useCaseList.vue
│  │  │      useCaseMain.vue
│  │  │
│  │  ├─versionPlan
│  │  │      versionPlan.vue
│  │  │
│  │  ├─view
│  │  │      bg.png
│  │  │      checked.png
│  │  │      click.png
│  │  │      dom.png
│  │  │      done.png
│  │  │      mask.png
│  │  │      nav-bg-hover.png
│  │  │      nav-bg.png
│  │  │      no.png
│  │  │      peple.png
│  │  │      selected.png
│  │  │      sprint.png
│  │  │      view.vue
│  │  │
│  │  └─workplace
│  │          workplace.vue
│  │
│  ├─filters
│  │      index.js
│  │      string.js
│  │      time.js
│  │
│  ├─http
│  │      api.js
│  │      http.js
│  │      path.js
│  │
│  ├─router
│  │      changeRoutes.js
│  │      index.js
│  │      routesKanban.js
│  │      routesScrum.js
│  │
│  └─store
│          actions.js
│          getters.js
│          mutations.js
│          store.js
│          type.js
│
└─static
    │  .gitkeep
    │
    ├─html
    │      unsupport-browser.html
    │
    ├─img
    │  │  404.png
    │  │  chrome.png
    │  │  default-head.png
    │  │  favicon.ico
    │  │  fireFox.png
    │  │  head_150X150.gif
    │  │  Opera.png
    │  │  Safari.png
    │  │  up_head.jpg
    │  │
    │  └─login
    │          browserSuport.png
    │          login-logo-adcloud.png
    │          login-logo-cmc.png
    │          login-logo.png
    │          login.jpg
    │          logo-cmc.png
    │          logo.png
    │
    ├─js
    │      jquery.nicescroll.min.js
    │
    └─staticData
            staticData.js

20190925 update4222
