# Electronic Arts GraphQL Schema

## Overview

This is a conceptual GraphQL schema for Electronic Arts (EA) gaming and player services. Electronic Arts does not currently publish a public developer API portal; this schema is derived from known EA service surfaces including the EA app, Origin platform, EA SPORTS FC, FIFA Ultimate Team (FUT), EA Play subscription service, and partner integrations documented through reverse engineering and public research.

EA's backend services power player account management (Nucleus ID / Origin accounts), game entitlements, storefronts, achievements, leaderboards, match history, and the FIFA Ultimate Team marketplace. This schema models those surfaces in a unified GraphQL vocabulary.

## Schema Source

- **Source type:** Conceptual / community-derived
- **Based on:** EA app (formerly Origin), EA SPORTS FC / FIFA Ultimate Team APIs, EA Help services, partner program documentation, and public research
- **GitHub:** https://github.com/electronicarts
- **Developer site:** https://developer.ea.com (limited public access)

## Key Domains

### Player Identity and Accounts
Types covering EA's multi-layer identity system: `Player`, `PlayerProfile`, `PlayerID`, `EAID`, `OriginAccount`, `EAPlayer`, and `NucleusID`. EA uses a Nucleus ID as the internal canonical account identifier, with the Origin/EA app providing the consumer-facing account surface.

### Social and Presence
`FriendList`, `Friend`, `FriendStatus`, and `Presence` cover the social graph and real-time online presence signals exposed through the EA app.

### Game Catalog and Entitlements
`Game`, `GameTitle`, `GameRelease`, `GamePlatform`, `GameStatus`, `OwnedGame`, `Entitlement`, `EntitlementType`, `DLC`, `Expansion`, `Pack`, and `Bundle` model EA's game catalog and the entitlement system that tracks what content a player has access to across platforms.

### Store and Transactions
`PurchaseHistory`, `Transaction`, `StoreListing`, `StoreCategory`, `StoreFilter`, `Price`, `Currency`, `Discount`, and `Promotion` model the EA storefront and in-game purchase surfaces.

### Achievements and Progression
`Achievement`, `AchievementDetail`, `AchievementProgress`, and `Trophy` cover EA's cross-platform achievement and trophy systems.

### Leaderboards and Competitive
`Leaderboard`, `LeaderboardEntry`, `Score`, and `Rank` cover ranked and global leaderboard surfaces available across EA sports and competitive titles.

### Statistics and Match History
`Statistics`, `GameStatistics`, `PlayerStats`, `MatchHistory`, `Match`, `MatchDetail`, `MatchResult`, `MatchParticipant`, and `MatchScore` model per-game and per-match statistical data.

### FIFA Ultimate Team (FUT)
`FUT`, `FUTPlayer`, `FUTTeam`, `FUTSquad`, `FUTClub`, `FUTTransfer`, and `FUTMarket` model the FIFA / EA SPORTS FC Ultimate Team mode, including squad building, player cards, and the transfer market.

### Auth and API Access
`APIKey`, `Token`, and `OAuthToken` model EA's OAuth 2.0 token-based authentication used for partner and internal integrations.

## GraphQL File

See `electronic-arts-schema.graphql` for the full type definitions.
