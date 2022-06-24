module.css unique className'ler ürettiği için istenmeyen stil ezilmeleri olmaz.

import Button from "../button/Button";
import cardStyle from "./card.module.css"

const Card = ({img,btnName,dil}) => {
  return (
    <div>
    <h1 className={cardStyle["title"]}>{dil}</h1>
    <img className={cardStyle["images"]} src={img} alt="img" />
    <Button btnName={btnName} />
    </div>
  )
}

export default Card;


Eger CSS'deki class adi kebap-case seklinde yazilmis ise module ile bu class'a erismek icin ornekte goruldugu gibi koseli parentez ile erisim yapilir. Koseli parentez erisimi en garanti yontemdir.

//*.ORN: moduleName["class-adi"]

import btnStyle from "./button.module.css"

const Button = ({btnName}) => {
  return (
    <div className={btnStyle.title}>
    <button className={btnStyle["btn-blue"]}>{btnName}
    </button></div>
    
  )
}

export default Button;