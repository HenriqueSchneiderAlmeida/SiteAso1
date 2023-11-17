# SiteAso1

   name: Deploy via ftp
      on: push
      jobs:
        deploy:
          name: Deploy
          runs-on: ubuntu-latest
          steps:
          - uses: actions/checkout@v2

          - name: FTP Deploy Locaweb
            uses: locaweb/ftp-deploy@1.0.0
            with:
              host: ${{ ftp.asoemdia.com.br.HOST }} 
              user: ${{ asoemdia1.USER }}
              password: ${{ Chacau#Cigano16.PASS }}
              localDir: "dist"
