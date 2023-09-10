<!-- <script>
  import Covid from "./components/Covid.vue"

 
  export default {
    name: 'App',
    components: {
      Covid,
    }
 }
</script> -->
<script setup>
  import PlayIcon from "./icons/play-1000.svg";
  import SearchIcon from "./icons/searchicon.svg";
  import ListIcon from "./icons/list.svg";
  import FlagIcon from "./icons/flag.svg";
  import ReportIcon from "./icons/report.svg";
  import TowerIcon from "./icons/tower.svg";
  import DashboardIcon from "./icons/dashboard.svg";
  import SettingsIcon from "./icons/setting.svg";
  import SendIcon from "./icons/send.svg";
  import ReceiveIcon from "./icons/receive.svg";
  import DoughnutChart from "./charts/doughnut.svg";
  import { TabGroup, TabList, Tab, TabPanels, TabPanel } from '@headlessui/vue'

  
  const menu = [
    { name: "儀表板", icon: DashboardIcon },
    { name: "資產管理", icon: ListIcon },
    { name: "GCB管理", icon: FlagIcon },
    { name: "VANS管裡", icon: TowerIcon },
    { name: "報表管理", icon: ReportIcon },
    { name: "任務管理", icon: PlayIcon },
    { name: "排程管理", icon: PlayIcon },
    { name: "搜尋", icon: SearchIcon },
    { name: "設定", icon: SettingsIcon },
  ];

  const assets_report=[
    {
      
      report:4,
      unreport:2366,
      th_report:2348,
    }
  ];
  const gcb_agentTrustSiteInfo=[
  {
                siteName: "http://10.70.4.202",
                userCoun: 1
            },
            {
                siteName: "https://10.70.4.202",
                userCoun: 1
            },
            {
                siteName: "http://*.lts.fia.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://edit.cyhg.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://edit.lts.fia.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://edittest.cyhg.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://edittest.lts.fia.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://fontupdate.fia.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://stspiw19.fia.gov.tw",
                userCoun: 1
            },
            {
                siteName: "*.lts.fia.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://sso.lts.fia.gov.tw",
                userCoun: 1
            },
            {
                siteName: "web45n",
                userCoun: 1
            },
            {
                siteName: "https://*.lts.fia.gov.tw",
                userCoun: 7
            },
            {
                siteName: "10.7.171.158",
                userCoun: 1
            },
            {
                siteName: "https://js.monitor.azure.com",
                userCoun: 1
            },
            {
                siteName: "https://edgefrecdn.azureedge.net",
                userCoun: 1
            },
            {
                siteName: "https://2542116.fls.doubleclick.net",
                userCoun: 2
            },
            {
                siteName: "https://www.google-analytics.com",
                userCoun: 3
            },
            {
                siteName: "https://clients1.google.com",
                userCoun: 1
            },
            {
                siteName: "https://www.google.com",
                userCoun: 3
            },
            {
                siteName: "https://www.googleadservices.com",
                userCoun: 2
            },
            {
                siteName: "https://www.googletagmanager.com",
                userCoun: 3
            },
            {
                siteName: "https://www.gstatic.com",
                userCoun: 3
            },
            {
                siteName: "https://*.microsoft.com",
                userCoun: 33
            },
            {
                siteName: "http://*.technet.microsoft.com",
                userCoun: 58
            },
            {
                siteName: "https://*.update.microsoft.com",
                userCoun: 105
            },
            {
                siteName: "https://*.windowsupdate.microsoft.com",
                userCoun: 46
            },
            {
                siteName: "http://go.microsoft.com",
                userCoun: 63
            },
            {
                siteName: "https://microsoftedgewelcome.microsoft.com",
                userCoun: 1
            },
            {
                siteName: "http://msdn.microsoft.com",
                userCoun: 61
            },
            {
                siteName: "https://oca.microsoft.com",
                userCoun: 46
            },
            {
                siteName: "http://support.microsoft.com",
                userCoun: 60
            },
            {
                siteName: "http://technet.microsoft.com",
                userCoun: 60
            },
            {
                siteName: "https://update.microsoft.com",
                userCoun: 46
            },
            {
                siteName: "https://windowsupdate.microsoft.com",
                userCoun: 46
            },
            {
                siteName: "http://www.microsoft.com",
                userCoun: 60
            },
            {
                siteName: "http://runonce.msn.com",
                userCoun: 64
            },
            {
                siteName: "http://windowsupdate.com",
                userCoun: 64
            },
            {
                siteName: "https://125.227.239.179",
                userCoun: 1
            },
            {
                siteName: "*.caa.gov.tw",
                userCoun: 6
            },
            {
                siteName: "192.168.116.*",
                userCoun: 4
            },
            {
                siteName: "210.241.93.*",
                userCoun: 4
            },
            {
                siteName: "http://edoc",
                userCoun: 4
            },
            {
                siteName: "http://edoc1",
                userCoun: 4
            },
            {
                siteName: "http://EDOC2",
                userCoun: 4
            },
            {
                siteName: "http://EDOC3",
                userCoun: 4
            },
            {
                siteName: "https://172.16.0.6",
                userCoun: 4
            },
            {
                siteName: "https://172.16.0.7",
                userCoun: 4
            },
            {
                siteName: "https://172.16.0.94",
                userCoun: 4
            },
            {
                siteName: "https://172.16.0.110",
                userCoun: 4
            },
            {
                siteName: "https://172.16.0.121",
                userCoun: 4
            },
            {
                siteName: "https://172.16.50.6",
                userCoun: 4
            },
            {
                siteName: "https://172.16.50.7",
                userCoun: 4
            },
            {
                siteName: "https://192.168.115.94",
                userCoun: 4
            },
            {
                siteName: "https://192.168.115.110",
                userCoun: 4
            },
            {
                siteName: "https://192.168.115.121",
                userCoun: 4
            },
            {
                siteName: "https://192.168.116.5",
                userCoun: 4
            },
            {
                siteName: "https://192.168.116.15",
                userCoun: 4
            },
            {
                siteName: "https://192.168.116.25",
                userCoun: 4
            },
            {
                siteName: "https://172.16.48.7",
                userCoun: 4
            },
            {
                siteName: "cpa.gov.tw",
                userCoun: 116
            },
            {
                siteName: "https://dgpa.gov.tw",
                userCoun: 15
            },
            {
                siteName: "EDOC",
                userCoun: 3
            },
            {
                siteName: "EDOC1",
                userCoun: 3
            },
            {
                siteName: "https://aiss.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://anwsvpn.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://aoaws.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "http://asset.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://charge.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://filecloud.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://mail.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://ms1.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://officescan.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://web3.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://www.anws.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://eip.caa.gov.tw",
                userCoun: 5
            },
            {
                siteName: "https://eatm.ctbcbank.com",
                userCoun: 3
            },
            {
                siteName: "https://www.ctbcbank.com",
                userCoun: 3
            },
            {
                siteName: "http://winsicld3.cwb.gov.tw",
                userCoun: 3
            },
            {
                siteName: "http://winsicld4.cwb.gov.tw",
                userCoun: 3
            },
            {
                siteName: "http://www.dgbas.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://ecpa.dgpa.gov.tw",
                userCoun: 118
            },
            {
                siteName: "https://lifelonglearn.dgpa.gov.tw",
                userCoun: 4
            },
            {
                siteName: "https://pdu.dgpa.gov.tw",
                userCoun: 106
            },
            {
                siteName: "https://webhr.dgpa.gov.tw",
                userCoun: 106
            },
            {
                siteName: "https://cas.ebas.gov.tw",
                userCoun: 104
            },
            {
                siteName: "http://edoc2",
                userCoun: 3
            },
            {
                siteName: "http://edoc3",
                userCoun: 3
            },
            {
                siteName: "https://elearning.taipei",
                userCoun: 3
            },
            {
                siteName: "http://hikey.hinet.net",
                userCoun: 3
            },
            {
                siteName: "https://elearn.hrd.gov.tw",
                userCoun: 4
            },
            {
                siteName: "https://elearning.hrd.gov.tw",
                userCoun: 13
            },
            {
                siteName: "https://kcg.elearn.hrd.gov.tw",
                userCoun: 3
            },
            {
                siteName: "http://www.hrd.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://id.taipei",
                userCoun: 3
            },
            {
                siteName: "http://moica.nat.gov.tw",
                userCoun: 106
            },
            {
                siteName: "https://inquiry.nccc.com.tw",
                userCoun: 274
            },
            {
                siteName: "https://web.pcc.gov.tw",
                userCoun: 13
            },
            {
                siteName: "http://web2test.pcc.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://ipost.post.gov.tw",
                userCoun: 3
            },
            {
                siteName: "https://webatm.post.gov.tw",
                userCoun: 4
            },
            {
                siteName: "https://www.ris.gov.tw",
                userCoun: 4
            },
            {
                siteName: "http://172.16.50.6",
                userCoun: 3
            },
            {
                siteName: "http://210.241.93.7",
                userCoun: 3
            },
            {
                siteName: "http://10.131.11.19",
                userCoun: 3
            },
            {
                siteName: "http://10.131.11.32",
                userCoun: 3
            },
            {
                siteName: "http://172.16.50.48",
                userCoun: 3
            },
            {
                siteName: "https://10.120.10.109",
                userCoun: 3
            },
            {
                siteName: "http://10.131.10.92",
                userCoun: 3
            },
            {
                siteName: "http://172.16.50.7",
                userCoun: 3
            },
            {
                siteName: "http://asset.anws.gov.tw/Login.aspx",
                userCoun: 3
            },
            {
                siteName: "https://filecloud.anws.gov.tw/",
                userCoun: 3
            },
            {
                siteName: "https://webatm.post.gov.tw/postatm/index1.jsp",
                userCoun: 3
            },
            {
                siteName: "https://eatm.ctbcbank.com/WebATM/login.jsp",
                userCoun: 3
            },
            {
                siteName: "http://10.131.11.19/AnwsSal/WEB/indexLogin.aspx",
                userCoun: 3
            },
            {
                siteName: "http://10.131.11.32/AnwsSt/Web/indexLogin.aspx",
                userCoun: 3
            },
            {
                siteName: "https://ipost.post.gov.tw/web/CSController",
                userCoun: 3
            },
            {
                siteName: "http://172.16.50.48/login.aspx",
                userCoun: 3
            },
            {
                siteName: "http://10.131.10.92/Login.aspx",
                userCoun: 3
            },
            {
                siteName: "https://www.ctbcbank.com/CTCBPortalWeb/toPage?id=TW_RB_TX_ebank_110101",
                userCoun: 3
            },
            {
                siteName: "http://www.hrd.gov.tw/",
                userCoun: 3
            },
            {
                siteName: "http://winsicld3.cwb.gov.tw/ovd/",
                userCoun: 3
            },
            {
                siteName: "https://cas.ebas.gov.tw/ebas-cas/login?service=http%3A%2F%2Febas.gov.tw%2Flogin.do",
                userCoun: 3
            },
            {
                siteName: "https://webhr.dgpa.gov.tw/web/",
                userCoun: 3
            },
            {
                siteName: "http://www.dgbas.gov.tw/mp.asp?mp=1",
                userCoun: 3
            },
            {
                siteName: "http://hikey.hinet.net/",
                userCoun: 3
            },
            {
                siteName: "https://lifelonglearn.dgpa.gov.tw/Default.aspx",
                userCoun: 3
            },
            {
                siteName: "https://officescan.anws.gov.tw:4343/officescan",
                userCoun: 3
            },
            {
                siteName: "https://elearning.hrd.gov.tw/inedx.php",
                userCoun: 3
            },
            {
                siteName: "https://elearning.taipei/mpage/",
                userCoun: 3
            },
            {
                siteName: "http://winsicld4.cwb.gov.tw/ovd/",
                userCoun: 3
            },
            {
                siteName: "http://web.pcc.gov.tw",
                userCoun: 10
            },
            {
                siteName: "https://elearn.hrd.gov.tw/mooc/index.php",
                userCoun: 3
            },
            {
                siteName: "https://id.taipei/tpcd/login",
                userCoun: 3
            },
            {
                siteName: "http://hikey.hinet.net/raservice/renew.jsp",
                userCoun: 3
            },
            {
                siteName: "https://kcg.elearn.hrd.gov.tw/mooc/index.php",
                userCoun: 3
            },
            {
                siteName: "dgpa.gov.tw",
                userCoun: 384
            },
            {
                siteName: "http://localhost",
                userCoun: 1
            },
            {
                siteName: "https://moi.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://cash.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://crowdfund.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://eservice.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://fortune.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://futures1.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://futures8.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://icetech.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://masterlink.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://megatime.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://wls.megatime.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://moneydj.com",
                userCoun: 1
            },
            {
                siteName: "https://smartorder.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://twca.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://w168.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://wlf.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://wls-consulting.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://wls.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://trade.wls.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://www16.masterlink.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://xq.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://192.168.1.224",
                userCoun: 1
            },
            {
                siteName: "https://www.microsoft.com",
                userCoun: 2
            },
            {
                siteName: "https://dragonsoft2021-files.sharepoint.com",
                userCoun: 18
            },
            {
                siteName: "https://dragonsoft2021-myfiles.sharepoint.com",
                userCoun: 18
            },
            {
                siteName: "https://victoriaca-files.sharepoint.com",
                userCoun: 3
            },
            {
                siteName: "https://victoriaca-myfiles.sharepoint.com",
                userCoun: 3
            },
            {
                siteName: "https://tw.yahoo.com",
                userCoun: 3
            },
            {
                siteName: "www.tyh.com.tw://10443",
                userCoun: 2
            },
            {
                siteName: "https://www.tyh.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://www.jingyaodoc.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://192.168.1.240",
                userCoun: 1
            },
            {
                siteName: "http://211.21.202.5",
                userCoun: 1
            },
            {
                siteName: "https://msedge.sf.dl.delivery.mp.microsoft.com",
                userCoun: 1
            },
            {
                siteName: "https://eysc.ey.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://eywebstorage.ey.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.update.microsoft.com",
                userCoun: 25
            },
            {
                siteName: "http://*.windowsupdate.microsoft.com",
                userCoun: 25
            },
            {
                siteName: "http://oca.microsoft.com",
                userCoun: 25
            },
            {
                siteName: "http://update.microsoft.com",
                userCoun: 25
            },
            {
                siteName: "http://windowsupdate.microsoft.com",
                userCoun: 25
            },
            {
                siteName: "https://eadm.ncku.edu.tw",
                userCoun: 1
            },
            {
                siteName: "https://eli.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://ncku365-files.sharepoint.com",
                userCoun: 1
            },
            {
                siteName: "https://ncku365-myfiles.sharepoint.com",
                userCoun: 1
            },
            {
                siteName: "https://www.esunbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "e-land.gov.tw",
                userCoun: 310
            },
            {
                siteName: "https://ntp.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://doc2-1.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://doc2-2.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://doc2-3.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://doc2-4.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://doc2-manage.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://doc2-school.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://property.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://172.18.*.*",
                userCoun: 2
            },
            {
                siteName: "bli.gov.tw",
                userCoun: 2
            },
            {
                siteName: "boca.gov.tw",
                userCoun: 2
            },
            {
                siteName: "bot.com.tw",
                userCoun: 373
            },
            {
                siteName: "cathaybk.com.tw",
                userCoun: 2
            },
            {
                siteName: "cp.gov.tw",
                userCoun: 371
            },
            {
                siteName: "ctbcbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://exam.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "esunbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "hncb.com.tw",
                userCoun: 2
            },
            {
                siteName: "hrd.gov.tw",
                userCoun: 4
            },
            {
                siteName: "landbank.com.tw",
                userCoun: 4
            },
            {
                siteName: "megabank.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://mocs.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://iocs.mocs.gov.tw",
                userCoun: 112
            },
            {
                siteName: "*.land.moi.gov.tw",
                userCoun: 4
            },
            {
                siteName: "https://glir.land.moi.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://moutzyy.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://www.myatm.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://www.mybank.com.tw",
                userCoun: 4
            },
            {
                siteName: "nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "*.etax.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "*.gcis.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://etw.etax.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://gcis.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://ncert.gcis.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "nhi.gov.tw",
                userCoun: 273
            },
            {
                siteName: "https://cloudicweb.nhi.gov.tw",
                userCoun: 2
            },
            {
                siteName: "ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://*.tax.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://cloud.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://clout.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://doc2-5.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "oas.bas.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "pcc.gov.tw",
                userCoun: 373
            },
            {
                siteName: "post.gov.tw",
                userCoun: 271
            },
            {
                siteName: "tcb-bank.com.tw",
                userCoun: 2
            },
            {
                siteName: "tcfhc.com.tw",
                userCoun: 2
            },
            {
                siteName: "tctb.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://web.tctb.gov.tw",
                userCoun: 2
            },
            {
                siteName: "yahoo.com",
                userCoun: 2
            },
            {
                siteName: "http://10.46.4.225",
                userCoun: 2
            },
            {
                siteName: "https://163.29.250.3",
                userCoun: 2
            },
            {
                siteName: "http://10.46.83.59",
                userCoun: 2
            },
            {
                siteName: "https://10.46.7.182",
                userCoun: 2
            },
            {
                siteName: "https://10.46.4.137",
                userCoun: 2
            },
            {
                siteName: "172.18.*.*",
                userCoun: 2
            },
            {
                siteName: "*.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "*.pcc.gov.tw",
                userCoun: 374
            },
            {
                siteName: "*.dgpa.gov.tw",
                userCoun: 375
            },
            {
                siteName: "*.nhi.gov.tw",
                userCoun: 4
            },
            {
                siteName: "*.mocs.gov.tw",
                userCoun: 372
            },
            {
                siteName: "*.hrd.gov.tw",
                userCoun: 4
            },
            {
                siteName: "*.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "*.bli.gov.tw",
                userCoun: 2
            },
            {
                siteName: "*.cpa.gov.tw",
                userCoun: 103
            },
            {
                siteName: "*.tcb-bank.com.tw",
                userCoun: 2
            },
            {
                siteName: "*.bot.com.tw",
                userCoun: 374
            },
            {
                siteName: "*.landbank.com.tw",
                userCoun: 4
            },
            {
                siteName: "*.hncb.com.tw",
                userCoun: 2
            },
            {
                siteName: "*.cathaybk.com.tw",
                userCoun: 2
            },
            {
                siteName: "*.esunbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "*.ctbcbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "*.post.gov.tw",
                userCoun: 2
            },
            {
                siteName: "*.cp.gov.tw",
                userCoun: 372
            },
            {
                siteName: "*.tcfhc.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://etw.etax.nat.gov.tw/etwn/sso/login",
                userCoun: 2
            },
            {
                siteName: "*.megabank.com.tw",
                userCoun: 2
            },
            {
                siteName: "ecpa.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "10.46.36.10",
                userCoun: 2
            },
            {
                siteName: "10.46.32.20",
                userCoun: 2
            },
            {
                siteName: "http://cloud.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "*.boca.gov.tw",
                userCoun: 2
            },
            {
                siteName: "*.tctb.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://ncert.gcis.nat.gov.tw/moea_portal/portal_job.htm",
                userCoun: 2
            },
            {
                siteName: "https://163.29.250.3:19991",
                userCoun: 2
            },
            {
                siteName: "*.yahoo.com",
                userCoun: 2
            },
            {
                siteName: "https://ecpa.dgpa.gov.tw/",
                userCoun: 4
            },
            {
                siteName: "https://www.myatm.com.tw/",
                userCoun: 2
            },
            {
                siteName: "https://www.mybank.com.tw/",
                userCoun: 2
            },
            {
                siteName: "http://*.tax.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://clout.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://cloudicweb.nhi.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "https://iocs.mocs.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "http://moutzyy.com.tw/mystery/",
                userCoun: 2
            },
            {
                siteName: "gcis.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://163.29.250.3:19991/",
                userCoun: 2
            },
            {
                siteName: "https://10.46.4.137:8015",
                userCoun: 2
            },
            {
                siteName: "https://exam.dgpa.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "edesk.bli.gov.tw",
                userCoun: 271
            },
            {
                siteName: "cib.gov.tw",
                userCoun: 269
            },
            {
                siteName: "csptc.gov.tw",
                userCoun: 269
            },
            {
                siteName: "cy.gov.tw",
                userCoun: 269
            },
            {
                siteName: "dgbas.gov.tw",
                userCoun: 369
            },
            {
                siteName: "ebas.gov.tw",
                userCoun: 369
            },
            {
                siteName: "fisc.com.tw",
                userCoun: 268
            },
            {
                siteName: "fnp.gov.tw",
                userCoun: 268
            },
            {
                siteName: "vrs.hinet.net",
                userCoun: 269
            },
            {
                siteName: "mocs.gov.tw",
                userCoun: 369
            },
            {
                siteName: "mohw.gov.tw",
                userCoun: 268
            },
            {
                siteName: "moi.gov.tw",
                userCoun: 268
            },
            {
                siteName: "moj.gov.tw",
                userCoun: 271
            },
            {
                siteName: "pdis.moj.gov.tw",
                userCoun: 271
            },
            {
                siteName: "gtlscaweb.nat.gov.tw",
                userCoun: 269
            },
            {
                siteName: "net.tax.nat.gov.tw",
                userCoun: 269
            },
            {
                siteName: "npa.gov.tw",
                userCoun: 281
            },
            {
                siteName: "statis.eportal.npa.gov.tw",
                userCoun: 269
            },
            {
                siteName: "cyhr.sfaa.gov.tw",
                userCoun: 269
            },
            {
                siteName: "wda.gov.tw",
                userCoun: 268
            },
            {
                siteName: "*.e-land.gov.tw",
                userCoun: 269
            },
            {
                siteName: "10.136.10.201",
                userCoun: 269
            },
            {
                siteName: "210.69.149.24",
                userCoun: 269
            },
            {
                siteName: "*.npa.gov.tw",
                userCoun: 269
            },
            {
                siteName: "*.cib.gov.tw",
                userCoun: 269
            },
            {
                siteName: "*.fnp.gov.tw",
                userCoun: 269
            },
            {
                siteName: "10.150.18.14",
                userCoun: 269
            },
            {
                siteName: "10.136.1.22",
                userCoun: 269
            },
            {
                siteName: "*.moi.gov.tw",
                userCoun: 269
            },
            {
                siteName: "*.fisc.com.tw",
                userCoun: 269
            },
            {
                siteName: "10.150.101.106",
                userCoun: 269
            },
            {
                siteName: "10.136.14.14",
                userCoun: 269
            },
            {
                siteName: "*.wda.gov.tw",
                userCoun: 269
            },
            {
                siteName: "59.125.186.133/mlpo",
                userCoun: 269
            },
            {
                siteName: "10.136.8.243",
                userCoun: 269
            },
            {
                siteName: "10.136.8.244",
                userCoun: 269
            },
            {
                siteName: "10.136.8.246",
                userCoun: 269
            },
            {
                siteName: "*.mohw.gov.tw",
                userCoun: 269
            },
            {
                siteName: "10.136.4.13",
                userCoun: 269
            },
            {
                siteName: "210.69.148.133",
                userCoun: 269
            },
            {
                siteName: "*.ebas.gov.tw",
                userCoun: 269
            },
            {
                siteName: "*.dgbas.gov.tw",
                userCoun: 370
            },
            {
                siteName: "163.29.131.219",
                userCoun: 269
            },
            {
                siteName: "http://vrs.hinet.net",
                userCoun: 12
            },
            {
                siteName: "https://oe2.eportal.npa.gov.tw",
                userCoun: 4
            },
            {
                siteName: "http://10.136.10.217",
                userCoun: 6
            },
            {
                siteName: "ckd.ap.cib.gov.tw",
                userCoun: 14
            },
            {
                siteName: "http://ecpa.cpa.gov.tw",
                userCoun: 118
            },
            {
                siteName: "www.cib.gov.tw",
                userCoun: 17
            },
            {
                siteName: "https://vrs.hinet.net",
                userCoun: 8
            },
            {
                siteName: "localhost",
                userCoun: 10
            },
            {
                siteName: "http://webcompanion.com",
                userCoun: 9
            },
            {
                siteName: "http://*.ap.cib.gov.tw",
                userCoun: 17
            },
            {
                siteName: "http://*.cib.gov.tw",
                userCoun: 16
            },
            {
                siteName: "https://*.nhi.gov.tw",
                userCoun: 4
            },
            {
                siteName: "http://e-learning.cdc.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://docs.e-land.gov.tw",
                userCoun: 13
            },
            {
                siteName: "https://i3-1.eportal.npa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://km.eportal.npa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://tm.eportal.npa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://10.10.4.116",
                userCoun: 2
            },
            {
                siteName: "https://pwm.trendmicro.com",
                userCoun: 1
            },
            {
                siteName: "https://eatm.landbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://ebank.landbank.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://iatm.landbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://ibank.landbank.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://mybank.landbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://mybankt.landbank.com.tw",
                userCoun: 2
            },
            {
                siteName: "http://www.landbank.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://eatm.landbankt.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://iatm.landbankt.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://mybank.landbankt.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://localhost",
                userCoun: 5
            },
            {
                siteName: "https://10.253.21.126",
                userCoun: 2
            },
            {
                siteName: "https://km.e-land.gov.tw",
                userCoun: 19
            },
            {
                siteName: "https://ilcpb.ivs.hinet.net",
                userCoun: 1
            },
            {
                siteName: "httpsï¼š",
                userCoun: 1
            },
            {
                siteName: "https://cib.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.ap.cib.gov.tw",
                userCoun: 1
            },
            {
                siteName: "crd.ap.cib.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://cibv00nt01",
                userCoun: 1
            },
            {
                siteName: "http://www.cns11643.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://mail.e-land.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://www02.eyny.com",
                userCoun: 1
            },
            {
                siteName: "http://www.google.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://ucam.hinet.net",
                userCoun: 2
            },
            {
                siteName: "https://c3i.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://idm.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://iweb.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://ris.eportal.npa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://sec.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://sn.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://ssp.eportal.npa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://www.senao.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://tw.news.yahoo.com",
                userCoun: 1
            },
            {
                siteName: "http://www.youtube.com",
                userCoun: 1
            },
            {
                siteName: "http://10.150.9.76",
                userCoun: 1
            },
            {
                siteName: "http://10.150.31.115",
                userCoun: 1
            },
            {
                siteName: "http://10.136.4.13",
                userCoun: 4
            },
            {
                siteName: "http://10.136.3.219",
                userCoun: 1
            },
            {
                siteName: "http://10.150.164.114",
                userCoun: 1
            },
            {
                siteName: "https://10.150.*.*",
                userCoun: 1
            },
            {
                siteName: "http://10.136.14.*",
                userCoun: 17
            },
            {
                siteName: "http://recsrv/",
                userCoun: 17
            },
            {
                siteName: "http://km.cib.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://eip.e-land.gov.tw",
                userCoun: 13
            },
            {
                siteName: "http://capital.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://capitalfutures.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://foreign.capitalfutures.com.tw/ap/cominfo.asp",
                userCoun: 2
            },
            {
                siteName: "http://*.capitalfutures.*.capital.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://moneydj.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://net.tax.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://netap.tax.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://idp.eportal.npa.gov.tw",
                userCoun: 5
            },
            {
                siteName: "https://nnb.tbb.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://nnbt.tbb.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://10.16.22.17",
                userCoun: 1
            },
            {
                siteName: "https://capital.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://kmlogin.cib.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://esp.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://dvpc.mohw.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://10.136.10.201",
                userCoun: 2
            },
            {
                siteName: "https://docs.google.com",
                userCoun: 1
            },
            {
                siteName: "https://stmarysstclairorg-files.sharepoint.com",
                userCoun: 1
            },
            {
                siteName: "https://stmarysstclairorg-myfiles.sharepoint.com",
                userCoun: 1
            },
            {
                siteName: "https://tangxine-files.sharepoint.com",
                userCoun: 2
            },
            {
                siteName: "https://tangxine-myfiles.sharepoint.com",
                userCoun: 2
            },
            {
                siteName: "http://10.136.14.14",
                userCoun: 8
            },
            {
                siteName: "http://ba.org.tw",
                userCoun: 1
            },
            {
                siteName: "https://ebank.bot.com.tw",
                userCoun: 102
            },
            {
                siteName: "http://ebill.ba.org.tw",
                userCoun: 1
            },
            {
                siteName: "http://fisc.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://paytax.nat.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://mybank.com.tw",
                userCoun: 2
            },
            {
                siteName: "http://10.136.1.10",
                userCoun: 3
            },
            {
                siteName: "https://sakuranulio-files.sharepoint.com",
                userCoun: 1
            },
            {
                siteName: "https://sakuranulio-myfiles.sharepoint.com",
                userCoun: 1
            },
            {
                siteName: "https://hr.e-land.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://10.136.14.31",
                userCoun: 1
            },
            {
                siteName: "docs.e-land.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://10.136.14.2",
                userCoun: 1
            },
            {
                siteName: "http://10.136.14.3",
                userCoun: 1
            },
            {
                siteName: "docs.gov.tw",
                userCoun: 2
            },
            {
                siteName: "www.e-land.gov.tw",
                userCoun: 1
            },
            {
                siteName: "*.ap.cib.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://tssco.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.sinopac.com",
                userCoun: 1
            },
            {
                siteName: "https://caweb.esunsec.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://onlineaccount.esunsec.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://e-land.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://10.1.31.*",
                userCoun: 1
            },
            {
                siteName: "http://*.Wondershare.com",
                userCoun: 1
            },
            {
                siteName: "https://1634ecajcaeduau-files.sharepoint.com",
                userCoun: 1
            },
            {
                siteName: "https://1634ecajcaeduau-myfiles.sharepoint.com",
                userCoun: 1
            },
            {
                siteName: "https://m2.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://10.136.8.57",
                userCoun: 1
            },
            {
                siteName: "http://10.136.33.109",
                userCoun: 1
            },
            {
                siteName: "https://ecpa.cpa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://pfiles.tax.nat.gov.tw",
                userCoun: 102
            },
            {
                siteName: "https://rtn.tax.nat.gov.tw",
                userCoun: 102
            },
            {
                siteName: "https://vpfiles.tax.nat.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://vrtn.tax.nat.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://www.youtube.com",
                userCoun: 1
            },
            {
                siteName: "https://10.136.14.14",
                userCoun: 1
            },
            {
                siteName: "https://10.136.*.*",
                userCoun: 1
            },
            {
                siteName: "https://serv.e-land.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://center.elearn.hrd.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://oa2.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://oacentral.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://iweb2.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://10.136.49.200",
                userCoun: 1
            },
            {
                siteName: "http://xmsecu.com",
                userCoun: 1
            },
            {
                siteName: "http://192.168.1.15",
                userCoun: 1
            },
            {
                siteName: "sinica.edu.tw",
                userCoun: 1
            },
            {
                siteName: "https://www.sinica.edu.tw",
                userCoun: 1
            },
            {
                siteName: "https://edoc.scr.ntnu.edu.tw",
                userCoun: 3
            },
            {
                siteName: "https://o365ntnu-files.sharepoint.com",
                userCoun: 2
            },
            {
                siteName: "https://o365ntnu-myfiles.sharepoint.com",
                userCoun: 2
            },
            {
                siteName: "https://140.122.66.236",
                userCoun: 3
            },
            {
                siteName: "https://140.122.64.4",
                userCoun: 3
            },
            {
                siteName: "ebacnk.bot.com.tw",
                userCoun: 101
            },
            {
                siteName: "https://school.bot.com.tw",
                userCoun: 102
            },
            {
                siteName: "https://www.cp.gov.tw",
                userCoun: 102
            },
            {
                siteName: "https://pdu.cpa.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://acms.csptc.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://cgba.dgbas.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://dga3.dgbas.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://medal.dgpa.gov.tw",
                userCoun: 102
            },
            {
                siteName: "pdu.dgpa.gov.tw",
                userCoun: 103
            },
            {
                siteName: "https://web2.dgpa.gov.tw",
                userCoun: 101
            },
            {
                siteName: "*.cpckm.ekm.org.tw",
                userCoun: 101
            },
            {
                siteName: "www.entrust.com.tw",
                userCoun: 101
            },
            {
                siteName: "eatm.firstbank.com.tw",
                userCoun: 101
            },
            {
                siteName: "http://gp.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://cs.learn.hinet.net",
                userCoun: 101
            },
            {
                siteName: "lms.learn.hinet.net",
                userCoun: 101
            },
            {
                siteName: "elearning.hrd.gov.tw",
                userCoun: 103
            },
            {
                siteName: "http://ivod.ly.gov.tw",
                userCoun: 102
            },
            {
                siteName: "https://megabank.com.tw",
                userCoun: 101
            },
            {
                siteName: "www.megabank.com.tw",
                userCoun: 103
            },
            {
                siteName: "iocs.mocs.gov.tw",
                userCoun: 103
            },
            {
                siteName: "http://mof.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://eip.mof.gov.tw",
                userCoun: 101
            },
            {
                siteName: "eip2.mof.gov.tw",
                userCoun: 101
            },
            {
                siteName: "museum.mof.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://news.mof.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://pts.mofnpb.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://pri.land.moi.gov.tw",
                userCoun: 101
            },
            {
                siteName: "law.moj.gov.tw",
                userCoun: 101
            },
            {
                siteName: "mojeaac.moj.gov.tw",
                userCoun: 103
            },
            {
                siteName: "https://cert.gcis.nat.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://cyey.nat.gov.tw",
                userCoun: 101
            },
            {
                siteName: "gcaweb.nat.gov.tw",
                userCoun: 103
            },
            {
                siteName: "http://gcis.nat.gov.tw",
                userCoun: 108
            },
            {
                siteName: "http://gpmnet.nat.gov.tw",
                userCoun: 102
            },
            {
                siteName: "rtn.tax.nat.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://www.tax.nat.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://eservice.nhi.gov.tw",
                userCoun: 102
            },
            {
                siteName: "http://nta-dvr",
                userCoun: 101
            },
            {
                siteName: "*.cto.nta.gov.tw",
                userCoun: 101
            },
            {
                siteName: "aac.cto.nta.gov.tw",
                userCoun: 101
            },
            {
                siteName: "certgcis.nta.gov.tw",
                userCoun: 101
            },
            {
                siteName: "ctowi-1.nta.gov.tw",
                userCoun: 101
            },
            {
                siteName: "ctowp-1.nta.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://gaze.nta.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://ntafilesr.nta.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://prsbedi.prsb.gov.tw",
                userCoun: 101
            },
            {
                siteName: "elearning.rad.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://welearning.taipei.gov.tw",
                userCoun: 101
            },
            {
                siteName: "wftp.taipower.com.tw",
                userCoun: 101
            },
            {
                siteName: "tradevan.com.tw",
                userCoun: 101
            },
            {
                siteName: "https://portal.tradevan.com.tw",
                userCoun: 101
            },
            {
                siteName: "trdo.gov.tw",
                userCoun: 101
            },
            {
                siteName: "https://www.trdo.gov.tw",
                userCoun: 108
            },
            {
                siteName: "www.ttb.gov",
                userCoun: 101
            },
            {
                siteName: "https://vtaiwan.tw",
                userCoun: 101
            },
            {
                siteName: "http://163.29.131.241",
                userCoun: 101
            },
            {
                siteName: "http://192.168.120.215",
                userCoun: 101
            },
            {
                siteName: "https://10.1.16.225",
                userCoun: 101
            },
            {
                siteName: "https://172.25.106.22",
                userCoun: 101
            },
            {
                siteName: "https://202.173.38.34",
                userCoun: 101
            },
            {
                siteName: "*.mof.gov.tw",
                userCoun: 101
            },
            {
                siteName: "*.tradevan.com.tw",
                userCoun: 101
            },
            {
                siteName: "*.trdo.gov.tw",
                userCoun: 101
            },
            {
                siteName: "172.16.*.*",
                userCoun: 101
            },
            {
                siteName: "172.16.1.*",
                userCoun: 101
            },
            {
                siteName: "172.16.1.133",
                userCoun: 101
            },
            {
                siteName: "172.16.1.134",
                userCoun: 101
            },
            {
                siteName: "172.16.1.135",
                userCoun: 101
            },
            {
                siteName: "172.16.1.136",
                userCoun: 101
            },
            {
                siteName: "172.16.1.145",
                userCoun: 101
            },
            {
                siteName: "172.20.1.19",
                userCoun: 101
            },
            {
                siteName: "210.69.109.*",
                userCoun: 101
            },
            {
                siteName: "cas.ebas.gov.tw/*",
                userCoun: 101
            },
            {
                siteName: "cert.gcis.nat.gov.tw",
                userCoun: 101
            },
            {
                siteName: "cyey.nat.gov.tw",
                userCoun: 101
            },
            {
                siteName: "dga3.dgbas.gov.tw/*",
                userCoun: 101
            },
            {
                siteName: "dga3.dgbas.gov.tw/dga/*",
                userCoun: 101
            },
            {
                siteName: "ebas.gov.tw/*",
                userCoun: 101
            },
            {
                siteName: "gpmnet.nat.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://*.gp.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://*.mof.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://cgba.dgbas.gov.tw/",
                userCoun: 101
            },
            {
                siteName: "http://Cs.learn.hinet.net",
                userCoun: 101
            },
            {
                siteName: "http://cyey.nat.gov.tw/",
                userCoun: 101
            },
            {
                siteName: "http://dga3.dgbas.gov.tw/dga/index.jsp",
                userCoun: 101
            },
            {
                siteName: "http://gcis.nat.gov.tw/",
                userCoun: 101
            },
            {
                siteName: "http://gcis.nat.gov.tw/portal/portal_job.htm",
                userCoun: 101
            },
            {
                siteName: "http://gpmnet.nat.gov.tw/",
                userCoun: 101
            },
            {
                siteName: "http://www.cp.gov.tw",
                userCoun: 101
            },
            {
                siteName: "http://www.tax.nat.gov.tw/",
                userCoun: 101
            },
            {
                siteName: "https://*.megabank.com.tw/*",
                userCoun: 101
            },
            {
                siteName: "https://cas.ebas.gov.tw/*",
                userCoun: 101
            },
            {
                siteName: "https://cert.gcis.nat.gov.tw/*",
                userCoun: 101
            },
            {
                siteName: "https://ebank.bot.com.tw/ ",
                userCoun: 101
            },
            {
                siteName: "https://ecpa.dgpa.gov.tw/Member/Application#",
                userCoun: 101
            },
            {
                siteName: "https://eservice.nhi.gov.tw/*",
                userCoun: 101
            },
            {
                siteName: "https://iocs.mocs.gov.tw/portal/index.aspx",
                userCoun: 101
            },
            {
                siteName: "https://medal.dgpa.gov.tw/CAAMain2.aspx",
                userCoun: 101
            },
            {
                siteName: "https://news.mof.gov.tw/",
                userCoun: 101
            },
            {
                siteName: "https://prsbedi.prsb.gov.tw/*",
                userCoun: 101
            },
            {
                siteName: "https://school.bot.com.tw/*",
                userCoun: 101
            },
            {
                siteName: "https://vtaiwan.tw/#!/",
                userCoun: 101
            },
            {
                siteName: "https://web2.dgpa.gov.tw/cpaseql/index.aspx",
                userCoun: 101
            },
            {
                siteName: "https://www.megabank.com.tw/*",
                userCoun: 101
            },
            {
                siteName: "https://www.trdo.gov.tw/*",
                userCoun: 101
            },
            {
                siteName: "https:\\\\\\\\pdu.dgpa.gov.tw",
                userCoun: 101
            },
            {
                siteName: "pdu.dgpa.gov.tw/",
                userCoun: 101
            },
            {
                siteName: "http://firstbank.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://twse.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://firstbank.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://edoc.ntu.edu.tw",
                userCoun: 1
            },
            {
                siteName: "http://140.112.6.135",
                userCoun: 1
            },
            {
                siteName: "http://140.112.6.199",
                userCoun: 1
            },
            {
                siteName: "http://docs.aws.amazon.com",
                userCoun: 1
            },
            {
                siteName: "http://media.amazonwebservices.com",
                userCoun: 1
            },
            {
                siteName: "about://blank",
                userCoun: 3
            },
            {
                siteName: "https://d36cz9buwru1tt.cloudfront.net",
                userCoun: 1
            },
            {
                siteName: "https://aws.qualtrics.com",
                userCoun: 1
            },
            {
                siteName: "about://security_ScriptedSandbox64.exe",
                userCoun: 1
            },
            {
                siteName: "https://ap12",
                userCoun: 7
            },
            {
                siteName: "https://www.asuswebstorage.com",
                userCoun: 7
            },
            {
                siteName: "https://bot.com.tw",
                userCoun: 8
            },
            {
                siteName: "https://gnweb.bot.com.tw",
                userCoun: 7
            },
            {
                siteName: "https://enterbox.chiefappc.com",
                userCoun: 7
            },
            {
                siteName: "https://cpa.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://cpami.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://dgbas.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://cgba.dgbas.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://cgba6.dgbas.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://ebas.gov.tw",
                userCoun: 8
            },
            {
                siteName: "http://ey.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://inquery.ey.gov.tw",
                userCoun: 8
            },
            {
                siteName: "https://www.ey.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://calendar.google.com",
                userCoun: 7
            },
            {
                siteName: "https://*.moea.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://amsps1.intra.moea.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://dmz5.moea.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://nat.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://oa.moea.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://wgba.dgbas.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://efiling.judicial.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://dmz5.moea.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://emaster.moea.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://intra.mofa.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://moj.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://nat.gov.tw",
                userCoun: 10
            },
            {
                siteName: "https://*.gcis.nat.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://*.tax.nat.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://gpmnet.nat.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://web.gcis.nat.gov.tw",
                userCoun: 7
            },
            {
                siteName: "http://www.nat.gov.tw",
                userCoun: 7
            },
            {
                siteName: "https://nhi.gov.tw",
                userCoun: 8
            },
            {
                siteName: "https://ebank.taipeifubon.com.tw",
                userCoun: 7
            },
            {
                siteName: "https://stpc00601.taipower.com.tw",
                userCoun: 7
            },
            {
                siteName: "http://www.taipower.com.tw",
                userCoun: 7
            },
            {
                siteName: "http://172.16.1.17",
                userCoun: 7
            },
            {
                siteName: "http://172.16.1.108",
                userCoun: 7
            },
            {
                siteName: "http://172.16.1.104",
                userCoun: 7
            },
            {
                siteName: "http://172.16.1.251",
                userCoun: 7
            },
            {
                siteName: "http://172.16.1.109",
                userCoun: 7
            },
            {
                siteName: "https://210.69.121.111",
                userCoun: 7
            },
            {
                siteName: "https://210.69.121.112",
                userCoun: 7
            },
            {
                siteName: "https://210.69.121.113",
                userCoun: 7
            },
            {
                siteName: "https://210.69.121.114",
                userCoun: 7
            },
            {
                siteName: "https://210.69.121.115",
                userCoun: 7
            },
            {
                siteName: "https://210.69.121.116",
                userCoun: 7
            },
            {
                siteName: "http://172.16.1.120",
                userCoun: 7
            },
            {
                siteName: "https://210.241.69.227",
                userCoun: 7
            },
            {
                siteName: "http://172.16.1.140",
                userCoun: 7
            },
            {
                siteName: "https://exg.moea.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://exg.intra.moea.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://172.16.11.135",
                userCoun: 1
            },
            {
                siteName: "http://statistweb.cpami.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://172.16.1.43",
                userCoun: 1
            },
            {
                siteName: "https://2secure.itri.org.tw",
                userCoun: 2
            },
            {
                siteName: "https://sslvpn.itri.org.tw",
                userCoun: 2
            },
            {
                siteName: "https://pollution.epd.ntpc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://eip2.freeway.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://eip.freeway.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://10.50.0.64",
                userCoun: 1
            },
            {
                siteName: "http://10.50.0.30",
                userCoun: 1
            },
            {
                siteName: "https://s7.addthis.com",
                userCoun: 1
            },
            {
                siteName: "http://ajax.aspnetcdn.com",
                userCoun: 1
            },
            {
                siteName: "https://pcalsweb.cpc.org.tw",
                userCoun: 1
            },
            {
                siteName: "https://googleads.g.doubleclick.net",
                userCoun: 1
            },
            {
                siteName: "fmms.freeway.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://mem.gfx.ms",
                userCoun: 1
            },
            {
                siteName: "https://adservice.google.com",
                userCoun: 1
            },
            {
                siteName: "https://apis.google.com",
                userCoun: 1
            },
            {
                siteName: "https://adservice.google.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://pagead2.googlesyndication.com",
                userCoun: 1
            },
            {
                siteName: "https://www.googletagservices.com",
                userCoun: 1
            },
            {
                siteName: "about://internet",
                userCoun: 5
            },
            {
                siteName: "https://www.mageni.net",
                userCoun: 1
            },
            {
                siteName: "https://login.microsoftonline.com",
                userCoun: 1
            },
            {
                siteName: "https://www.microsoftstore.com",
                userCoun: 1
            },
            {
                siteName: "https://assets.onestore.ms",
                userCoun: 1
            },
            {
                siteName: "https://a3698060313.cdn.optimizely.com",
                userCoun: 1
            },
            {
                siteName: "https://cdn.optimizely.com",
                userCoun: 1
            },
            {
                siteName: "http://c.s-microsoft.com",
                userCoun: 2
            },
            {
                siteName: "http://gpms.taitung.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://embed.tawk.to",
                userCoun: 1
            },
            {
                siteName: "https://vulners.com",
                userCoun: 1
            },
            {
                siteName: "https://mc.yandex.ru",
                userCoun: 1
            },
            {
                siteName: "https://10.50.0.112",
                userCoun: 2
            },
            {
                siteName: "https://salweb.freeway.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://dl.google.com",
                userCoun: 1
            },
            {
                siteName: "https://www.google.com.tw",
                userCoun: 2
            },
            {
                siteName: "https://docs.microsoft.com",
                userCoun: 1
            },
            {
                siteName: "www.bot.com.tw",
                userCoun: 2
            },
            {
                siteName: "caa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "caafmis.caa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "eip.caa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://km2.caa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "mgrdrone.caa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "ssl.caa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "e-learning.cdc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "www.cp.gov.tw",
                userCoun: 2
            },
            {
                siteName: "abs.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "aud.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://compen.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "cpabom.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "exam.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "lifelonglearn.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "medal.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "service.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "svrorg.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "web2.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "web5.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "webhr.dgpa.gov.tw",
                userCoun: 3
            },
            {
                siteName: "worker.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://ebas.gov.tw",
                userCoun: 2
            },
            {
                siteName: "edoc",
                userCoun: 2
            },
            {
                siteName: "edoc1",
                userCoun: 2
            },
            {
                siteName: "https://fnp.gov.tw",
                userCoun: 3
            },
            {
                siteName: "*.pts.fnp.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://pts.fnp.gov.tw",
                userCoun: 2
            },
            {
                siteName: "report.pts.fnp.gov.tw",
                userCoun: 2
            },
            {
                siteName: "hikey.hinet.net",
                userCoun: 2
            },
            {
                siteName: "spam.kia.gov.tw",
                userCoun: 2
            },
            {
                siteName: "www.kia.gov.tw",
                userCoun: 2
            },
            {
                siteName: "easymap.land.moi.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://glir.land.moi.gov.tw",
                userCoun: 2
            },
            {
                siteName: "eria.aac.moj.gov.tw",
                userCoun: 2
            },
            {
                siteName: "eth.moj.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://ecollege.nacs.gov.tw",
                userCoun: 2
            },
            {
                siteName: "edic.good.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "pfiles.tax.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "tax.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "www.einvoice.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "www.etax.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "eservice.nhi.gov.tw",
                userCoun: 2
            },
            {
                siteName: "iccert.nhi.gov.tw",
                userCoun: 2
            },
            {
                siteName: "myhealthbank.nhi.gov.tw",
                userCoun: 2
            },
            {
                siteName: "nou.edu.tw",
                userCoun: 2
            },
            {
                siteName: "motcode.odedi.gov.tw",
                userCoun: 2
            },
            {
                siteName: "web.pcc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "web2.pcc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "www.pcc.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://www.ris.gov.tw",
                userCoun: 2
            },
            {
                siteName: "www.stockvote.com.tw",
                userCoun: 2
            },
            {
                siteName: "addr.taipei.gov.tw",
                userCoun: 2
            },
            {
                siteName: "elearning.taipei.gov.tw",
                userCoun: 2
            },
            {
                siteName: "etrade.yuanta.com.tw",
                userCoun: 2
            },
            {
                siteName: "www.yuanta.com.tw",
                userCoun: 2
            },
            {
                siteName: "192.168.116.25",
                userCoun: 2
            },
            {
                siteName: "129.2.127.205",
                userCoun: 2
            },
            {
                siteName: "pts.fnp.gov.tw",
                userCoun: 2
            },
            {
                siteName: "192.168.115.68",
                userCoun: 2
            },
            {
                siteName: "compen.dgpa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "km2.caa.gov.tw",
                userCoun: 2
            },
            {
                siteName: "ecollege.nacs.gov.tw",
                userCoun: 2
            },
            {
                siteName: "www.ris.gov.tw",
                userCoun: 2
            },
            {
                siteName: "172.16.50.10",
                userCoun: 2
            },
            {
                siteName: "172.16.50.6",
                userCoun: 2
            },
            {
                siteName: "172.16.50.160",
                userCoun: 2
            },
            {
                siteName: "hikey.hinet.net/pubca/unblockcard_pubca.htm",
                userCoun: 2
            },
            {
                siteName: "https://elearning.hrd.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "210.69.99.119",
                userCoun: 2
            },
            {
                siteName: "172.16.50.68",
                userCoun: 2
            },
            {
                siteName: "https://inquiry.nccc.com.tw/",
                userCoun: 2
            },
            {
                siteName: "moica.nat.gov.tw",
                userCoun: 2
            },
            {
                siteName: "http://ecollege.nacs.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "https://compen.dgpa.gov.tw/cpa/sso_verify.aspx",
                userCoun: 2
            },
            {
                siteName: "https://pts.fnp.gov.tw/APNPA/",
                userCoun: 2
            },
            {
                siteName: "172.16.50.60",
                userCoun: 2
            },
            {
                siteName: "172.16.50.61",
                userCoun: 2
            },
            {
                siteName: "https://*.fnp.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "http://moica.nat.gov.tw/unblockcard.html",
                userCoun: 2
            },
            {
                siteName: "http://*.nat.gov.tw/",
                userCoun: 3
            },
            {
                siteName: "https://*.nat.gov.tw/",
                userCoun: 3
            },
            {
                siteName: "http://glir.land.moi.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "http://www.ris.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "http://ebas.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "https://eip.caa.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "http://km2.caa.gov.tw/",
                userCoun: 2
            },
            {
                siteName: "*.nou.edu.tw",
                userCoun: 2
            },
            {
                siteName: "129.2.124.25",
                userCoun: 2
            },
            {
                siteName: "192.168.159.62",
                userCoun: 2
            },
            {
                siteName: "192.168.159.64",
                userCoun: 2
            },
            {
                siteName: "192.168.159.66",
                userCoun: 2
            },
            {
                siteName: "192.168.159.68",
                userCoun: 2
            },
            {
                siteName: "129.2.127.208",
                userCoun: 2
            },
            {
                siteName: "192.168.100.3",
                userCoun: 2
            },
            {
                siteName: "192.168.1.201",
                userCoun: 2
            },
            {
                siteName: "*.moj.gov.tw",
                userCoun: 2
            },
            {
                siteName: "online.archives.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://evans.bot.com.tw",
                userCoun: 1
            },
            {
                siteName: "alw.dgpa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "taiwan.net.tw",
                userCoun: 1
            },
            {
                siteName: "https://admin.taiwan.net.tw",
                userCoun: 1
            },
            {
                siteName: "theme.taiwan.net.tw",
                userCoun: 1
            },
            {
                siteName: "touap.tbad.gov.tw",
                userCoun: 1
            },
            {
                siteName: "tbap",
                userCoun: 1
            },
            {
                siteName: "touap",
                userCoun: 1
            },
            {
                siteName: "https://bli.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://cp.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://dgbas.gov.tw",
                userCoun: 2
            },
            {
                siteName: "https://epa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://webatm.fast.org.tw",
                userCoun: 1
            },
            {
                siteName: "https://hrd.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*..mocs.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.land.moi.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://www.mvdis.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://nlsc.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://pcc.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://ris.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://sfaa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://tbap.tbad.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://touap.tbad.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://tbroc.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://10.171.2.62",
                userCoun: 1
            },
            {
                siteName: "http://10.171.2.57",
                userCoun: 1
            },
            {
                siteName: "http://10.171.2.15",
                userCoun: 1
            },
            {
                siteName: "http://touap.tbad.gov.tw/",
                userCoun: 1
            },
            {
                siteName: "http://tbap.tbad.gov.tw/",
                userCoun: 1
            },
            {
                siteName: "http://10.171.2.62/",
                userCoun: 1
            },
            {
                siteName: "http://10.171.2.57/",
                userCoun: 1
            },
            {
                siteName: "http://10.171.2.15/",
                userCoun: 1
            },
            {
                siteName: "http://*.tbroc.gov.tw/",
                userCoun: 1
            },
            {
                siteName: "http://*.cp.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.cp.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.dgbas.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.dgbas.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.dgpa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.dgpa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.pcc.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.pcc.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.bot.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.bot.com.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.land.moi.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.sfaa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.sfaa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.ris.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.ris.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.bli.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.bli.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://*.hrd.gov.tw/*",
                userCoun: 1
            },
            {
                siteName: "https://*.hrd.gov.tw/*",
                userCoun: 1
            },
            {
                siteName: "https://*.fnp.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://*.masterlink.com.tw/*",
                userCoun: 1
            },
            {
                siteName: "https://*.nlsc.gov.tw/*",
                userCoun: 1
            },
            {
                siteName: "http://*..mocs.gov.tw/*",
                userCoun: 1
            },
            {
                siteName: "https://*..mocs.gov.tw/*",
                userCoun: 1
            },
            {
                siteName: "http://*.epa.gov.tw/*",
                userCoun: 1
            },
            {
                siteName: "https://*.epa.gov.tw/*",
                userCoun: 1
            },
            {
                siteName: "https://iocs.mocs.gov.tw/*",
                userCoun: 1
            },
            {
                siteName: "https://tn.eportal.npa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://10.150.18.14",
                userCoun: 1
            },
            {
                siteName: "www.tyh.com.tw",
                userCoun: 1
            },
            {
                siteName: "https://aosd.moj",
                userCoun: 1
            },
            {
                siteName: "http://apsv.moj",
                userCoun: 1
            },
            {
                siteName: "https://audit.gov.tw",
                userCoun: 1
            },
            {
                siteName: "awpm.moj",
                userCoun: 1
            },
            {
                siteName: "https://cfcmweb.cy.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://pics.dgpa.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://eform.moj",
                userCoun: 1
            },
            {
                siteName: "https://ezwork.moj",
                userCoun: 1
            },
            {
                siteName: "https://pms.fnp.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://hievent.hinet.net",
                userCoun: 1
            },
            {
                siteName: "http://media.hrd.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://www.hrd.gov.tw",
                userCoun: 1
            },
            {
                siteName: "http://misq.ly.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://elearning.moj.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://mojsingle.moj",
                userCoun: 1
            },
            {
                siteName: "https://ecollege.nacs.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://cyey.nat.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://gcaweb.nat.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://eps.nta.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://rad.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://portal.sso.moj",
                userCoun: 1
            },
            {
                siteName: "http://www.km.moj",
                userCoun: 1
            },
            {
                siteName: "http://www.moj",
                userCoun: 1
            },
            {
                siteName: "http://cpaminp.cpami.gov.tw",
                userCoun: 1
            },
            {
                siteName: "about://security_mmc.exe",
                userCoun: 1
            },
            {
                siteName: "cpaminp.cpami.gov.tw",
                userCoun: 1
            },
            {
                siteName: "https://download.microsoft.com",
                userCoun: 2
            },
            {
                siteName: "http://g.adnxs.com",
                userCoun: 1
            },
            {
                siteName: "http://ib.adnxs.com",
                userCoun: 1
            },
            {
                siteName: "https://ajax.aspnetcdn.com",
                userCoun: 1
            },
            {
                siteName: "http://www.bing.com",
                userCoun: 1
            },
            {
                siteName: "http://tags.bkrtx.com",
                userCoun: 1
            },
            {
                siteName: "http://tags.bluekai.com",
                userCoun: 1
            },
            {
                siteName: "http://nexus.ensighten.com",
                userCoun: 1
            },
            {
                siteName: "https://mail.exchangecn.com",
                userCoun: 1
            },
            {
                siteName: "http://ajax.googleapis.com",
                userCoun: 1
            },
            {
                siteName: "https://ssl.gstatic.com",
                userCoun: 1
            },
            {
                siteName: "https://mail.exchange",
                userCoun: 1
            },
            {
                siteName: "http://www.microsofttranslator.com",
                userCoun: 1
            },
            {
                siteName: "http://az416426.vo.msecnd.net",
                userCoun: 1
            },
            {
                siteName: "http://cdn.optimizely.com",
                userCoun: 1
            },
            {
                siteName: "http://i.s-microsoft.com",
                userCoun: 1
            },
            {
                siteName: "http://i1.social.s-msft.com",
                userCoun: 1
            },
            {
                siteName: "http://widgets.membership.s-msft.com",
                userCoun: 1
            },
            {
                siteName: "http://m.webtrends.com",
                userCoun: 1
            },
            {
                siteName: "http://ots.optimize.webtrends.com",
                userCoun: 1
            },
            {
                siteName: "https://win-okj655q3d2d",
                userCoun: 1
            },
            {
                siteName: "http://192.168.11.243",
                userCoun: 1
            },
            {
                siteName: "https://oao-js-tag.onemobile.yahoo.com",
                userCoun: 1
            },
            {
                siteName: "https://s.yimg.com",
                userCoun: 1
            },
            {
                siteName: "https://ldb-svn-ap1",
                userCoun: 2
            },
            {
                siteName: "https://100.100.6.83",
                userCoun: 2
            },
            {
                siteName: "https://192.168.30.179",
                userCoun: 1
            }

  ];

  const agentSoftInfo=[
                    {
                        version: "Microsoft Windows 10 (1809)",
                        count: 122
                    },
                    {
                        version: "Microsoft Windows 10 (21H2)",
                        count: 305
                    },
                    {
                        version: "Microsoft Windows Server 2016 Standard Evaluation (1607)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows 10 (22H2)",
                        count: 3
                    },
                    {
                        version: "Microsoft Windows Server 2022 Standard (21H2)",
                        count: 3
                    },
                    {
                        version: "Microsoft Windows 11 å°ˆæ¥­ç‰ˆ (21H2)",
                        count: 10
                    },
                    {
                        version: "Microsoft Windows 10 (2004)",
                        count: 4
                    },
                    {
                        version: "Microsoft Windows Server 2019 Standard (1809)",
                        count: 10
                    },
                    {
                        version: "Microsoft Windows Server 2019 (N/A)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows 7 (N/A)",
                        count: 336
                    },
                    {
                        version: "Microsoft Windows 10 (21H1)",
                        count: 205
                    },
                    {
                        version: "Microsoft Windows 10 (20H2)",
                        count: 210
                    },
                    {
                        version: "Microsoft Windows 10 (1909)",
                        count: 265
                    },
                    {
                        version: "Microsoft Windows Server 2008 R2 Standard  (N/A)",
                        count: 8
                    },
                    {
                        version: "Microsoft Windows Server 2016 Standard (1607)",
                        count: 14
                    },
                    {
                        version: "Microsoft Windows 10 (1803)",
                        count: 5
                    },
                    {
                        version: "Microsoft Windows 10 (1607)",
                        count: 13
                    },
                    {
                        version: "Microsoft Windows 10 (1709)",
                        count: 15
                    },
                    {
                        version: "Microsoft Windows Server 2019 Datacenter (1809)",
                        count: 6
                    },
                    {
                        version: "Microsoft Windows Server 2016 Datacenter (1607)",
                        count: 60
                    },
                    {
                        version: "Microsoft Windows Server 2012 R2 Datacenter (N/A)",
                        count: 9
                    },
                    {
                        version: "Microsoft Windows Server 2008 R2 Enterprise  (N/A)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows Server 2012 R2 Standard (N/A)",
                        count: 35
                    },
                    {
                        version: "Microsoft Windows 11 å®¶ç”¨ç‰ˆ (21H2)",
                        count: 3
                    },
                    {
                        version: "Red Hat Enterprise Linux 8.2 (Ootpa) (N/A)",
                        count: 3
                    },
                    {
                        version: "Red Hat Enterprise Linux 8.4 (Ootpa) (N/A)",
                        count: 15
                    },
                    {
                        version: "Red Hat Enterprise Linux 8.5 (Ootpa) (N/A)",
                        count: 1
                    },
                    {
                        version: "Red Hat Enterprise Linux 8.6 (Ootpa) (N/A)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows 10 (N/A)",
                        count: 616
                    },
                    {
                        version: "Red Hat Enterprise Linux 8.3 (Ootpa) (N/A)",
                        count: 3
                    },
                    {
                        version: "Microsoft Windows Server 2012 Standard (9.11.9600.19329)",
                        count: 24
                    },
                    {
                        version: "Mozilla Firefox (N/A)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows 8.1 (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2016 R2 WebServer (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2016 R2 FileServer (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2016 R2 DNS (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2016 R2 DC (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2016 R2 (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2012 R2 WebServer (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2012 R2 FileServer (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2012 R2 DNS (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2012 R2 DC (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2012 R2 (N/A)",
                        count: 1
                    },
                    {
                        version: "Windows Server 2008 R2 (N/A)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows 10 (2009)",
                        count: 9
                    },
                    {
                        version: "Microsoft Windows 10 (1511)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows Storage Server 2016 Standard (1607)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows 10 (1903)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows Server 2016 Standard (N/A)",
                        count: 5
                    },
                    {
                        version: "Microsoft Windows 11 å°ˆæ¥­ç‰ˆ (N/A)",
                        count: 9
                    },
                    {
                        version: "Microsoft Windows Server 2012 R2 Standard (9.11.9600.16384)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows Server 2012 R2 Standard (9.11.9600.20016)",
                        count: 4
                    },
                    {
                        version: "Microsoft Windows Server 2012 R2 Standard (9.11.9600.17031)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows Server 2012 Standard (9.10.9200.16384)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows 7 (8.0.7601.17514)",
                        count: 1
                    },
                    {
                        version: "Red Hat Enterprise Linux Server release 7.9 (Maipo) (N/A)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows Storage Server 2012 R2 Standard (N/A)",
                        count: 1
                    },
                    {
                        version: "SUSE Linux Enterprise Server 11 SP4 (N/A)",
                        count: 2
                    },
                    {
                        version: "CentOS Linux 7 (Core) (N/A)",
                        count: 2
                    },
                    {
                        version: "SUSE Linux Enterprise Server 15 (N/A)",
                        count: 1
                    },
                    {
                        version: "Microsoft Windows Server 2012 R2 Standard (9.11.9600.19724)",
                        count: 1
                    },
                    {
                        version: "Red Hat Enterprise Linux release 8.3 (Ootpa) (N/A)",
                        count: 1
                    },
                    {
                        version: "Ubuntu 14.04.6 LTS (N/A)",
                        count: 1
                    },
                    {
                        version: "CentOS Linux release 7.8.2003 (Core) (N/A)",
                        count: 1
                    },
                    {
                        version: "8.0.2510.8",
                        count: 96
                    },
                    {
                        version: "8.0.2810.9",
                        count: 2
                    },
                    {
                        version: "8.0.3510.10",
                        count: 1
                    },
                    {
                        version: "8.0.2020.8",
                        count: 1
                    },
                    {
                        version: "7.0.800",
                        count: 3
                    },
                    {
                        version: "8.0.1810.13",
                        count: 1
                    },
                    {
                        version: "8.0.3330.2",
                        count: 380
                    },
                    {
                        version: "8.0.1710.11",
                        count: 2
                    },
                    {
                        version: "8.0.2710.9",
                        count: 1
                    },
                    {
                        version: "8.0.2210.11",
                        count: 1
                    },
                    {
                        version: "6.0.220",
                        count: 1
                    },
                    {
                        version: "7.0.790",
                        count: 1
                    },
                    {
                        version: "8.0.3410.10",
                        count: 2
                    },
                    {
                        version: "8.0.1120.15",
                        count: 1
                    },
                    {
                        version: "8.0.3310.9",
                        count: 2
                    },
                    {
                        version: "8.0.3210.7",
                        count: 1
                    },
                    {
                        version: "1.8.0",
                        count: 2
                    },
                    {
                        version: "8.0.2010.9",
                        count: 1
                    },
                    {
                        version: "8.0.400",
                        count: 1
                    },
                    {
                        version: "8.0.3110.11",
                        count: 1
                    },
                    {
                        version: "other",
                        count: 942
                    },
                    {
                        version: "Trend Micro Apex One é˜²æ¯’",
                        count: 2
                    },
                    {
                        version: "Windows Defender",
                        count: 22
                    },
                    {
                        version: "Trend Micro Apex One é˜²æ¯’_14.0.0.11088",
                        count: 3
                    },
                    {
                        version: "F-Secure Client Security Premium_3.7.36.0",
                        count: 1
                    },
                    {
                        version: "Kaspersky Endpoint Security for Windows_11.2.0.2254",
                        count: 7
                    },
                    {
                        version: "Windows Defender_1.351.176.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.293.2024.0",
                        count: 8
                    },
                    {
                        version: "Windows Defender_1.329.2200.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1622.0",
                        count: 8
                    },
                    {
                        version: "Windows Defender_1.355.2408.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1519.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.313.842.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.51.0",
                        count: 5
                    },
                    {
                        version: "Windows Defender_1.311.17.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1595.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.333.368.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.663.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.574.0",
                        count: 1
                    },
                    {
                        version: "Kaspersky Endpoint Security for Windows_11.6.0.394",
                        count: 186
                    },
                    {
                        version: "Windows Defender_1.355.2425.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.1297.0",
                        count: 41
                    },
                    {
                        version: "Windows Defender_1.355.2612.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.2092.0",
                        count: 11
                    },
                    {
                        version: "Windows Defender_1.347.559.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.329.1187.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.1782.0",
                        count: 3
                    },
                    {
                        version: "Windows Defender_1.311.1747.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.357.221.0",
                        count: 1
                    },
                    {
                        version: "Kaspersky Endpoint Security for Windows_11.4.0.233",
                        count: 4
                    },
                    {
                        version: "Windows Defender_1.343.2079.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.1301.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.1262.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.201.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.1426.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.359.156.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.1352.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.1294.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.799.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.374.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.349.407.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.828.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.311.96.0",
                        count: 4
                    },
                    {
                        version: "Windows Defender_1.311.34.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.319.690.0",
                        count: 29
                    },
                    {
                        version: "Windows Defender_1.359.592.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.319.625.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.357.303.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.414.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.311.11.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.343.845.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.303.25.0",
                        count: 3
                    },
                    {
                        version: "Windows Defender_1.357.412.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.670.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.309.601.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.480.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.1306.0",
                        count: 1
                    },
                    {
                        version: "McAfee Endpoint Security_10.5.3",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.645.0",
                        count: 4
                    },
                    {
                        version: "Windows Defender_1.309.488.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.319.399.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.527.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.603.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.309.609.0",
                        count: 3
                    },
                    {
                        version: "Windows Defender_1.309.723.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.247.663.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.309.775.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.2275.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.334.0",
                        count: 7
                    },
                    {
                        version: "Windows Defender_1.313.2099.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.2243.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.325.13.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.359.407.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.345.0",
                        count: 9
                    },
                    {
                        version: "Windows Defender_1.347.68.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.48.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.2027.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.1499.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.521.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.370.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.421.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.349.1466.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.355.1876.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.329.1992.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.410.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.335.659.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.325.146.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.356.0",
                        count: 13
                    },
                    {
                        version: "Windows Defender_1.323.362.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.462.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.359.559.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.2094.0",
                        count: 25
                    },
                    {
                        version: "Windows Defender_1.353.12.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.325.1508.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.1239.0",
                        count: 2
                    },
                    {
                        version: "McAfee Endpoint Security (anti-virus)",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.1587.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1123.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.331.186.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.1561.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.925.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1011.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1130.0",
                        count: 1
                    },
                    {
                        version: "McAfee Endpoint Security_10.6.1",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.347.366.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.315.1096.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.355.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.512.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.236.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.2056.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.309.429.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.309.925.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.309.1235.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.341.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.347.625.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.313.2703.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.339.914.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1162.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.307.920.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.333.160.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.2265.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.1065.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.339.1972.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.1811.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.359.570.0",
                        count: 5
                    },
                    {
                        version: "Windows Defender_1.343.1718.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.77.0",
                        count: 4
                    },
                    {
                        version: "Windows Defender_1.309.699.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.1676.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.313.0",
                        count: 1
                    },
                    {
                        version: "McAfee Endpoint Security",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.702.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.410.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.1292.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.624.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.317.330.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.1798.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.355.738.0",
                        count: 3
                    },
                    {
                        version: "Windows Defender_1.321.997.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.698.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.357.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.2205.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1380.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.331.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.1052.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.1030.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.314.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.345.434.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.101.0",
                        count: 1
                    },
                    {
                        version: "Microsoft Security Essentials_4.10.209.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.329.1772.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.801.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.1895.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.542.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.2103.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.323.1684.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.621.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.359.282.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.324.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.305.2437.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.550.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.1385.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.81.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.2254.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.333.1441.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.359.547.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.333.373.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.309.728.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.329.829.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.1810.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.441.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.315.59.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.309.470.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.329.2872.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.569.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.2403.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.934.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.2153.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.109.0",
                        count: 1
                    },
                    {
                        version: "Trend Micro Apex One é˜²æ¯’_14.0.0.10101",
                        count: 135
                    },
                    {
                        version: "Trend Micro Apex One é˜²æ¯’_14.0.0.9601",
                        count: 222
                    },
                    {
                        version: "Windows Defender_4.18.1807.18075",
                        count: 93
                    },
                    {
                        version: "Windows Defender_4.18.1902.5",
                        count: 26
                    },
                    {
                        version: "Windows Defender_4.18.1909.6",
                        count: 72
                    },
                    {
                        version: "è¶¨å‹¢ç§‘æŠ€ OfficeScan é˜²æ¯’_12.0.0.6359",
                        count: 2
                    },
                    {
                        version: "Trend Micro Apex One é˜²æ¯’_14.0.0.9110",
                        count: 1
                    },
                    {
                        version: "Trend Micro Apex One é˜²æ¯’_14.0.0.8288",
                        count: 1
                    },
                    {
                        version: "Trend Micro Apex One é˜²æ¯’_14.0.0.8317",
                        count: 4
                    },
                    {
                        version: "Trend Micro Apex One Antivirus_14.0.0.10101",
                        count: 1
                    },
                    {
                        version: "Windows Defender_4.13.17134.1",
                        count: 1
                    },
                    {
                        version: "Symantec Endpoint Protection_14.3.1148.100",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.355.1538.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.333.1507.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.1507.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.231.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.357.194.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.974.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.865.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.24.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.331.2134.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.2184.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.333.1308.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.331.2143.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1549.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.831.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.2207.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.2076.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.353.561.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.1613.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.305.304.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.237.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.2064.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.1245.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.1312.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.137.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.1904.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.2520.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.1597.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.2169.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.1374.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1115.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.333.255.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.239.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.884.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.1221.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.345.627.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.335.1199.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.1191.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.2033.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.234.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.557.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.329.2075.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.341.1383.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.772.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.323.424.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.311.598.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.2211.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.1731.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.1214.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.1070.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.359.608.0",
                        count: 3
                    },
                    {
                        version: "Windows Defender_1.327.1487.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.622.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.1383.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.823.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.813.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.429.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.329.3327.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1568.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.795.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.832.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.329.838.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.1341.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.1196.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.755.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.2135.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1306.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.359.588.0",
                        count: 4
                    },
                    {
                        version: "Windows Defender_1.353.1817.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.1886.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.2043.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.698.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.1104.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.811.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.1714.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.1348.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.2253.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.347.124.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.548.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.1925.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.1111.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.329.140.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.25.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.379.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.1392.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.359.278.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.339.1772.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.345.209.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.1383.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.303.261.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.604.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.1233.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.321.1703.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.321.1644.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.305.1333.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.311.8.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.1306.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.766.0",
                        count: 1
                    },
                    {
                        version: "Avast Antivirus",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.1028.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.263.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.385.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.1758.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.2050.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.343.1665.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.345.208.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.2354.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.335.1149.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.857.0",
                        count: 4
                    },
                    {
                        version: "Windows Defender_1.339.1908.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.790.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.2459.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.309.339.0",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.347.830.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.345.741.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.339.373.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.331.882.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.693.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.1708.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.2150.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.355.2262.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.327.1980.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.1059.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.2295.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.337.541.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.347.201.0",
                        count: 1
                    },
                    {
                        version: "F-Secure Client Security Premium_15.21.4.0",
                        count: 99
                    },
                    {
                        version: "Windows Defender_1.359.326.0",
                        count: 1
                    },
                    {
                        version: "F-Secure Client Security Premium_15.21",
                        count: 4
                    },
                    {
                        version: "Windows Defender_4.9.10586.1106",
                        count: 1
                    },
                    {
                        version: "Symantec Endpoint Protection_14.3.1169.0100",
                        count: 6
                    },
                    {
                        version: "Trend Micro OfficeScan Antivirus",
                        count: 2
                    },
                    {
                        version: "Windows Defender_1.363.162.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_4.18.2104.10",
                        count: 2
                    },
                    {
                        version: "ESET Security",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.361.124.0",
                        count: 1
                    },
                    {
                        version: "Symantec Endpoint Protection_14.2.3332.1000",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.343.957.0",
                        count: 1
                    },
                    {
                        version: "Symantec Endpoint Protection_14.3.558.0000",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.349.1964.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.353.1553.0",
                        count: 1
                    },
                    {
                        version: "F-Secure Client Security_14.22.109.0",
                        count: 2
                    },
                    {
                        version: "F-Secure Client Security_14.22",
                        count: 2
                    },
                    {
                        version: "F-Secure Client Security Premium_15.21.6.0",
                        count: 2
                    },
                    {
                        version: "F-Secure Client Security Premium_15.11",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.333.1225.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.742.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.351.1213.0",
                        count: 1
                    },
                    {
                        version: "Windows Defender_1.361.555.0",
                        count: 1
                    },
                    {
                        version: "7.18.0630",
                        count: 1
                    }                               
  ];
  const gcb_agentPassStat=[ 
    {
      total: 2370,
      passed: 822,
      failed: 832,
      other: 716,
    }
  ];
  const gcb_ratio= [
    {
      passed: "0.3468354430379747",      
      failed: "0.3510548523206751",
      other: "0.30210970464135023",
    }
  ];
  const recentTransactions = [
    {
      icon: SendIcon,
      type: "Send transaction",
      date: "Dec 24, 2021",
      amount: "$ 123.00",
      balance: "$ 334.00",
    },
    {
      icon: ReceiveIcon,
      type: "Receive fund",
      date: "Jul 20. 2021",
      amount: "$ 322.00",
      balance: "$ 658.00",
    },
  ];

  const invoices = [
    {
      no: "#BCS101",
      date: "Jun 21, 2020",
      avatar: "/img/avatar-2.jpeg",
      name: "Alexandar Parkinson",
      amount: "$ 13435.50",
      status: "Successful",
    },
    {
      no: "#BSD133",
      date: "Jun 21, 2020",
      avatar: "/img/avatar-3.jpeg",
      name: "Natasha Analington",
      amount: "$ 1654.50",
      status: "Pending",
    },
  ];
</script>

<template> 
  <nav class="bg-white border-gray-200 dark:bg-gray-900">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between">
      <a class="flex items-center">
          <img src="./icons/dragonsoftlogo.png" class="h-11 mr-3 ml-4"/>
          <span class="self-center font-semi whitespace-nowrap dark:text-white text-gray-400 text-[3px] ml-14">政府組態基準(GCB) | 政府機關資安落點通報機制(VANS)</span>
      </a>
      <div class="justify-end">
          <button class="inline-flex items-center gap-x-1 py-2 px-4 text-sm text-gray-400 text-[3px] hover:text-blue-400">
            說明
          </button>
          <button class="inline-flex items-center gap-x-1 py-2 px-4 text-sm text-gray-400 text-[3px] hover:text-blue-400">
            登出
          </button>
      </div>
    </div>
  </nav>
  <div class="flex min-h-screen w-full bg-gray-700 font-sans">
    <aside class="flex w-56 flex-col px-4 pb-6"><!--pt-10-->
      <ul class="flex flex-1 flex-col pt-5"><!-- px-8 gap-y-10-->
        <li v-for="item in menu">
          <a
            href="#"
            class="flex items-center gap-x-4 text-white hover:bg-gray-600 hover:font-medium hover:text-blue-300 hover:rounded-lg p-4 focus:font-medium focus:text-white focus:outline-none">
            <Component :is="item.icon" class="h-6 w-6 stroke-current" />
            <span>{{ item.name }}</span>
          </a>
        </li>
      </ul>
      
    </aside>
    
      <!--選擇器-->
    <main class="flex min-h-screen flex-1 flex-col bg-gray-300 p-4">
      <TabGroup >
        <TabList>
          <Tab class="inline-block p-4 rounded-t-lg bg-gray-100 text-gray-400 hover:text-blue-400 hover:bg-gray-50 ">資產</Tab>
          <Tab class="inline-block p-4 rounded-t-lg bg-gray-100 text-gray-400 hover:text-blue-400 hover:bg-gray-50 ">GCB</Tab>
          <Tab class="inline-block p-4 rounded-t-lg bg-gray-100 text-gray-400 hover:text-blue-400 hover:bg-gray-50 ">VANS</Tab>
        </TabList>
        <TabPanels>

          <TabPanel>
          <div class="flex gap-x-4 px-4 py-6 bg-gray-100 rounded-tr-lg">
            <!-- <div class="flex gap-y-8 gap-x-3 "> -->
              <!--資產總額-->  
              <div class="flex items-center rounded-10 bg-gray-100 p-6 border border-gray-300">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill: rgb(59 130 246);transform: ;msFilter:;"><path d="M22 7.999a1 1 0 0 0-.516-.874l-9.022-5a1.003 1.003 0 0 0-.968 0l-8.978 4.96a1 1 0 0 0-.003 1.748l9.022 5.04a.995.995 0 0 0 .973.001l8.978-5A1 1 0 0 0 22 7.999zm-9.977 3.855L5.06 7.965l6.917-3.822 6.964 3.859-6.918 3.852z"></path><path d="M20.515 11.126 12 15.856l-8.515-4.73-.971 1.748 9 5a1 1 0 0 0 .971 0l9-5-.97-1.748z"></path><path d="M20.515 15.126 12 19.856l-8.515-4.73-.971 1.748 9 5a1 1 0 0 0 .971 0l9-5-.97-1.748z"></path></svg>              </div>
                <div>
                  <div v-for="item in gcb_agentPassStat" class="text-blue-500">
                    <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                    <span>{{ item.total }}</span>
                  </div>
                  <div class="text-sm pt-1 text-gray-400">資產總額</div>
                </div>
              </div>
              <!--今日回報數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-7 border border-gray-300">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill:rgb(132 204 22);transform: ;msFilter:;"><path d="M12 2C6.486 2 2 6.486 2 12s4.486 10 10 10 10-4.486 10-10S17.514 2 12 2zm0 18c-4.411 0-8-3.589-8-8s3.589-8 8-8 8 3.589 8 8-3.589 8-8 8z"></path><path d="M9.999 13.587 7.7 11.292l-1.412 1.416 3.713 3.705 6.706-6.706-1.414-1.414z"></path></svg>
                </div>
                <div>
                  <div class="text-lime-500">
                    <div v-for="item in assets_report">
                      <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                      <span>{{ item.report }}</span>
                    </div>
                  </div>
                  <div class="text-sm pt-1 text-gray-400">今日回報數</div>
                </div>
              </div>
              <!--今日未回報數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-7 border border-gray-300">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill: rgb(248 113 113);transform: ;msFilter:;"><path d="M9.172 16.242 12 13.414l2.828 2.828 1.414-1.414L13.414 12l2.828-2.828-1.414-1.414L12 10.586 9.172 7.758 7.758 9.172 10.586 12l-2.828 2.828z"></path><path d="M12 22c5.514 0 10-4.486 10-10S17.514 2 12 2 2 6.486 2 12s4.486 10 10 10zm0-18c4.411 0 8 3.589 8 8s-3.589 8-8 8-8-3.589-8-8 3.589-8 8-8z"></path></svg>
                </div>
                <div>
                  <div class="text-red-400">
                    <div v-for="item in assets_report">
                    <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                    <span>{{ item.unreport }}</span>
                    </div>
                  </div>
                  <div class="text-sm pt-1 text-gray-400">今日未回報數</div>
                </div>
              </div>
              <!--30天未回報數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-7 border border-gray-300">
                <div class="pr-2">
                  <div class="rounded-full border-4 border-gray-500 ">
                    <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" style="fill: rgb(107 114 128);transform: ;msFilter:;"><path d="M12 4C9.243 4 7 6.243 7 9h2c0-1.654 1.346-3 3-3s3 1.346 3 3c0 1.069-.454 1.465-1.481 2.255-.382.294-.813.626-1.226 1.038C10.981 13.604 10.995 14.897 11 15v2h2v-2.009c0-.024.023-.601.707-1.284.32-.32.682-.598 1.031-.867C15.798 12.024 17 11.1 17 9c0-2.757-2.243-5-5-5zm-1 14h2v2h-2z"></path></svg>
                  </div>
                </div>
                <div>
                  <div class="text-gray-400">
                    <div v-for="item in assets_report">
                    <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                    <span>{{ item.th_report }}</span>
                    </div>
                  </div>
                  <div class="text-sm pt-1 text-gray-400">30天未回報數</div>
                </div>
              </div>
              <!--部門選擇器-->
              <div class="flex items-center rounded-10 text-center bg-gray-100 p-7 border border-gray-300">
                  <div>
                    <div class="text-gray-400">部門
                    
                    </div>
                    <div class="text-sm pt-1 text-gray-400">
                      <select class="p-2 rounded-10">
                        <option value="none" selected disabled hidden>全部</option> 
                        <option value ="taipei">台北市</option>
                        <option value ="Kaohsiung">高雄市</option>
                      </select>
                    </div>
                  </div>
              </div>
              <!--本部選擇器-->
              <div class="flex items-center rounded-10 text-center bg-gray-100 p-7 border border-gray-300">
                <div>
                  <div class="text-gray-400">本部
                  </div>
                  <div class="text-sm pt-1 text-gray-400">
                    <select class="p-2 rounded-10">
                      <option value="none" selected disabled hidden>選擇分站</option> 
                      <option value ="taipei">台北市</option>
                      <option value ="Kaohsiung">高雄市</option>
                    </select>
                  </div>
                </div>
              </div>
            <!-- </div> -->
          </div>
          <div class="flex gap-x-6  px-4 py-2 pb-4 bg-gray-100 rounded-b-lg">
            <!--左側圖表-->
            <div class="flex w-1/2 flex-col gap-y-8 "><!--w-3/5-->
              <div class="flex flex-col justify-between rounded-10 bg-gray-100 border border-gray-300 ">
                <div class="p-3 rounded-t-lg bg-gray-300">
                  <div class="flex-wrap">
                    <div>
                      <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1 ">作業系統</span>
                      <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1 ">Internet Explorer</span>
                      <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1 ">Google Chrome</span>
                      <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1">Firefox</span>
                    </div>
                    <div class="pt-4">
                    </div>
                    <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1">Edge</span>
                    <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1">Java</span>
                    <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1">防毒軟體</span>
                    <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1">Flash Player</span>
                    <span class="rounded-10 p-2 bg-gray-400 text-gray-300 text-sm m-1">Adobe Reader</span>
                  </div>
                </div>
                <div class="gap-x-8 pt-2 h-80 overflow-scroll">
                  <div class="flex">
                    <div class="w-1/4">
                        <DoughnutChart class="pl-2"/>
                      </div>
                    <div class="w-3/4 pl-4 pt-2 text-gray-400 text-sm">
                      <p class="pl-4">網址</p>
                      <ul class="flex flex-1 flex-col pt-1"><!-- px-8 gap-y-10-->
                        <li v-for="item in agentSoftInfo">
                          <a
                            href="#"
                            class="flex items-center gap-x-4 text-gray-400 hover:font-medium hover:text-blue-300 hover:rounded-lg px-4 py-1 focus:font-medium focus:text-white focus:outline-none">
                            <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                            <div class="text-xs">
                              <span>{{ item.version }}</span>
                            </div>
                          </a>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="flex w-1/2 flex-col gap-y-8"><!--w-2/5-->
              <div class="flex flex-col justify-between rounded-10 bg-gray-100 border border-gray-300">
                  <div class="p-3 rounded-t-lg bg-gray-300">
                    最近30天回保狀況
                  </div>
                  <div class="flex gap-x-8">
                    <img src="./image/asset_1.png" alt="">
                  </div>
              </div>
            </div>
          </div>
          </TabPanel>
          <TabPanel>

            <div class="flex gap-x-4 px-4 py-6 bg-gray-100 rounded-tr-lg">
            <!-- <div class="flex gap-y-8 gap-x-3 "> -->
              <!--2 資產總額-->  
              <div class="flex items-center rounded-10 bg-gray-100 p-6 border border-gray-300 w-full">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill: rgb(59 130 246);transform: ;msFilter:;"><path d="M22 7.999a1 1 0 0 0-.516-.874l-9.022-5a1.003 1.003 0 0 0-.968 0l-8.978 4.96a1 1 0 0 0-.003 1.748l9.022 5.04a.995.995 0 0 0 .973.001l8.978-5A1 1 0 0 0 22 7.999zm-9.977 3.855L5.06 7.965l6.917-3.822 6.964 3.859-6.918 3.852z"></path><path d="M20.515 11.126 12 15.856l-8.515-4.73-.971 1.748 9 5a1 1 0 0 0 .971 0l9-5-.97-1.748z"></path><path d="M20.515 15.126 12 19.856l-8.515-4.73-.971 1.748 9 5a1 1 0 0 0 .971 0l9-5-.97-1.748z"></path></svg>              </div>
                <div>
                  <div class="text-blue-500">
                    <div v-for="item in gcb_agentPassStat">
                      <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                      <span>{{ item.total }}</span>
                    </div>
                </div>
                  <div class="text-sm pt-1 text-gray-400">資產總額</div>
                </div>
              </div>
              <!--2 符合數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-7 border border-gray-300 w-full">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill:rgb(132 204 22);transform: ;msFilter:;"><path d="M12 2C6.486 2 2 6.486 2 12s4.486 10 10 10 10-4.486 10-10S17.514 2 12 2zm0 18c-4.411 0-8-3.589-8-8s3.589-8 8-8 8 3.589 8 8-3.589 8-8 8z"></path><path d="M9.999 13.587 7.7 11.292l-1.412 1.416 3.713 3.705 6.706-6.706-1.414-1.414z"></path></svg>
                </div>
                <div>
                  <div class="text-lime-500">
                    <div v-for="item in gcb_agentPassStat">
                      <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                      <span>{{ item.passed }}</span>
                    </div>
                  </div>
                  <div class="text-sm pt-1 text-gray-400">符合數</div>
                </div>
              </div>
              <!--2 未符合數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-7 border border-gray-300 w-full">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill: rgb(248 113 113);transform: ;msFilter:;"><path d="M9.172 16.242 12 13.414l2.828 2.828 1.414-1.414L13.414 12l2.828-2.828-1.414-1.414L12 10.586 9.172 7.758 7.758 9.172 10.586 12l-2.828 2.828z"></path><path d="M12 22c5.514 0 10-4.486 10-10S17.514 2 12 2 2 6.486 2 12s4.486 10 10 10zm0-18c4.411 0 8 3.589 8 8s-3.589 8-8 8-8-3.589-8-8 3.589-8 8-8z"></path></svg>
                </div>
                <div>
                  <div class="text-red-400">
                    <div v-for="item in gcb_agentPassStat">
                      <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                      <span>{{ item.failed }}</span>
                    </div>
                  </div>
                  <div class="text-sm pt-1 text-gray-400">未符合數</div>
                </div>
              </div>
              <!--2 未稽核數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-7 border border-gray-300 w-full">
                <div class="pr-2">
                  <div class="rounded-full border-4 border-gray-500 ">
                    <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" style="fill: rgb(107 114 128);transform: ;msFilter:;"><path d="M12 4C9.243 4 7 6.243 7 9h2c0-1.654 1.346-3 3-3s3 1.346 3 3c0 1.069-.454 1.465-1.481 2.255-.382.294-.813.626-1.226 1.038C10.981 13.604 10.995 14.897 11 15v2h2v-2.009c0-.024.023-.601.707-1.284.32-.32.682-.598 1.031-.867C15.798 12.024 17 11.1 17 9c0-2.757-2.243-5-5-5zm-1 14h2v2h-2z"></path></svg>
                  </div>
                </div>
                <div>
                  <div class="text-gray-400">
                    <div v-for="item in gcb_agentPassStat">
                      <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                      <span>{{ item.other }}</span>
                    </div>
                  </div>
                  <div class="text-sm pt-1 text-gray-400">未稽核數</div>
                </div>
              </div>
              <!--部門選擇器-->
              <div class="flex items-center rounded-10 text-center bg-gray-100 p-7 border border-gray-300">
                  <div>
                    <div class="text-gray-400">部門
                    
                    </div>
                    <div class="text-sm pt-1 text-gray-400">
                      <select class="p-2 rounded-10">
                        <option value="none" selected disabled hidden>全部</option> 
                        <option value ="taipei">台北市</option>
                        <option value ="Kaohsiung">高雄市</option>
                      </select>
                    </div>
                  </div>
              </div>
              <!--本部選擇器-->
              <div class="flex items-center rounded-10 text-center bg-gray-100 p-7 border border-gray-300">
                <div>
                  <div class="text-gray-400">本部
                  </div>
                  <div class="text-sm pt-1 text-gray-400">
                    <select class="p-2 rounded-10">
                      <option value="none" selected disabled hidden>選擇分站</option> 
                      <option value ="taipei">台北市</option>
                      <option value ="Kaohsiung">高雄市</option>
                    </select>
                  </div>
                </div>
              </div>
            <!-- </div> -->
          </div>
          <div class="flex gap-x-6  px-4 py-2 bg-gray-100 rounded-b-lg pb-4">
            <!--左側圖表-->
              <div class="flex w-1/2 flex-col gap-y-8"><!--w-3/5-->
                <div class="flex gap-y-8 ">
                  <!--近期稽核情形（稽核資產數）-->
                  <div class="flex-col w-1/2 justify-between rounded-10 bg-gray-100 border border-gray-300 mr-2"><!-- p-7-->
                    <nav>
                      <select class="p-3 rounded-t-lg bg-gray-300 w-full">
                        <option value="none" selected disabled hidden>近期稽核情形（稽核資產數）</option> 
                        <option value ="unknow1">近期稽核情形（稽核資產數）</option>
                        <option value ="unknow2">HelloWorld</option>
                    </select>
                    </nav>
                    <div class="flex items-center justify-between px-2">
                      <div class="w-3/4">
                        <img src="./image/dashboard_gcb_1.png">
                      </div>
                      <div class="w-1/4">
                        <div>
                          <div class="flex-col items-right gap-x-1 py-2 pl-2">
                            <p class="text-black text-lg">11</p>
                            <p class="text-gray-400 text-xs">最近3日</p>
                          </div>
                          <div class="flex-col items-right gap-x-1 py-2 pl-2 ">
                            <p class="text-black text-lg">15</p>
                            <p class="text-gray-400 text-xs">最近7日</p>
                          </div>
                          <div class="flex-col items-right gap-x-1 py-2 pl-2 ">
                            <p class="text-black text-lg">22</p>
                            <p class="text-gray-400 text-xs">最近15日</p>
                          </div>
                          <div class="flex-col items-right gap-x-1 py-2 pl-2 ">
                            <p class="text-black text-lg">26</p>
                            <p class="text-gray-400 text-xs">最近30日</p>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <!--資產符合率-->
                  <div class="flex-col w-1/2 justify-between rounded-10 bg-gray-100 border border-gray-300 ml-2" ><!-- p-7-->
                    <nav>
                      <select class="p-3 rounded-t-lg bg-gray-300 w-full">
                        <option value="none" selected disabled hidden>資產符合率</option> 
                        <option value ="unknow1">資產符合率</option>
                        <option value ="unknow2">HelloWorld</option>
                    </select>
                    </nav>
                    <div class="flex items-center justify-between px-2">
                      <div class="w-3/5">
                        <DoughnutChart />
                      </div>
                      <div class="w-2/5">
                        <div class="inline-flex flex-col items-right gap-x-1 py-2 px-4 ">
                          <p class="text-black text-lg">34.68%</p>
                          <p class="text-gray-400 text-xs">符合</p>
                        </div>
                        <div class="flex-col items-right gap-x-1 py-2 px-4 ">
                          <p class="text-black text-lg">35.11%</p>
                          <p class="text-gray-400 text-xs">未符合</p>
                        </div>
                        <div class="flex-col items-right gap-x-1 py-2 px-4 ">
                          <p class="text-black text-lg">30.21%</p>
                          <p class="text-gray-400 text-xs">未稽核</p>
                        </div>
                      </div>
                    </div>
                  </div>
              </div>
              <div class="flex flex-col justify-between rounded-10 bg-gray-100 border border-gray-30 h-80"><!-- p-7-->
                <nav>
                  <select class="p-3 rounded-t-lg bg-gray-300 w-full">
                    <option value="none" selected disabled hidden>信任網址列表</option> 
                    <option value ="unknow1">信任網址列表</option>
                    <option value ="unknow2">HelloWorld</option>
                  </select>
                </nav>
                <div class="overflow-scroll"><!--flex items-center overflow-auto??-->
                  <div class="flex">
                    <div class="w-3/4 pl-4 pt-2 text-gray-400 text-sm">
                      <p>網址</p>
                    </div>
                    <div class="w-1/4 pt-2 text-gray-400 text-sm">
                      <p>使用次數</p>
                    </div>
                  </div>
                  <ul class="flex flex-1 flex-col pt-1"><!-- px-8 gap-y-10-->
                  <li v-for="item in gcb_agentTrustSiteInfo">
                    <a
                      href="#"
                      class="flex items-center gap-x-4 text-gray-400 hover:font-medium hover:text-blue-300 hover:rounded-lg px-4 py-1 focus:font-medium focus:text-white focus:outline-none">
                      <Component :is="item.icon" class="h-6 w-6 stroke-current" />
                      <div class="w-3/4 text-xs">
                        <span>{{ item.siteName }}</span>
                      </div>
                      <div class="w-1/4 text-xs">
                        <span>{{ item.userCoun }}</span>
                      </div>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
            </div>
            <div class="flex w-1/2 flex-col gap-y-8"><!--w-2/5-->
              <div class="flex flex-col justify-between rounded-10 bg-gray-100 border border-gray-300 "><!--p-7-->
                <nav>
                    <select class="p-3 rounded-t-lg bg-gray-300 w-full">
                      <option value="none" selected disabled hidden>稽核項目分類統計</option> 
                      <option value ="unknow1">稽核項目分類統計</option>
                      <option value ="unknow2">HelloWorld</option>
                    </select>
                  </nav>
              <div class="flex gap-x-8">
                <img src="./image/gcb_3.png">
              </div>
              </div>
            </div>
          </div>
          </TabPanel>

          <TabPanel>
            <div class="flex gap-x-2 px-4 py-6 bg-gray-100 rounded-tr-lg">
            <!-- <div class="flex gap-y-8 gap-x-3 "> -->
              <!--2 資產總額-->  
              <div class="flex items-center rounded-10 bg-gray-100 p-4 border border-gray-300">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill: rgb(59 130 246);transform: ;msFilter:;"><path d="M22 7.999a1 1 0 0 0-.516-.874l-9.022-5a1.003 1.003 0 0 0-.968 0l-8.978 4.96a1 1 0 0 0-.003 1.748l9.022 5.04a.995.995 0 0 0 .973.001l8.978-5A1 1 0 0 0 22 7.999zm-9.977 3.855L5.06 7.965l6.917-3.822 6.964 3.859-6.918 3.852z"></path><path d="M20.515 11.126 12 15.856l-8.515-4.73-.971 1.748 9 5a1 1 0 0 0 .971 0l9-5-.97-1.748z"></path><path d="M20.515 15.126 12 19.856l-8.515-4.73-.971 1.748 9 5a1 1 0 0 0 .971 0l9-5-.97-1.748z"></path></svg>              </div>
                <div>
                  <div class="text-blue-500">2370</div>
                  <div class="text-sm pt-1 text-gray-400">資產總額</div>
                </div>
              </div>
              <!--無風險資產數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-4 border border-gray-300">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill:rgb(132 204 22);transform: ;msFilter:;"><path d="M12 2C6.486 2 2 6.486 2 12s4.486 10 10 10 10-4.486 10-10S17.514 2 12 2zm0 18c-4.411 0-8-3.589-8-8s3.589-8 8-8 8 3.589 8 8-3.589 8-8 8z"></path><path d="M9.999 13.587 7.7 11.292l-1.412 1.416 3.713 3.705 6.706-6.706-1.414-1.414z"></path></svg>
                </div>
                <div>
                  <div class="text-lime-500">2370</div>
                  <div class="text-sm pt-1 text-gray-400">無風險資產數</div>
                </div>
              </div>
              <!--低風險資產數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-4 border border-gray-300">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill:rgb(132 204 22);transform: ;msFilter:;"><path d="M12 2C6.486 2 2 6.486 2 12s4.486 10 10 10 10-4.486 10-10S17.514 2 12 2zm0 18c-4.411 0-8-3.589-8-8s3.589-8 8-8 8 3.589 8 8-3.589 8-8 8z"></path><path d="M9.999 13.587 7.7 11.292l-1.412 1.416 3.713 3.705 6.706-6.706-1.414-1.414z"></path></svg>
                </div>
                <div>
                  <div class="text-lime-500">822</div>
                  <div class="text-sm pt-1 text-gray-400">低風險資產數</div>
                </div>
              </div>
              <!--中風險資產數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-4 border border-gray-300">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill: rgb(248 113 113);transform: ;msFilter:;"><path d="M9.172 16.242 12 13.414l2.828 2.828 1.414-1.414L13.414 12l2.828-2.828-1.414-1.414L12 10.586 9.172 7.758 7.758 9.172 10.586 12l-2.828 2.828z"></path><path d="M12 22c5.514 0 10-4.486 10-10S17.514 2 12 2 2 6.486 2 12s4.486 10 10 10zm0-18c4.411 0 8 3.589 8 8s-3.589 8-8 8-8-3.589-8-8 3.589-8 8-8z"></path></svg>
                </div>
                <div>
                  <div class="text-red-400">832</div>
                  <div class="text-sm pt-1 text-gray-400">中風險資產數</div>
                </div>
              </div>
              <!--高風險資產數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-4 border border-gray-300">
                <div class="pr-2">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" style="fill: rgb(248 113 113);transform: ;msFilter:;"><path d="M9.172 16.242 12 13.414l2.828 2.828 1.414-1.414L13.414 12l2.828-2.828-1.414-1.414L12 10.586 9.172 7.758 7.758 9.172 10.586 12l-2.828 2.828z"></path><path d="M12 22c5.514 0 10-4.486 10-10S17.514 2 12 2 2 6.486 2 12s4.486 10 10 10zm0-18c4.411 0 8 3.589 8 8s-3.589 8-8 8-8-3.589-8-8 3.589-8 8-8z"></path></svg>
                </div>
                <div>
                  <div class="text-red-400">2370</div>
                  <div class="text-sm pt-1 text-gray-400">高風險資產數</div>
                </div>
              </div>
              <!--未稽核資產數-->
              <div class="flex items-center rounded-10 bg-gray-100 p-4 border border-gray-300 ">
                <div class="pr-2">
                  <div class="rounded-full border-4 border-gray-500 ">
                    <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" style="fill: rgb(107 114 128);transform: ;msFilter:;"><path d="M12 4C9.243 4 7 6.243 7 9h2c0-1.654 1.346-3 3-3s3 1.346 3 3c0 1.069-.454 1.465-1.481 2.255-.382.294-.813.626-1.226 1.038C10.981 13.604 10.995 14.897 11 15v2h2v-2.009c0-.024.023-.601.707-1.284.32-.32.682-.598 1.031-.867C15.798 12.024 17 11.1 17 9c0-2.757-2.243-5-5-5zm-1 14h2v2h-2z"></path></svg>
                  </div>
                </div>
                <div>
                  <div class="text-gray-400">2370</div>
                  <div class="text-sm pt-1 text-gray-400">未稽核資產數</div>
                </div>
              </div>
              <!--部門選擇器-->
              <div class="flex items-center rounded-10 text-center bg-gray-100 p-2 border border-gray-300">
                  <div>
                    <div class="text-gray-400">部門
                    
                    </div>
                    <div class="text-sm pt-1 text-gray-400">
                      <select class="p-2 rounded-10">
                        <option value="none" selected disabled hidden>全部</option> 
                        <option value ="taipei">台北市</option>
                        <option value ="Kaohsiung">高雄市</option>
                      </select>
                    </div>
                  </div>
              </div>
              <!--本部選擇器-->
              <div class="flex items-center rounded-10 text-center bg-gray-100 p-2 border border-gray-300">
                <div>
                  <div class="text-gray-400">本部
                  </div>
                  <div class="text-sm pt-1 text-gray-400">
                    <select class="p-2 rounded-10">
                      <option value="none" selected disabled hidden>選擇分站</option> 
                      <option value ="taipei">台北市</option>
                      <option value ="Kaohsiung">高雄市</option>
                    </select>
                  </div>
                </div>
              </div>
            <!-- </div> -->
          </div>
          <div class="flex gap-x-6  px-4 py-2 bg-gray-100 rounded-b-lg pb-4">
            <!--左側圖表-->
              <div class="flex w-2/5 flex-col gap-y-8"><!--w-3/5-->
              <div class="flex flex-col justify-between rounded-10 bg-gray-100 border border-gray-300 "><!-- p-7-->
                <h2 class="p-3 w-full text-gray-400">信任網址列表</h2>
                <div class="flex gap-x-8">
                  <img src="./image/VANS_1.png">
                </div>
              </div>
            </div>
            <div class="flex w-3/5 flex-col gap-y-8"><!--w-2/5-->
              <div class="flex flex-col justify-between rounded-10 bg-gray-100 border border-gray-300 p-4"><!--p-7-->
                <nav>
                    <select class="p-3 rounded-10 bg-white">
                      <option value="none" selected disabled hidden>資產數量排名</option> 
                      <option value ="unknow1">資產數量排名</option>
                      <option value ="unknow2">CVE總數排名</option>
                    </select>
                  </nav>
              <div class="flex gap-x-8 pt-2">
                <img src="./image/VANS_2.png" >
              </div>
              </div>
            </div>
          </div>
          </TabPanel>
        </TabPanels>
      </TabGroup>
    </main>
  </div>
</template>
