```rs
use std::collections::HashMap;
use std::env;
use GitHub::GitUser;

enum GitValues {
    Aliases(Vec<&str>),
    Contact(HashMap<&'static str, &'static str>),
    ProgrammingLanguages(Vec<&str>),
    Interests(Vec<&str>),
}

fn user_info() -> HashMap<&'static str, GitValue> {
    HashMap::from([
        (
            "contact",
            GitValues::Contact(HashMap::from([(
                "email",
                "1305@national.shitposting.agency",
            )])),
        ),
        (
            "aliases",
            GitValues::Aliases(vec!["outsider1305", "Outsider", "1305", "13-05"]),
        ),
        (
            "programming-langages",
            GitValues::ProgrammingLanguages(vec!["Rust", "Python", "C#", "C++", "JavaScript"]),
        ),
        (
            "interests",
            GitValues::Interests(vec!["Malware", "Reverse Engineering", "APIs"]),
        ),
    ])
}

fn main() {
    let outsider1305 = GitUser::from(&user_info());
}
```
