```aura width=820 height=220
<div style={{
  display: 'flex',
  flexDirection: 'column',
  alignItems: 'center',
  justifyContent: 'center',
  width: '100%',
  height: '100%',
  background: 'linear-gradient(135deg, #16161e 0%, #1a1b26 55%, #0d0d14 100%)',
  borderRadius: '18px',
  border: '1px solid #292e42',
  gap: '18px',
  position: 'relative',
  overflow: 'hidden',
}}>
  <div style={{
    display: 'flex',
    position: 'absolute',
    top: '0',
    left: '0',
    right: '0',
    height: '3px',
    background: 'linear-gradient(90deg, #414868 0%, #7aa2f7 35%, #bb9af7 65%, #ff9e64 100%)',
  }} />

  <div style={{
    display: 'flex',
    position: 'absolute',
    top: '-90px',
    right: '-70px',
    width: '260px',
    height: '260px',
    borderRadius: '50%',
    background: 'radial-gradient(circle, rgba(255,158,100,0.10) 0%, transparent 70%)',
  }} />

  <div style={{
    display: 'flex',
    position: 'absolute',
    bottom: '-110px',
    left: '-60px',
    width: '260px',
    height: '260px',
    borderRadius: '50%',
    background: 'radial-gradient(circle, rgba(122,162,247,0.09) 0%, transparent 70%)',
  }} />

  <div style={{
    display: 'flex',
    alignItems: 'center',
    gap: '22px',
  }}>
    <div style={{
      display: 'flex',
      width: '80px',
      height: '80px',
      borderRadius: '50%',
      background: 'linear-gradient(135deg, #7aa2f7 0%, #bb9af7 55%, #ff9e64 100%)',
      alignItems: 'center',
      justifyContent: 'center',
    }}>
      <div style={{
        display: 'flex',
        width: '73px',
        height: '73px',
        borderRadius: '50%',
        overflow: 'hidden',
        border: '3px solid #1a1b26',
      }}>
        <img src="https://github.com/yorushi-code.png" style={{ width: '73px', height: '73px' }} />
      </div>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: '6px' }}>
      <span style={{
        fontSize: '40px',
        fontWeight: '700',
        color: '#c0caf5',
        letterSpacing: '-1px',
      }}>
        yorushi
      </span>
      <span style={{
        fontSize: '13px',
        color: '#7aa2f7',
        fontWeight: '600',
        letterSpacing: '2px',
        textTransform: 'uppercase',
      }}>
        systems · networking · linux
      </span>
    </div>
  </div>

  <div style={{ display: 'flex', gap: '9px' }}>
    {[
      { tag: 'rust',   bg: 'rgba(255,158,100,0.12)', border: '#ff9e64', color: '#ff9e64' },
      { tag: 'python', bg: 'rgba(122,162,247,0.12)', border: '#7aa2f7', color: '#7aa2f7' },
      { tag: 'c++',    bg: 'rgba(187,154,247,0.12)', border: '#bb9af7', color: '#bb9af7' },
      { tag: 'linux',  bg: 'rgba(158,206,106,0.12)', border: '#9ece6a', color: '#9ece6a' },
    ].map(({ tag, bg, border, color }) => (
      <div key={tag} style={{
        display: 'flex',
        padding: '5px 16px',
        borderRadius: '999px',
        background: bg,
        border: `1px solid ${border}`,
        color: color,
        fontSize: '12px',
        fontWeight: '700',
        letterSpacing: '1px',
        textTransform: 'uppercase',
      }}>
        {tag}
      </div>
    ))}
  </div>
</div>
```

```aura width=820 height=120
<div style={{
  display: 'flex',
  alignItems: 'stretch',
  width: '100%',
  height: '100%',
  background: '#1a1b26',
  borderRadius: '18px',
  border: '1px solid #292e42',
  overflow: 'hidden',
}}>
  {[
    { label: 'Email',    value: 'yorushi.code@hotmail.com', accent: '#9ece6a' },
    { label: 'GitHub',   value: '@yorushi-code',            accent: '#7aa2f7' },
    { label: 'Location', value: 'somewhere after midnight', accent: '#ff9e64' },
  ].map((item, i) => (
    <div key={i} style={{
      display: 'flex',
      flex: '1',
      flexDirection: 'column',
      alignItems: 'center',
      justifyContent: 'center',
      gap: '8px',
      borderRight: i < 2 ? '1px solid #292e42' : 'none',
      position: 'relative',
      overflow: 'hidden',
    }}>
      <div style={{
        display: 'flex',
        position: 'absolute',
        bottom: '0',
        left: '18%',
        right: '18%',
        height: '2px',
        background: item.accent,
        borderRadius: '2px',
        opacity: '0.55',
      }} />

      <span style={{
        fontSize: '11px',
        color: '#565f89',
        fontWeight: '700',
        letterSpacing: '1.4px',
        textTransform: 'uppercase',
      }}>
        {item.label}
      </span>

      <span style={{
        fontSize: '14px',
        color: item.accent,
        fontWeight: '600',
      }}>
        {item.value}
      </span>
    </div>
  ))}
</div>
```

```aura width=820 height=215
<div style={{
  display: 'flex',
  flexDirection: 'column',
  width: '100%',
  height: '100%',
  background: '#1a1b26',
  borderRadius: '18px',
  border: '1px solid #292e42',
  padding: '22px 24px',
  gap: '16px',
}}>
  <div style={{ display: 'flex', alignItems: 'center', gap: '10px' }}>
    <div style={{
      display: 'flex',
      width: '4px',
      height: '18px',
      borderRadius: '2px',
      background: 'linear-gradient(180deg, #7aa2f7, #ff9e64)',
    }} />
    <span style={{
      fontSize: '15px',
      color: '#c0caf5',
      fontWeight: '700',
      letterSpacing: '1.2px',
      textTransform: 'uppercase',
    }}>
      Selected work
    </span>
  </div>

  <div style={{ display: 'flex', gap: '14px' }}>
    {[
      {
        name: 'ddnet_proxy',
        lang: 'Rust',
        accent: '#ff9e64',
        desc: 'Async UDP proxy on Tokio — per-client sessions, idle timeouts, hex-dump tracing',
      },
      {
        name: 'yandex-extension',
        lang: 'JavaScript',
        accent: '#e0af68',
        desc: 'DJ toolset for Yandex Music — waveform, hot cues, BPM and Camelot wheel',
      },
      {
        name: 'migrate_to_niri',
        lang: 'Shell',
        accent: '#9ece6a',
        desc: 'Full desktop migration to the niri Wayland compositor',
      },
    ].map((p, i) => (
      <div key={i} style={{
        display: 'flex',
        flex: '1',
        flexDirection: 'column',
        gap: '9px',
        padding: '16px',
        borderRadius: '12px',
        background: '#16161e',
        border: '1px solid #292e42',
      }}>
        <div style={{ display: 'flex', alignItems: 'center', gap: '7px' }}>
          <div style={{
            display: 'flex',
            width: '8px',
            height: '8px',
            borderRadius: '50%',
            background: p.accent,
          }} />
          <span style={{ fontSize: '11px', color: p.accent, fontWeight: '700', letterSpacing: '0.6px' }}>
            {p.lang}
          </span>
        </div>

        <span style={{ fontSize: '15px', color: '#c0caf5', fontWeight: '700' }}>
          {p.name}
        </span>

        <span style={{ fontSize: '11px', color: '#787c99', lineHeight: '1.5' }}>
          {p.desc}
        </span>
      </div>
    ))}
  </div>
</div>
```

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=yorushi-code&show_icons=true&theme=tokyonight&hide_border=true&bg_color=1a1b26&title_color=7aa2f7&icon_color=ff9e64&text_color=c0caf5&border_radius=18&include_all_commits=true&count_private=true" height="170" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=yorushi-code&layout=compact&theme=tokyonight&hide_border=true&bg_color=1a1b26&title_color=7aa2f7&text_color=c0caf5&border_radius=18&langs_count=8" height="170" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=yorushi-code&theme=tokyonight&hide_border=true&background=1a1b26&ring=ff9e64&fire=ff9e64&currStreakLabel=7aa2f7&border_radius=18" height="170" />
</p>
