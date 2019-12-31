# UIKIT
Script adaptation
public class NEARXDEMO_01WIDGET_014 extends NearxDemoBase {
    @Override
    protected boolean test() throws Exception {
        logger.info("1.点击“控件” ");
        Widget.click(TOPO.phoneDUT, HomePage.WidgetS, ClickType.NORMAL);

        logger.info("2.点击 “开关” ");
        Widget.click(TOPO.phoneDUT,WidgetPage.SWITCH,ClickType.NORMAL);
        Widget.clickSimilarNodeByBatch(TOPO.phoneDUT, WidgetPage.TEST_CLASSAME_SWITCH,WidgetPage.TEST_COUNT_SWITCH,ClickType.NORMAL);
        Common.wait(TOPO.phoneDUT,2);
        Common.goBack(TOPO.phoneDUT);

        logger.info("3.点击 “下载组件” ");
        Widget.click(TOPO.phoneDUT,WidgetPage.LOADING,ClickType.NORMAL);
        Widget.click(TOPO.phoneDUT,WidgetPage.TEST_ID,ClickType.NORMAL);
        int index[] = {0,1,2};
        Widget.clickByClass(TOPO.phoneDUT,WidgetPage.TEST_CLASSNAME_LOADING,index,ClickType.NORMAL);
        Common.wait(TOPO.phoneDUT,10);
        Common.goBack(TOPO.phoneDUT);

        logger.info("4.点击“按钮” ");
        Widget.click(TOPO.phoneDUT,WidgetPage.BUTTONS,ClickType.NORMAL);
        //列表
        Widget.clickSimilarNodeByBatch(TOPO.phoneDUT,WidgetPage.TEST_CLASSNAME_BUTTONS,5,ClickType.NORMAL);
        Common.wait(TOPO.phoneDUT,2);
        // 中按钮
        Widget.clickByText(TOPO.phoneDUT,"中按钮",ClickType.NORMAL);
        Widget.clickByText(TOPO.phoneDUT,"按钮",ClickType.NORMAL);
        Widget.clickByText(TOPO.phoneDUT,"次级按钮",ClickType.NORMAL);
        //大按钮
        Widget.clickByText(TOPO.phoneDUT,"大按钮",ClickType.NORMAL);
        Widget.clickByText(TOPO.phoneDUT,"主要按钮",ClickType.NORMAL);
        //双按钮
        Widget.clickByText(TOPO.phoneDUT,"双按钮",ClickType.NORMAL);
        Widget.clickByText(TOPO.phoneDUT,"按钮文案",0,ClickType.NORMAL);
        Common.wait(TOPO.phoneDUT,2);
        Widget.clickByText(TOPO.phoneDUT,"按钮文案",1,ClickType.NORMAL);
        Common.goBack(TOPO.phoneDUT);



        logger.info("5.点击 “快速滑动” ");
        Widget.click(TOPO.phoneDUT,WidgetPage.SWIPE_QUICK,ClickType.NORMAL);
        Widget.scrollDownToBottom(TOPO.phoneDUT);
        Common.wait(TOPO.phoneDUT,2);
        Common.goBack(TOPO.phoneDUT);




        return true;


    }

    public static void main(String[] args) {
        new NEARXDEMO_01WIDGET_014().run(args);
    }
}
