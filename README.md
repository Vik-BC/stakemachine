# ⚙️ StakeMachine
### 📈 Торговый бот для децентрализованной биржи [RuDEX](https://market.rudex.org) ⛓




## 🔌 Установка

    git clone https://github.com/vikxx/stakemachine
    cd stakemachine
    python3 setup.py install
    

## 🔧 Конфигурация

Отредактируйте файл `config.yml` (пример содержания в файле `config-example.yml`) 
Вы можете комбинировать стратегии торгов, аккаунты, пары и многое другое.

```
witness_url: "wss://node.market.rudex.org"
prefix: "BTS"
safe_mode: True
account: "v0id"
wif: "5*************************************************"

market_separator: ":"

reserves:
 BTS: 1000
 RUBLE: 200

bots:
    MakerWallBitAssets:
        module: "stakemachine.strategies.maker"
        bot: "MakerSellBuyWalls"
        markets:
            - "RUBLE:BTS"
        target_price: "last"
        target_price_offset_percentage: 1
        spread_percentage: 5
        volume_percentage: 50
        symmetric_sides: True
        only_buy: False
        only_sell: False
```

## ⌨️ Команды 
* `stakemachine run` Запуск
* `stakemachine once` Единичный запуск
* `stakemachine cancel_all` Отмена ордеров и остановка работы

☣️ **Warning**: This is highly experimental code! Use at your OWN risk!
☣️ **Внимание**: Это экспериментальный код! Автор не несет ответсвенности за неправильное использование!

# 📃 IMPORTANT NOTE

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.
