# Kener Status Page - Zeabur Template

A sleek, modern status page deployment template for [Zeabur](https://zeabur.com) using [Kener](https://kener.ing/) and PostgreSQL.

[![Deploy to Zeabur](https://zeabur.com/button.svg)](https://zeabur.com/templates/TXURD9)

## 🚀 Quick Deploy

Click the deploy button above or use the Zeabur CLI:

```bash
zeabur auth login
zeabur template deploy --url https://zeabur.com/templates/TXURD9
```

## 📋 Template Variables

When deploying, you'll need to configure these variables:

| Variable | Type | Description |
|----------|------|-------------|
| `PUBLIC_DOMAIN` | DOMAIN | Your status page domain (e.g. status.example.com) |
| `KENER_SECRET_KEY` | PASSWORD | Strong random secret for encryption |
| `ORIGIN` | STRING | Full origin URL (e.g. https://status.example.com) |
| `TZ` | STRING | Server timezone (e.g. Etc/UTC or Asia/Tokyo) |
| `POSTGRES_USER` | STRING | PostgreSQL username |
| `POSTGRES_PASSWORD` | PASSWORD | PostgreSQL password |
| `POSTGRES_DB` | STRING | PostgreSQL database name |

### Optional Email Notifications

Choose either SMTP or Resend for email alerts:

**SMTP Setup:**
- `ENABLE_SMTP`: Set to "yes" to enable SMTP
- `SMTP_HOST`: SMTP server hostname
- `SMTP_PORT`: Port number (465 or 587)
- `SMTP_USER`: SMTP username
- `SMTP_PASS`: SMTP password

**Or Resend Setup:**
- `RESEND_API_KEY`: Your Resend API key
- `RESEND_SENDER_EMAIL`: Sender email address

## 🛠 Local Development

Want to modify the template? Clone this repo and edit `kener_template.yaml`:

```bash
git clone https://github.com/wari-sul/kener-status-zeabur.git
cd kener-status-zeabur

# Edit kener_template.yaml with your customizations
zeabur template deploy --file kener_template.yaml
```

## 📁 Repository Structure

```
📦 kener-zeabur-template/
├── kener_template.yaml      # Main deployment template
├── README.md          # This file
└── LICENSE
```

## 🔧 What's Included

- **Kener**: Modern open-source status page system
- **PostgreSQL**: Robust database backend with pgvector support
- **Custom Domain**: Easy domain binding
- **Email Notifications**: SMTP or Resend integration
- **Modern UI**: Clean, responsive status page design
- **Monitoring**: Built-in uptime monitoring capabilities

## 📊 After Deployment

Once deployed, you can:

1. **Access Dashboard**: Visit your configured domain
2. **Set Up Monitors**: Add services/websites to monitor
3. **Customize Pages**: Configure appearance and branding
4. **Test Notifications**: Verify email alerts work
5. **Add Categories**: Organize your monitored services

## 🔒 Security Notes

- Generate a strong `KENER_SECRET_KEY` (use `openssl rand -base64 32`)
- Use HTTPS for your domain (if using custom domain)
- Consider adding authentication if needed
- Regularly update the Kener image

## 🚀 Next Steps

After deploying:

1. Clone your GitHub repo
2. Customize the template for your needs
3. Push changes to re-deploy
4. Share your status page!

## 🤝 Contributing

Feel free to submit issues or pull requests to improve this template!

## 📚 More Resources

- [Zeabur Documentation](https://zeabur.com/docs)
- [Kener Documentation](https://docs.kener.ing/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/16/)
- [Template Schema Reference](https://schema.zeabur.app/template.json)
