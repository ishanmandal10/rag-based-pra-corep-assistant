# LLM-Assisted PRA COREP Reporting Assistant (Prototype)

This repository contains a constrained prototype of an LLM-assisted regulatory reporting assistant for the PRA COREP Own Funds template.

## Overview

The system demonstrates end-to-end behaviour:

- Semantic retrieval of PRA/CRR rulebook provisions using FAISS
- Context-grounded structured extraction using an instruction-tuned LLM (Flan-T5)
- Deterministic validation of capital components
- Mapping to a simplified COREP Own Funds reporting template
- Audit traceability linking populated fields to regulatory rule references

## Architecture

User Query  
→ Semantic Retrieval (FAISS + SentenceTransformers)  
→ Context Injection into LLM (Flan-T5)  
→ Structured JSON Extraction  
→ Deterministic Validation (Python)  
→ Template Mapping  
→ Audit Log Generation  

## Scope

For demonstration purposes, this prototype focuses on a constrained subset of Own Funds provisions (CRR Articles 26, 51, 62, 72).

The architecture separates LLM reasoning from deterministic validation to reduce hallucination risk and improve regulatory robustness.
