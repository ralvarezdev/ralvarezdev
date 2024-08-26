```javascript
import React from "react"
import Language from "./components/Language"
import ProgrammingLanguage from "./components/ProgrammingLanguage"
import Framework from "./components/Framework"

const YEAR_OF_BIRTH = 2005

export default function Ralvarezdev() {
    const age = new Date().getFullYear() - YEAR_OF_BIRTH
    
    return (
        <>
            <div className="personal-info">
                <p className="personal-info__full-name">Ramón Álvarez</p>
                <p className="personal-info__age">{age}</p>
            </div>
            
            <div className="skills">
                {['English', 'Spanish'].map((language, index) => (
                    <Language key={index}>{language}</Language>
                ))}
                
                {['JavaScript', 'Python', 'C++', 'Go', 'Java'].map((skill, index) => (
                    <ProgrammingLanguage key={index}>{skill}</ProgrammingLanguage>
                ))}
            
                {['React'].map((framework, index) => (
                    <Framework key={index}>{framework}</Framework>
                ))}
            </div>
            
            <div className="academic-bg">
                <div className="academic-bg__in-progress">
                    <p className="degree">Computer Science at the Rafael Urdaneta University</p>
                </div>
            </div>
                
            
            <div className="social-media">
                <a href="https://github.com/ralvarezdev">GitHub</a>
                <a href="https://instagram.com/ralvarezdev">Instagram</a>
                <a href="https://leetcode.com/u/ralvarezdev">Leetcode</a>
            </div>
        </>
    )
}
```

<!--
So, I got your attention. Feel free to contact me if you want to talk about programming, technology, or anything else. I'm always open to new opportunities and collaborations.
-->