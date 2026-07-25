---
name: ooux-designer
description: Apply Object-Oriented UX (OOUX) principles using the ORCA framework (Objects, Relationships, CTAs, Attributes) to design user-centered features and interfaces
---

# Generic OOUX Skill

This skill guides you to apply Object-Oriented UX principles systematically when designing features, components, or systems.

## When to Use This Skill

Apply OOUX principles when:
- Designing new features or components
- Modeling data structures or database schemas
- Creating UI component hierarchies
- Planning API endpoints and resources
- Refactoring existing systems for better object modeling

## The ORCA Process

Follow these steps in order:

### 1. Objects (O)
**Define the core "things" in your system**
- Identify nouns from requirements (User, Product, Order, etc.)
- Use singular names, be specific and concrete
- Distinguish core objects (central to purpose) from supporting objects
- Avoid making actions into objects

### 2. Relationships (R)
**Map how objects connect**
- Define cardinality: One-to-One (1:1), One-to-Many (1:M), Many-to-Many (M:M)
- Label relationships clearly (e.g., "User creates Posts")
- Consider bidirectional relationships
- Identify parent-child hierarchies

### 3. Calls-to-Action (C)
**Define actions users can perform**
- Start with CRUD: Create, Read, Update, Delete
- Add object-specific actions (Publish, Archive, Share)
- Include relationship actions (Follow, Assign, Join)
- Consider user roles and permissions
- Map state transitions (Draft → Published)

### 4. Attributes (A)
**Specify object properties**
- Core attributes: Essential properties (email, username)
- Descriptive attributes: Additional info (description, color)
- System attributes: Metadata (created_at, id, status)
- Relational attributes: Foreign keys (author_id, category_id)
- Computed attributes: Derived values (total_price, age)

### 5. Output
**Generate deliverables**
- Create Mermaid.js diagram showing objects and relationships
- Define database schema (tables, columns, foreign keys)
- Map to API design (resources, endpoints, methods)
- Structure UI components based on object model

## Core Rules

- **Object-first thinking**: Always start with objects before features or functions
- **Consistency**: Objects map directly to database tables, API resources, and UI components
- **User-driven**: Let user needs drive object discovery
- **Validation**: Test your model against real-world scenarios
- **Simplicity**: Keep the model understandable; add complexity only when needed

## Common Mistakes to Avoid

- ❌ Making actions into objects (e.g., "Login" is not an object)
- ❌ Using vague names like "Item" or "Thing"
- ❌ Creating objects with no relationships to others
- ❌ Adding attributes that should be separate objects
- ❌ Ignoring how objects change state over time

## Reference Materials

For detailed guidance, see:
- `docs/orca-framework.md` - Complete ORCA methodology with examples
- `docs/examples.md` - Real-world patterns (e-commerce, task management, blog, LMS)
- `docs/ux-states-reference.md` - Three UX implementation approaches (Platform, Services, Phases)
- `docs/How we OOUX in ZeroTrust.pdf` - Production implementation reference

## Integration Patterns

**Database Schema:**
- Objects → Tables
- Attributes → Columns  
- Relationships → Foreign Keys / Junction Tables

**API Design:**
- Objects → Resources/Endpoints
- CTAs → HTTP Methods (GET, POST, PUT, DELETE)
- Attributes → Request/Response Fields

**UI Components:**
- Objects → Component Types
- CTAs → Buttons, Forms, Actions
- Attributes → Form Fields, Display Properties