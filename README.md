# Props-

props-Read only properties shared between components.
It allows parent component to send data to child component.
In the form of key value pairs.

#propTypes
A mechanism that ensures that passed value of correct datatype.

#Default props
default values passed for props incase there is no value passsed by parent

//App.js
import Student from './Student.jsx';
function App()
{
   return (
   <Student name='Harshi'  age={22} isStudent={true}/>
   <Student name='Janu'  age={22} isStudent={false}/>
   <Student />   ----->Default props
   
   );
}






//Student.jsx
import propTypes from 'prop-Types';
functio Student(props)
{
return(
<div>
  <p>Name: {props.name}</p>
   <p>Age: {props.age}</p>
  <p>isStudent: {props.isStudent ? "Yes" : "No" }</p>
</div>
)
}
Student.propTypes = {
name: propTypes.string,
age: propTypes.number,
isStudent:propTypes.bool,
}
Student.defaultProps={
name:"JOhn",
age:30,
isStudent:true
}
