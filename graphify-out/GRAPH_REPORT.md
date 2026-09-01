# Graph Report - freeReviewChessBot-main  (2026-09-01)

## Corpus Check
- 8 files · ~58,198 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 288 nodes · 697 edges · 21 communities (19 shown, 2 thin omitted)
- Extraction: 97% EXTRACTED · 3% INFERRED · 0% AMBIGUOUS · INFERRED: 18 edges (avg confidence: 0.58)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `839a7ea3`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- chess.js
- chessground.js
- app.js
- renderCircle
- callUserFunction
- handleReviewMove
- doMaiaResponse
- updateBoard
- render$1
- updateExplorer
- coachReset
- bindDocument
- configure
- stockfish.js
- getMaiaMove
- dependencies
- selectSquare
- Handler
- export_maia3.py
- speakText

## God Nodes (most connected - your core abstractions)
1. `doMaiaResponse()` - 20 edges
2. `updateBoard()` - 16 edges
3. `renderHistory()` - 13 edges
4. `handleReviewMove()` - 13 edges
5. `generate_moves()` - 13 edges
6. `callUserFunction()` - 13 edges
7. `coachReset()` - 12 edges
8. `setEngineStatus()` - 11 edges
9. `handleBranchMove()` - 11 edges
10. `dropNewPiece()` - 11 edges

## Surprising Connections (you probably didn't know these)
- `showPromotionPicker()` --indirect_call--> `p()`  [INFERRED]
  app.js → stockfish.js
- `analyzePositionalFactors()` --indirect_call--> `file()`  [INFERRED]
  app.js → chess.js
- `analyzePositionalFactors()` --indirect_call--> `f()`  [INFERRED]
  app.js → stockfish.js
- `computePlan()` --indirect_call--> `p()`  [INFERRED]
  chessground.js → stockfish.js
- `render$1()` --indirect_call--> `p()`  [INFERRED]
  chessground.js → stockfish.js

## Import Cycles
- None detected.

## Communities (21 total, 2 thin omitted)

### Community 0 - "chess.js"
Cohesion: 0.12
Nodes (40): algebraic(), ascii(), attacked(), clear(), clone(), file(), generate_fen(), generate_moves() (+32 more)

### Community 1 - "chessground.js"
Cohesion: 0.11
Nodes (11): canDrop(), computeSquareCenter(), customSvgHash(), explosion(), getSnappedKeyAtDomPos(), modifiersHash(), pieceCloseTo(), pieceHash() (+3 more)

### Community 2 - "app.js"
Cohesion: 0.10
Nodes (19): buildGameItem(), buildRefutationNarration(), cancelReview(), classifyAndPushMove(), classifyMove(), createAnalysisPool(), detectBrilliantSacrifice(), endReview() (+11 more)

### Community 3 - "renderCircle"
Cohesion: 0.16
Nodes (19): circleWidth(), createElement(), makeCustomBrush(), opacity(), orient(), pos2user(), render(), renderArrow() (+11 more)

### Community 4 - "callUserFunction"
Cohesion: 0.21
Nodes (23): baseMove(), baseNewPiece(), baseUserMove(), callUserFunction(), cancelMove(), canPredrop(), drop(), dropNewPiece() (+15 more)

### Community 5 - "handleReviewMove"
Cohesion: 0.20
Nodes (16): buildMaiaMoveVocab(), coachProgress(), deleteBranch(), deleteBranchesAt(), genBranchId(), goToBranch(), goToMove(), handleReviewMove() (+8 more)

### Community 6 - "doMaiaResponse"
Cohesion: 0.23
Nodes (12): cancelTTS(), checkDrawConditions(), doMaiaResponse(), drawGraph(), evalPosition(), isInsufficientMaterial(), onMaiaUserMove(), recordPosition() (+4 more)

### Community 7 - "updateBoard"
Cohesion: 0.21
Nodes (13): getLegalDests(), handleBranchMove(), hideSfPreview(), initBoard(), isPromotionMove(), onMove(), onMoveWithPromotion(), playChessSound() (+5 more)

### Community 8 - "render$1"
Cohesion: 0.20
Nodes (10): addSquare(), animate(), appendValue(), computePlan(), computeSquareClasses(), posZIndex(), removeNodes(), render$1() (+2 more)

### Community 9 - "updateExplorer"
Cohesion: 0.28
Nodes (9): doUpdateExplorer(), explorerFetchOpts(), fetchExplorerMoves(), fetchOpening(), getApiToken(), loadApiToken(), normalizeRatingToLichessBucket(), renderExplorer() (+1 more)

### Community 10 - "coachReset"
Cohesion: 0.35
Nodes (11): advanceToLandmark(), clearMistakeUI(), coachReset(), finishMaiaGame(), finishReview(), parseLines(), runGameReview(), setEngineStatus() (+3 more)

### Community 11 - "bindDocument"
Cohesion: 0.22
Nodes (10): addShape(), bindDocument(), cancel$1(), clear(), end$1(), move(), move$1(), onChange() (+2 more)

### Community 12 - "configure"
Cohesion: 0.24
Nodes (10): applyAnimation(), Chessground(), configure(), deepMerge(), defaults(), isPlainObject(), read(), setCheck() (+2 more)

### Community 13 - "stockfish.js"
Cohesion: 0.36
Nodes (8): analyzePositionalFactors(), generateReviewCommentary(), staticFallback(), d(), f(), l(), n(), o()

### Community 14 - "getMaiaMove"
Cohesion: 0.25
Nodes (9): buildMaiaInputTensor(), eloToTemp(), getMaiaMove(), getMaiaTopMoves(), mirrorFen(), mirrorSq(), mirrorUci(), sampleFromLogits() (+1 more)

### Community 15 - "dependencies"
Cohesion: 0.22
Nodes (8): chess.js, onnxruntime-web, dependencies, chess.js, onnxruntime-web, devDependencies, vite-plugin-static-copy, vite-plugin-static-copy

### Community 16 - "selectSquare"
Cohesion: 0.18
Nodes (14): cancel(), dragNewPiece(), isDraggable(), isMovable(), isPremovable(), pieceElementByKey(), premove(), processDrag() (+6 more)

### Community 19 - "speakText"
Cohesion: 0.38
Nodes (7): jumpToLandmark(), showLandmark(), _speakBrowser(), _speakEdgeTTS(), speakText(), speakTextWithCb(), updateLandmarkCounter()

## Knowledge Gaps
- **4 isolated node(s):** `Args`, `chess.js`, `onnxruntime-web`, `vite-plugin-static-copy`
  These have ≤1 connection - possible missing edges or undocumented components.
- **2 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `p()` connect `render$1` to `stockfish.js`, `updateBoard`?**
  _High betweenness centrality (0.426) - this node is a cross-community bridge._
- **Why does `showPromotionPicker()` connect `updateBoard` to `render$1`, `app.js`?**
  _High betweenness centrality (0.352) - this node is a cross-community bridge._
- **Why does `analyzePositionalFactors()` connect `stockfish.js` to `chess.js`, `app.js`?**
  _High betweenness centrality (0.244) - this node is a cross-community bridge._
- **What connects `Args`, `chess.js`, `onnxruntime-web` to the rest of the system?**
  _4 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `chess.js` be split into smaller, more focused modules?**
  _Cohesion score 0.12403100775193798 - nodes in this community are weakly interconnected._
- **Should `chessground.js` be split into smaller, more focused modules?**
  _Cohesion score 0.11067193675889328 - nodes in this community are weakly interconnected._
- **Should `app.js` be split into smaller, more focused modules?**
  _Cohesion score 0.09655172413793103 - nodes in this community are weakly interconnected._