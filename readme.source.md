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
      width: '84px',
      height: '84px',
      borderRadius: '50%',
      background: 'linear-gradient(135deg, #7aa2f7 0%, #bb9af7 55%, #ff9e64 100%)',
      alignItems: 'center',
      justifyContent: 'center',
    }}>
      <img
        src="https://github.com/yorushi-code.png"
        width="72"
        height="72"
        style={{
          width: '72px',
          height: '72px',
          borderRadius: '50%',
          border: '3px solid #1a1b26',
          objectFit: 'cover',
        }}
      />
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
    { label: 'Telegram', value: '@the_yorushi',             accent: '#7dcfff' },
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
      borderRight: i < 3 ? '1px solid #292e42' : 'none',
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

```aura width=820 height=245
<div style={{
  display: 'flex',
  alignItems: 'stretch',
  width: '100%',
  height: '100%',
  background: '#1a1b26',
  borderRadius: '18px',
  border: '1px solid #292e42',
  position: 'relative',
  overflow: 'hidden',
}}>
  <div style={{
    display: 'flex',
    position: 'absolute',
    bottom: '0',
    left: '0',
    right: '0',
    height: '3px',
    background: 'linear-gradient(90deg, #ff9e64 0%, #bb9af7 35%, #7aa2f7 65%, #414868 100%)',
  }} />

  <div style={{
    display: 'flex',
    flex: '1',
    flexDirection: 'column',
    padding: '20px 24px',
    gap: '14px',
    borderRight: '1px solid #292e42',
  }}>
    <div style={{ display: 'flex', alignItems: 'center', gap: '10px' }}>
      <div style={{
        display: 'flex',
        width: '4px',
        height: '16px',
        borderRadius: '2px',
        background: 'linear-gradient(180deg, #7aa2f7, #ff9e64)',
      }} />
      <span style={{
        fontSize: '13px',
        color: '#c0caf5',
        fontWeight: '700',
        letterSpacing: '1.2px',
        textTransform: 'uppercase',
      }}>
        Stats
      </span>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: '12px' }}>
      {[
        { label: 'Stars earned', value: github.stats.totalStars, color: '#e0af68' },
        { label: 'Member since', value: github.user.createdAt.slice(0, 4), color: '#9ece6a' },
        { label: 'Repositories', value: github.stats.totalRepos, color: '#7aa2f7' },
        { label: 'Forks', value: github.stats.totalForks, color: '#bb9af7' },
        { label: 'Followers', value: github.user.followers, color: '#ff9e64' },
        { label: 'Following', value: github.user.following, color: '#7dcfff' },
      ].map((row, i) => (
        <div key={i} style={{ display: 'flex', alignItems: 'center', gap: '10px' }}>
          <div style={{
            display: 'flex',
            width: '7px',
            height: '7px',
            borderRadius: '50%',
            background: row.color,
          }} />
          <span style={{ fontSize: '13px', color: '#787c99', flex: '1' }}>
            {row.label}
          </span>
          <span style={{ fontSize: '14px', color: row.color, fontWeight: '700' }}>
            {row.value}
          </span>
        </div>
      ))}
    </div>
  </div>

  <div style={{
    display: 'flex',
    flex: '1',
    flexDirection: 'column',
    padding: '20px 24px',
    gap: '14px',
  }}>
    <div style={{ display: 'flex', alignItems: 'center', gap: '10px' }}>
      <div style={{
        display: 'flex',
        width: '4px',
        height: '16px',
        borderRadius: '2px',
        background: 'linear-gradient(180deg, #bb9af7, #9ece6a)',
      }} />
      <span style={{
        fontSize: '13px',
        color: '#c0caf5',
        fontWeight: '700',
        letterSpacing: '1.2px',
        textTransform: 'uppercase',
      }}>
        Top languages
      </span>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: '11px' }}>
      {github.languages.slice(0, 5).map((lang, i) => {
        const palette = ['#7aa2f7', '#bb9af7', '#ff9e64', '#9ece6a', '#e0af68'];
        const tone = palette[i];
        return (
          <div key={lang.name} style={{ display: 'flex', flexDirection: 'column', gap: '5px' }}>
            <div style={{ display: 'flex', alignItems: 'center' }}>
              <span style={{ fontSize: '12px', color: '#c0caf5', fontWeight: '600', flex: '1' }}>
                {lang.name}
              </span>
              <span style={{ fontSize: '12px', color: tone, fontWeight: '700' }}>
                {lang.percentage}%
              </span>
            </div>
            <div style={{
              display: 'flex',
              width: '100%',
              height: '6px',
              borderRadius: '3px',
              background: '#16161e',
            }}>
              <div style={{
                display: 'flex',
                width: `${lang.percentage}%`,
                height: '6px',
                borderRadius: '3px',
                background: tone,
              }} />
            </div>
          </div>
        );
      })}
    </div>
  </div>
</div>
```
