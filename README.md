# MGR Teknoloji Transfer Paketi Akış Diyagramı
'''flowchart TD
    Start[Sistemler] --> MGR[MGR Sistemi]
    Start --> MODES[MODE-S SSR Sistemi]
    
    MGR --> MGR_C{Müşteri DHMİ mi?}
    MODES --> MODES_C{Müşteri DHMİ mi?}
    
    %% MGR Normal Satış
    MGR_C -->|Evet| MGR_NS1[Normal Satış]
    MGR_C -->|Hayır| MGR_NS2[Normal Satış]
    
    MGR_NS1 --> MGR_E[Ruhsat/Lisans bedeli ve
    Teknoloji Transfer bedeli
    satış bedeline yansıtılmaz]
    
    MGR_NS2 --> MGR_F[Satış bedelinin maksimum %15'i
    kadar ruhsat/lisans bedeli
    DHMİ'ye ödenir]
    
    %% MGR Teknoloji Transferi
    MGR_C --> |Evet| MGR_TT1[Teknoloji Transferi]
    MGR_C --> |Hayır| MGR_TT2[Teknoloji Transferi]
    
    MGR_TT1 --> MGR_I[Transfer bedeli yansıtılmaz 
    TÜBİTAK BİLGEM bedel talep etmez 
    DHMİ'ye bedel aktarılmaz]
    
    MGR_TT2 --> MGR_J[TÜBİTAK BİLGEM gelirinin %50'si
    DHMİ'ye aktarılır
    10 iş günü içinde ödenir]

    %% MODE-S Normal Satış
    MODES_C -->|Evet| MODES_NS1[Normal Satış]
    MODES_C -->|Hayır| MODES_NS2[Normal Satış]
    
    MODES_NS1 --> MODES_E[Ruhsat/Lisans bedeli ve
    Teknoloji Transfer bedeli
    satış bedeline yansıtılmaz]
    
    MODES_NS2 --> MODES_F[Satış bedelinin maksimum %15'i
    kadar ruhsat/lisans bedeli
    DHMİ'ye ödenir]
    
    %% MODE-S Teknoloji Transferi
    MODES_C --> |Evet| MODES_TT1[Teknoloji Transferi]
    MODES_C --> |Hayır| MODES_TT2[Teknoloji Transferi]
    
    MODES_TT1 --> MODES_I[Transfer bedeli yansıtılmaz
    TÜBİTAK BİLGEM bedel talep etmez
    DHMİ'ye bedel aktarılmaz]
    
    MODES_TT2 --> MODES_J[TÜBİTAK BİLGEM gelirinin %50'si
    DHMİ'ye aktarılır
    10 iş günü içinde ödenir]


