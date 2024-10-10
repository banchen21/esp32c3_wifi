# use crate
```toml
[dependencies]
esp32c3_wifi = "0.1.2"
```
# use conn wifi
```rust
    esp_idf_svc::sys::link_patches();
    esp_idf_svc::log::EspLogger::initialize_default();

    let peripherals = Peripherals::take().unwrap();
    let sysloop = EspSystemEventLoop::take()?;

    let ssid = "test";
    let pass = "";
    let auth_method = AuthMethod::None;
    let _wifi = wifi(ssid, pass, auth_method, peripherals.modem, sysloop)?;
```
