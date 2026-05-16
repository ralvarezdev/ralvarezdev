```go
package ralvarezdev

import "time"

type Proficiency uint8

const (
	Beginner     Proficiency = iota + 1
	Intermediate
	Advanced
)

type (
	Language    struct{ Name string; Proficiency Proficiency }
	Framework   struct{ Name, Ecosystem string }
	Degree      struct{ Field, Institution string }
	Position    struct{ Title, Company string; Since time.Time; Current bool }
	Competition struct{ Name string; Year int; Roles []string }
)

type Profile struct {
	Name, Email  string
	Bio          string
	Roles        []string
	Education    []Degree
	Languages    []Language
	Frameworks   []Framework
	Tools        map[string]Proficiency
	Standards    []string
	Hardware     []string
	Experience   []Position
	Competitions []Competition
	Links        map[string]string
}

var Ralvarezdev = Profile{
	Name:  "Ramón Álvarez",
	Email: "inquiries@ralvarez.dev",
	Bio:   "Backend engineer with a hands-on approach — from gRPC services and AI pipelines to embedded systems on Arduino and Raspberry Pi. I build things that work in the real world.",
	Roles: []string{"Software Engineer", "Backend Engineer"},

	Education: []Degree{
		{"Computer Engineering", "Rafael Urdaneta University"},
	},

	Languages: []Language{
		{"Go", Advanced}, {"Python", Advanced}, {"JavaScript/TypeScript", Advanced},
		{"C++", Intermediate}, {"Java", Intermediate},
		{"TinyGo", Intermediate}, {"CircuitPython", Intermediate}, {"MicroPython", Intermediate},
		{"Rust", Beginner},
	},

	Frameworks: []Framework{
		{"Gin", "Go"}, {"ConnectRPC", "Go"},
		{"ROS2", "Python"}, {"Pydantic V2", "Python"}, {"OpenCV", "Python"}, {"Pandas", "Python"}, {"YOLO", "Python"},
		{"React", "JavaScript"}, {"Angular", "TypeScript"},
	},

	Tools: map[string]Proficiency{
		"Docker": Advanced, "Docker Compose": Advanced,
		"Cloudflare": Intermediate, "Hailo AI": Intermediate,
	},

	Standards: []string{"REST", "gRPC", "NATS", "Protocol Buffers", "Protovalidate", "JWT", "MCP"},
	Hardware:  []string{"Raspberry Pi 5", "Arduino Mega", "Arduino"},

	Experience: []Position{
		{"Backend Engineer", "Automation Labs", time.Date(2025, time.October, 1, 0, 0, 0, 0, time.UTC), true},
		{"Backend Engineer Intern", "Automation Labs", time.Date(2025, time.August, 1, 0, 0, 0, 0, time.UTC), false},
	},

	Competitions: []Competition{
		{"WRO Future Engineers", 2026, []string{"Team Lead", "Programmer"}},
		{"WRO Future Engineers", 2025, []string{"Team Lead", "Programmer"}},
		{"ORC", 2025, []string{"Team Lead", "Programmer"}},
	},

	Links: map[string]string{
		"GitHub":    "https://github.com/ralvarezdev",
		"LinkedIn":  "https://www.linkedin.com/in/ralvarezdev/",
		"Instagram": "https://instagram.com/ralvarezdev",
		"LeetCode":  "https://leetcode.com/u/ralvarezdev",
		"Email":     "inquiries@ralvarez.dev",
	},
}
```

<!--
So, I got your attention. Feel free to contact me if you want to talk about programming, technology, or anything else. I'm always open to new opportunities and collaborations.
-->
