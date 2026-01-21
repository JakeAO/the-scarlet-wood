# OpenCode Skills Directory

This directory contains specialized skills for managing The Scarlet Wood campaign hub using OpenCode.

## Available Skills

### Content Creation
- **create-session**: Generate session summary articles with proper Jekyll formatting
- **create-npc**: Create character articles with token images and cross-references
- **create-faction**: Generate faction articles with member lists and values
- **create-organization**: Create organization and enemy group articles
- **create-enemy**: Generate antagonist character articles with threat assessments
- **create-info**: Create world building and rules articles

### Content Management
- **campaign-sync**: Synchronize cross-references and maintain content consistency
- **content-batch**: Batch process content creation from CSV data or templates
- **update-links**: Validate and update internal links between articles
- **campaign-analytics**: Analyze character relationships, faction dynamics, and narrative patterns

### Technical Operations
- **jekyll-build**: Validate Jekyll builds and preview content changes locally
- **media-manager**: Organize campaign images, generate character tokens, validate asset references
- **git-workflow**: Manage Git operations with proper commit messages and branching

### Guidance
- **content-guide**: Comprehensive documentation for content creation best practices

## Usage Examples

### Quick Session Creation
```
/skill({ name: "create-session" })
```

### Batch Character Generation
```
/skill({ name: "content-batch" })
```

### Campaign Analysis
```
/skill({ name: "campaign-analytics" })
```

### Build Validation
```
/skill({ name: "jekyll-build" })
```

### Content Synchronization
```
/skill({ name: "campaign-sync" })
```

## Skill Categories

### For Content Writers
- Create new articles quickly using templates
- Maintain consistent formatting across all content
- Generate cross-references automatically
- Follow Jekyll best practices

### For Campaign Managers
- Analyze campaign health and relationships
- Manage publication workflows
- Coordinate collaborative development
- Generate analytics and insights

### For Technical Operations
- Validate Jekyll builds and catch errors early
- Manage media assets and organization
- Handle Git operations with proper conventions
- Automate repetitive content tasks

## Integration Workflow

### Creating New Content
1. Use appropriate creation skill (session, npc, faction, etc.)
2. Apply campaign-sync to update cross-references
3. Validate with jekyll-build before publication
4. Commit changes using git-workflow skill

### Updating Existing Content
1. Analyze with campaign-analytics to understand impact
2. Use update-links to maintain link integrity
3. Batch update with content-batch if multiple changes
4. Test and commit using specialized skills

### Content Maintenance
1. Run campaign-sync periodically for consistency
2. Use media-manager to organize assets
3. Generate analytics reports with campaign-analytics
4. Perform jekyll-build validation before major updates

## Best Practices

### Content Creation
- Always start with draft status (`published: false`)
- Include comprehensive cross-references
- Follow established naming conventions
- Use proper Jekyll `relative_url` filter for all internal links

### Campaign Management
- Maintain character consistency across all articles
- Track faction relationships and power dynamics
- Keep session chronology accurate and sequential
- Document campaign themes and moral axis movements

### Technical Operations
- Validate builds before each publication
- Use consistent Git commit messages
- Organize media assets systematically
- Generate analytics for informed decision-making

These skills work together to create a comprehensive campaign management system for The Scarlet Wood Jekyll hub, enabling efficient content creation, maintenance, and publication workflows.