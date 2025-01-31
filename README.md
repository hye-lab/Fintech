#핀테크 짱짱

##안녕하세요

### 헤딩3

```
Stay hungry, stay foolish
```

import React from 'react';
import { Github, Linkedin, Mail, Users } from 'lucide-react';

const TeamPage = () => {
  const teamMembers = [
    {
      name: 'Sarah Chen',
      role: 'Team Lead',
      skills: ['Project Management', 'Strategy', 'Team Building'],
      bio: 'With over 8 years of experience in tech leadership, Sarah drives innovation and team excellence.',
      image: '/api/placeholder/300/300'
    },
    {
      name: 'Michael Rodriguez',
      role: 'Senior Developer',
      skills: ['Full Stack', 'Architecture', 'Mentoring'],
      bio: 'A passionate coder with a keen eye for clean architecture and scalable solutions.',
      image: '/api/placeholder/300/300'
    },
    {
      name: 'Emily Watson',
      role: 'UI/UX Designer',
      skills: ['User Research', 'Prototyping', 'Visual Design'],
      bio: 'Creating beautiful and intuitive user experiences through research-driven design.',
      image: '/api/placeholder/300/300'
    },
    {
      name: 'David Kim',
      role: 'Backend Developer',
      skills: ['Database Design', 'API Development', 'Security'],
      bio: 'Specialized in building robust and secure backend systems that scale.',
      image: '/api/placeholder/300/300'
    }
  ];

  return (
    <div className="min-h-screen bg-gray-50">
      {/* Header Section */}
      <header className="bg-indigo-600 text-white py-20">
        <div className="container mx-auto px-6 text-center">
          <Users className="w-16 h-16 mx-auto mb-6" />
          <h1 className="text-4xl font-bold mb-4">Meet Our Team</h1>
          <p className="text-xl max-w-2xl mx-auto">
            We're a diverse group of passionate individuals working together to create amazing solutions.
          </p>
        </div>
      </header>

      {/* Team Values Section */}
      <section className="py-16 bg-white">
        <div className="container mx-auto px-6">
          <h2 className="text-3xl font-bold text-center mb-12">Our Values</h2>
          <div className="grid md:grid-cols-3 gap-8">
            <div className="text-center p-6">
              <h3 className="text-xl font-semibold mb-3">Innovation</h3>
              <p className="text-gray-600">
                We constantly push boundaries and explore new technologies to deliver cutting-edge solutions.
              </p>
            </div>
            <div className="text-center p-6">
              <h3 className="text-xl font-semibold mb-3">Collaboration</h3>
              <p className="text-gray-600">
                We believe in the power of teamwork and open communication to achieve exceptional results.
              </p>
            </div>
            <div className="text-center p-6">
              <h3 className="text-xl font-semibold mb-3">Excellence</h3>
              <p className="text-gray-600">
                We strive for excellence in everything we do, from code quality to user experience.
              </p>
            </div>
          </div>
        </div>
      </section>

      {/* Team Members Section */}
      <section className="py-16">
        <div className="container mx-auto px-6">
          <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
            {teamMembers.map((member, index) => (
              <div key={index} className="bg-white rounded-lg shadow-md overflow-hidden">
                <img
                  src={member.image}
                  alt={member.name}
                  className="w-full h-64 object-cover"
                />
                <div className="p-6">
                  <h3 className="text-xl font-semibold mb-2">{member.name}</h3>
                  <p className="text-indigo-600 mb-3">{member.role}</p>
                  <p className="text-gray-600 mb-4">{member.bio}</p>
                  <div className="space-y-2">
                    {member.skills.map((skill, skillIndex) => (
                      <span
                        key={skillIndex}
                        className="inline-block bg-gray-100 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
                      >
                        {skill}
                      </span>
                    ))}
                  </div>
                  <div className="mt-4 flex space-x-4">
                    <Mail className="w-5 h-5 text-gray-500 hover:text-indigo-600 cursor-pointer" />
                    <Github className="w-5 h-5 text-gray-500 hover:text-indigo-600 cursor-pointer" />
                    <Linkedin className="w-5 h-5 text-gray-500 hover:text-indigo-600 cursor-pointer" />
                  </div>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Team Stats Section */}
      <section className="bg-indigo-600 text-white py-16">
        <div className="container mx-auto px-6">
          <div className="grid md:grid-cols-4 gap-8 text-center">
            <div>
              <h4 className="text-4xl font-bold mb-2">15+</h4>
              <p>Projects Completed</p>
            </div>
            <div>
              <h4 className="text-4xl font-bold mb-2">8</h4>
              <p>Team Members</p>
            </div>
            <div>
              <h4 className="text-4xl font-bold mb-2">24/7</h4>
              <p>Support</p>
            </div>
            <div>
              <h4 className="text-4xl font-bold mb-2">98%</h4>
              <p>Client Satisfaction</p>
            </div>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section className="py-16 bg-white">
        <div className="container mx-auto px-6 text-center">
          <h2 className="text-3xl font-bold mb-8">Want to Work With Us?</h2>
          <p className="text-gray-600 mb-8 max-w-2xl mx-auto">
            We're always looking for talented individuals to join our team. 
            Let's create something amazing together.
          </p>
          <button className="bg-indigo-600 text-white px-8 py-3 rounded-lg font-semibold hover:bg-indigo-700 transition-colors">
            Join Our Team
          </button>
        </div>
      </section>
    </div>
  );
};

export default TeamPage;
