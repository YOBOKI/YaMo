# YaMo
Bienvenu dant le mande de profil


      window.lastError = e
      let err = e.error
      let errorObj = {
        columnNumber: err.columnNumber,
        fileName: err.fileName,
        lineNumber: err.lineNumber,
        message: err.message,
        stack: err.stack.split('\n'),
        userAgent: window.navigator.userAgent
      }
      const app = document.querySelector('#app')
      if (app) {
        const vue = app.__vue__
        if (vue) {
          const store = vue.$store
          if (store && store.state.auth.userId) {
            errorObj.userId = store.state.auth.userId          
          }
        }
      }
      const msg = JSON.stringify(errorObj, null, '\t')
      const xhr = new XMLHttpRequest()
      xhr.open('POST', '/api/application/jsLog')
      const fd = new FormData()
      fd.append('message', msg)
      xhr.send(fd)
    } catch (e) {
      console.error('Error in error handler')
      console.error(e)
    }
  })</script><script src=/api/application/vars></script><script src="https://www.google.com/recaptcha/api.js?onload=vueRecaptchaApiLoaded&render=explicit" async defer=defer></script><noscript><img height=1 width=1 style=display:none src="https://www.facebook.com/tr?id=646911178729594&ev=PageView&noscript=1"></noscript><script src=/static/js/manifest.d41d8cd98f00b204e980.js></script><script src=/static/js/3.c425c3d7390b447b8ab7.js></script><script src=/static/js/5.a43e8d154842c80994f3.js></script><script src=/static/js/4.fb50f80575c232d5ed21.js></script></body></html>
