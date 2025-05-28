- name: Deploy
  run: |
    ssh -o StrictHostKeyChecking=no ubuntu@54.123.45.67 << 'EOF'
      cd /var/www/your-app
      git pull origin main
      sudo systemctl restart your-service
    EOF
