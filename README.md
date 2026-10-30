# ClimateGuard – Climate Risk Awareness and Personalised Safety Platform

## 1. Project Overview

ClimateGuard is a climate-risk awareness platform designed to help people understand changing weather conditions and their possible effects on daily life. The platform provides personalised climate briefings for the next 72 hours by analysing important environmental factors such as temperature, rainfall, air quality, and ultraviolet (UV) exposure.

Weather information is often presented as raw numerical data, making it difficult for ordinary users to understand the actual risks and decide what precautions they should take. ClimateGuard addresses this problem by converting environmental data into understandable risk levels and practical recommendations.

Instead of simply displaying weather forecasts, the platform focuses on explaining what the predicted conditions could mean for people and their households. It combines weather information, environmental indicators, household-specific considerations, rule-based calculations, and AI-generated recommendations to provide a more meaningful understanding of potential climate risks.

The main objective is to make climate-related information accessible, understandable, and actionable so that users can make better-informed decisions in their daily lives.

## 2. Problem Statement

Climate change and unpredictable weather conditions are increasing the importance of understanding environmental risks. People regularly experience extreme temperatures, heavy rainfall, poor air quality, and high UV exposure. However, conventional weather applications primarily focus on displaying forecast information rather than explaining its possible consequences.

For example, a weather application may display a high temperature, but users may not understand the associated heat risk or the precautions they should consider. Similarly, an air-quality reading may be available, but users may not know how the pollution level could affect their outdoor activities.

The main problems addressed by ClimateGuard include:

1. Difficulty understanding raw weather and environmental data.
2. Limited awareness of the potential effects of heat, rainfall, air pollution, and UV exposure.
3. Lack of practical recommendations connected to specific environmental conditions.
4. Insufficient consideration of household-specific risks.
5. Difficulty combining information from multiple environmental data sources.
6. Limited availability of simple, understandable climate-risk briefings covering multiple environmental factors.

ClimateGuard aims to address these challenges by transforming environmental information into personalised and easy-to-understand risk briefings.

## 3. Proposed Solution

ClimateGuard provides an integrated platform that collects environmental information, analyses potential hazards, and generates recommendations based on the identified conditions.

The platform focuses on the upcoming 72 hours and considers four major environmental risk categories:

- Heat exposure
- Rainfall conditions
- Air quality
- Ultraviolet radiation

The collected information is processed using predefined calculations and risk-assessment logic. The platform then identifies the relevant hazard levels and uses AI to generate understandable recommendations.

The system is designed to ensure that numerical calculations and hazard classifications are handled through application logic rather than relying entirely on AI-generated responses.

AI is primarily used to communicate the identified risks in natural language and suggest practical actions. Generated recommendations are screened before being presented to users.

This approach combines structured environmental analysis with AI-assisted communication to make climate-risk information more useful.

## 4. Key Features

### 4.1. 72-Hour Climate Briefing

ClimateGuard provides climate and environmental risk information for the upcoming 72 hours.

Instead of focusing only on the current weather, the platform considers upcoming conditions to help users prepare in advance.

The briefing covers:

- Expected heat conditions.
- Predicted rainfall.
- Air-quality conditions.
- UV exposure levels.
- Relevant environmental hazards.
- Practical recommendations based on the identified conditions.

This allows users to understand potential changes in environmental conditions and take precautions before risks become significant.

### 4.2. Heat Risk Analysis

High temperatures can affect daily activities, outdoor work, and general comfort.

ClimateGuard analyses temperature-related conditions and identifies potential heat risks using a heat-index calculation based on the NWS Rothfusz approach.

The platform uses the calculated information to determine relevant heat conditions and communicate possible precautions.

The objective is to make temperature information more meaningful by explaining its potential impact rather than displaying temperature values alone.

### 4.3. Rainfall Risk Analysis

Rainfall conditions can influence transportation, outdoor activities, and everyday planning.

ClimateGuard analyses rainfall information to identify relevant rainfall categories and communicate potential concerns.

The platform uses rainfall classifications to explain expected conditions and provide general recommendations.

These classifications are intended for climate-risk awareness. They should not be interpreted as official flood predictions or warnings.

### 4.4. Air Quality Monitoring

Air pollution is an important environmental factor that can affect outdoor activities and general well-being.

ClimateGuard incorporates air-quality information from available environmental data sources and uses EPA AQI categories to communicate air-quality conditions.

The system helps users understand whether the available air-quality information indicates relatively good or concerning conditions.

Based on the identified category, the platform can provide relevant general precautions.

### 4.5. UV Exposure Analysis

Ultraviolet radiation is another important environmental risk factor.

ClimateGuard analyses UV information and classifies exposure levels using WHO UV categories.

The platform communicates the identified UV conditions and provides relevant precautions to help users understand potential exposure risks.

This feature makes UV information part of the overall climate briefing instead of treating it as an unrelated weather measurement.

### 4.6. Household-Specific Risk Considerations

ClimateGuard is designed to consider household-specific risk information when presenting climate-related recommendations.

The objective is to make the information more relevant to the people using the platform rather than providing identical generic recommendations to everyone.

Household-related information can influence how environmental conditions are communicated and which precautions are highlighted.

This feature supports the platform's goal of providing more contextualised climate-risk awareness.

### 4.7. AI-Powered Recommendations

ClimateGuard uses the Mistral `open-mistral-nemo` model to generate natural-language recommendations based on the environmental conditions identified by the application.

The AI component focuses on communicating risks and suggesting practical actions.

Importantly, AI does not independently determine the application's numerical measurements or hazard classifications. These are calculated using the platform's predefined logic.

This separation helps maintain consistency between the environmental analysis and the recommendations presented to users.

### 4.8. Recommendation Screening and Safety Checks

AI-generated recommendations may sometimes contain inaccurate, unsupported, or unsuitable information. ClimateGuard includes screening mechanisms to evaluate generated content before displaying it.

The screening process checks for issues such as:

- Unsupported numerical information.
- Unjustified instructions to remain indoors.
- Recommendations that do not appropriately address the identified hazards.
- Empty or excessively long responses.
- Inappropriate or disallowed vocabulary.
- Recommendations that fail to meet the platform's expected safety conditions.

The system also uses fixed safety notices when a serious hazard is identified but an acceptable AI-generated recommendation is not retained.

This provides an additional layer of protection and helps prevent the application from depending entirely on unrestricted AI-generated content.

### 4.9. Multilingual Support

ClimateGuard supports two languages:

- English
- Bahasa Indonesia

This feature helps make climate-risk information accessible to users who prefer different languages.

The multilingual approach is intended to improve the accessibility and usability of environmental information.

## 5. Technology Stack and Data Sources

ClimateGuard combines environmental data services, AI capabilities, and application-level risk calculations.

### Environmental Data Sources

Open-Meteo

Open-Meteo provides weather and forecast information used by the platform to analyse upcoming environmental conditions.

ECMWF IFS and AIFS

The platform incorporates information associated with ECMWF's Integrated Forecasting System (IFS) and Artificial Intelligence Forecasting System (AIFS).

These forecasting sources contribute to the environmental information used in the climate briefing.

CAMS

The Copernicus Atmosphere Monitoring Service (CAMS) provides atmospheric and air-quality-related information used by the platform.

ERA5-Based Archive

ERA5-based historical environmental information supports the platform's use of climate-related reference data.

NASA POWER

NASA POWER is included as a fallback data source when the primary data sources are unavailable or unsuitable.

### AI Technology

ClimateGuard uses the Mistral `open-mistral-nemo` model for generating natural-language recommendations.

The model receives relevant information from the application's environmental analysis and produces recommendations intended to help users understand potential risks.

The generated output is subsequently screened by the application.

### Risk Calculation and Classification

The platform uses established approaches and reference categories for interpreting environmental conditions.

These include:

- NWS Rothfusz approach for heat-index calculations.
- EPA AQI categories for air-quality interpretation.
- WHO UV categories for ultraviolet exposure.
- Project-defined rainfall classifications.

This combination allows the application to process different environmental indicators through a structured approach.

## 6. System Workflow

The overall ClimateGuard workflow can be understood through the following stages.

Stage 1: Environmental Data Collection

The platform retrieves relevant weather and environmental information from its integrated data sources.

The collected information includes temperature, rainfall, air quality, and UV-related measurements.

Stage 2: Data Processing

The collected information is processed and organised so that it can be used for environmental analysis.

This stage prepares the available data for the platform's risk calculations.

Stage 3: Hazard Calculation

The application uses predefined logic and relevant classification approaches to calculate environmental conditions and identify potential hazards.

The numerical calculations and hazard levels are determined by the application rather than being invented by the AI model.

Stage 4: Household Risk Consideration

The platform considers available household-specific information to make the resulting risk briefing more relevant.

Stage 5: AI Recommendation Generation

The processed environmental information and identified hazards are used to generate natural-language recommendations through the Mistral model.

Stage 6: Recommendation Screening

The generated recommendations are evaluated using predefined screening conditions.

Responses that fail the platform's checks are not retained as acceptable recommendations.

Stage 7: Safety Notice Generation

When a serious hazard exists but no acceptable AI recommendation is retained, the system displays a fixed safety notice.

Stage 8: Final Climate Briefing

The platform presents the environmental conditions, identified risks, and available recommendations in an understandable format.

The final result is intended to help users understand upcoming climate conditions and prepare accordingly.

## 7. Reference Frameworks and Standards

ClimateGuard draws conceptual and technical inspiration from established climate, disaster-risk, and environmental reference materials.

WMO-No. 1150

The platform draws conceptual inspiration from the World Meteorological Organization's guidance related to climate services and climate information.

UN Sendai Framework

The United Nations Sendai Framework for Disaster Risk Reduction provides conceptual inspiration for the platform's focus on risk awareness and preparedness.

WMO-No. 1203

The platform refers to the 1991–2020 climatological standard normal baseline associated with WMO-No. 1203.

NWS Heat Index

The NWS Rothfusz approach is used as the reference for heat-index calculations.

EPA Air Quality Index

EPA AQI categories provide a reference for communicating air-quality conditions.

WHO UV Categories

WHO UV categories are used as a reference for classifying ultraviolet exposure.

These references help establish a structured foundation for environmental interpretation. Their inclusion does not mean that ClimateGuard is officially certified or endorsed by the organisations responsible for them.

## 8. Evaluation and Testing

ClimateGuard includes an evaluation of its AI-generated recommendations and safety-screening process.

The reported evaluation covers runs conducted between 19 and 22 October 2026.

The evaluation considers four categories:

- English tuned data.
- English held-out data.
- Bahasa Indonesia tuned data.
- Bahasa Indonesia held-out data.

### Reported Evaluation Results

| Evaluation category | AI actions kept | Serious hazards covered by kept AI actions |
| ------------------- | --------------- | ------------------------------------------ |
| English tuned       | 76.7%           | 76.3%                                      |
| English held-out    | 85.2%           | 84.2%                                      |
| Indonesian tuned    | 90.7%           | 89.8%                                      |
| Indonesian held-out | 81.5%           | 84.2%                                      |

The evaluation also reports that serious hazards are covered after fixed safety notices are included. The reported 100% coverage after notices is achieved by the system's construction.

The evaluation reports zero AI-generated numerical values displayed, as numerical information is handled through the application's calculation logic.

These results provide an indication of how the recommendation-generation and screening mechanisms performed during the reported tests.

However, the evaluation has limitations. The sample sizes are small, and the acceptance of a recommendation by the screening system does not necessarily prove that the recommendation is accurate, useful, or clinically validated.

Therefore, the reported percentages should be interpreted as project evaluation results rather than proof of real-world safety or effectiveness.

## 9. Advantages of ClimateGuard

1\. Multi-factor environmental analysis: Combines heat, rainfall, air quality, and UV information in one platform.

2\. Future-oriented awareness: Provides briefings for the next 72 hours, helping users prepare for upcoming conditions.

3\. Personalised risk considerations: Incorporates household-specific information to make risk communication more relevant.

4\. AI-assisted recommendations: Converts technical environmental information into understandable natural-language guidance.

5\. Structured calculations: Uses application-level logic for numerical calculations and hazard classifications.

6\. Recommendation screening: Evaluates AI-generated content before presenting it to users.

7\. Fallback safety notices: Provides fixed notices when serious hazards do not have an acceptable AI-generated recommendation.

8\. Multilingual accessibility: Supports English and Bahasa Indonesia.

9\. Multiple data sources: Incorporates information from different weather and environmental services.

10\. Risk-awareness focus: Emphasises understanding and preparedness rather than simply displaying weather measurements.

## 10. Limitations

ClimateGuard is designed as a climate-risk awareness and decision-support platform. It has certain limitations that should be considered.

- AI-generated recommendations are screened but have not been clinically validated.
- Environmental data availability depends on the integrated external services.
- Free data services may have usage restrictions, rate limits, or availability limitations.
- Household risk thresholds and some classifications are specific to the project.
- Rainfall classifications should not be interpreted as official flood forecasts.
- The platform does not replace official weather alerts, emergency instructions, or professional medical advice.
- The reported evaluation uses relatively small samples and does not establish real-world effectiveness.
- Screening acceptance does not guarantee that every recommendation is appropriate for every individual or situation.

Users should follow official warnings and instructions issued by relevant authorities during serious weather and environmental events.

## 11. Future Scope

ClimateGuard can be extended in several ways to improve its functionality and practical usefulness.

Improved Environmental Data Integration

Additional environmental data sources and more comprehensive forecasting information could improve the coverage and reliability of the platform.

Advanced Personalisation

The platform could incorporate more household context and user-defined preferences to make climate-risk recommendations more relevant.

Expanded Language Support

Additional regional and international languages could improve accessibility for a wider range of users.

Enhanced Risk Analysis

Future versions could improve the interpretation of combined environmental hazards and provide more detailed explanations of how different conditions interact.

Improved Recommendation Evaluation

Larger datasets, additional test scenarios, and expert reviews could help assess the quality and reliability of generated recommendations.

Improved Safety Mechanisms

The screening process could be expanded and evaluated against a broader range of potentially unsafe or misleading recommendations.

Additional Environmental Indicators

Further environmental factors could be incorporated to provide a more comprehensive climate-awareness experience.

These are possible future improvements and should not be understood as features already implemented in the current version.

## 12. Conclusion

ClimateGuard aims to make climate and environmental information more understandable and useful for everyday decision-making. By combining weather forecasts, air-quality information, UV exposure data, household-specific considerations, and AI-assisted recommendations, the platform provides a structured approach to climate-risk awareness.

Its primary strength is the integration of multiple environmental indicators into a single 72-hour briefing. Rather than presenting only raw numerical information, ClimateGuard attempts to explain the potential risks and provide practical recommendations.

The separation of application-level calculations from AI-generated communication is an important part of its design. Environmental measurements and hazard classifications are determined through predefined logic, while AI is used to communicate the results in natural language. Recommendation screening and fixed safety notices provide additional safeguards.

Overall, ClimateGuard demonstrates how environmental data, structured risk analysis, and artificial intelligence can be combined to improve climate awareness and encourage better preparation for changing environmental conditions.

The platform is intended to support informed decision-making and climate-risk awareness, not to replace official warnings, emergency services, or professional advice.

## 13. Project Attribution

ClimateGuard is based on the Prakira project, originally available at:

[https://github.com/rofiperlungoding/prakira](https://github.com/rofiperlungoding/prakira?utm_source=chatgpt.com)

The project has been adapted and presented under the name ClimateGuard. Appropriate attribution and compliance with the original project's licence terms should be maintained.
