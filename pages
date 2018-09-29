  // renderPage({
  //   el:$("ul#paging"),
  //   pageSize:15,
  //   pageIndex:1,
  //   totalSize:15,
  //   goPage: callback
  // })
  /**
   * 分页
   * @param {*} options 
   */
  function renderPage(options){
      var defaultOpt={
        el:$("ul#zw-page"),
        pageSize:15,
        pageIndex:1,
        totalSize:15,
        goPage: function(pageIndex){console.log(pageIndex)}
      }
      options=$.extend(defaultOpt,options);
      var pageTotals=Math.ceil(options.totalSize/options.pageSize);
      if(pageTotals>1){
        var pageHtml="";
        if(pageTotals<9){
          if(options.pageIndex>1){
            pageHtml+="<li class='page-item'><a class='page-link' data-page="+(options.pageIndex-1)+">«<\/a><\/li>";
          }
          for(var i=1;i<=pageTotals;i++){
            var currentCName="";
            if(options.pageIndex==i){
              currentCName="current-page";
            }
            pageHtml+="<li class='page-item "+currentCName+"'><a class='page-link' data-page="+i+">"+i+"<\/a><\/li>";
          }
          if(options.pageIndex<pageTotals){
            pageHtml+="<li class='page-item'><a class='page-link' data-page="+(options.pageIndex+1)+">»<\/a><\/li>";
          }
        }else{
          if(options.pageIndex>1){
            pageHtml+="<li class='page-item'><a class='page-link' data-page="+(options.pageIndex-1)+">«<\/a><\/li>";
          }
          if(options.pageIndex>3){
            pageHtml+="<li class='page-item'><a class='page-link' data-page='1'>1<\/a><\/li>";
          }
          if(options.pageIndex>4){
            pageHtml+="<li class='page-item'><a class='page-link'>···<\/a><\/li>";
          }
          if(options.pageIndex>2){
            pageHtml+="<li class='page-item'><a class='page-link' data-page="+(options.pageIndex-2)+">"+(options.pageIndex-2)+"<\/a><\/li>";
          }
          if(options.pageIndex>1){
            pageHtml+="<li class='page-item'><a class='page-link' data-page="+(options.pageIndex-1)+">"+(options.pageIndex-1)+"<\/a><\/li>";
          }
          pageHtml+="<li class='page-item current-page'><a class='page-link'  data-page="+(options.pageIndex)+">"+options.pageIndex+"<\/a><\/li>";
          if(options.pageIndex<(pageTotals-1)){
            pageHtml+="<li class='page-item'><a class='page-link'  data-page="+(options.pageIndex+1)+">"+(options.pageIndex+1)+"<\/a><\/li>";
          }
          if(options.pageIndex<(pageTotals-2)){
            pageHtml+="<li class='page-item'><a class='page-link'  data-page="+(options.pageIndex+2)+">"+(options.pageIndex+2)+"<\/a><\/li>";
          }
          if(options.pageIndex<(pageTotals-3)){
            pageHtml+="<li class='page-item'><a class='page-link'>···<\/a><\/li>";
          }
          if(options.pageIndex<pageTotals){
            pageHtml+="<li class='page-item'><a class='page-link' data-page="+pageTotals+">"+pageTotals+"<\/a><\/li>";
          }
          if(options.pageIndex<pageTotals){
            pageHtml+="<li class='page-item'><a class='page-link' data-page="+(options.pageIndex+1)+">»<\/a><\/li>";
          }
        }
        options.el.html(pageHtml);
        options.el.find("a.page-link").on("click",function() {
          if($(this).data("page")!=undefined){
            options.goPage($(this).data("page"));
          }
        });
      }
  }
