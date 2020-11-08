---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965594"
---
# <span data-ttu-id="a180f-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="a180f-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="a180f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a180f-102">SYNOPSIS</span></span>
<span data-ttu-id="a180f-103">取得 application insights 資源的 application insights 連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="a180f-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a180f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a180f-104">SYNTAX</span></span>

### <span data-ttu-id="a180f-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a180f-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a180f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a180f-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a180f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a180f-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a180f-108">說明</span><span class="sxs-lookup"><span data-stu-id="a180f-108">DESCRIPTION</span></span>
<span data-ttu-id="a180f-109">取得 application insights 資源的 application insights 連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="a180f-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a180f-110">示例</span><span class="sxs-lookup"><span data-stu-id="a180f-110">EXAMPLES</span></span>

### <span data-ttu-id="a180f-111">範例1取得 application insights 資源的連續匯出</span><span class="sxs-lookup"><span data-stu-id="a180f-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="a180f-112">在資源群組 "testgroup" 中取得名為「test」之資源的 application insights 連續匯出設定</span><span class="sxs-lookup"><span data-stu-id="a180f-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="a180f-113">範例2取得 application insights 資源的連續匯出</span><span class="sxs-lookup"><span data-stu-id="a180f-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="a180f-114">針對資源群組 "testgroup" 中名為 "test" 的資源，取得含匯出 id "ZJrfffySPdtG3ESn3iRxVIEFuNY =" 的 application insights 連續匯出設定</span><span class="sxs-lookup"><span data-stu-id="a180f-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a180f-115">參數</span><span class="sxs-lookup"><span data-stu-id="a180f-115">PARAMETERS</span></span>

### <span data-ttu-id="a180f-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a180f-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a180f-117">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="a180f-117">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a180f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a180f-118">-DefaultProfile</span></span>
<span data-ttu-id="a180f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a180f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a180f-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="a180f-120">-ExportId</span></span>
<span data-ttu-id="a180f-121">Application Insights 連續匯出 Id。</span><span class="sxs-lookup"><span data-stu-id="a180f-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a180f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a180f-122">-Name</span></span>
<span data-ttu-id="a180f-123">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="a180f-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a180f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a180f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a180f-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a180f-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a180f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a180f-126">-ResourceId</span></span>
<span data-ttu-id="a180f-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a180f-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a180f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a180f-128">CommonParameters</span></span>
<span data-ttu-id="a180f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a180f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a180f-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a180f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a180f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a180f-131">INPUTS</span></span>

### <span data-ttu-id="a180f-132">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="a180f-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a180f-133">System.object</span><span class="sxs-lookup"><span data-stu-id="a180f-133">System.String</span></span>

## <span data-ttu-id="a180f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a180f-134">OUTPUTS</span></span>

### <span data-ttu-id="a180f-135">PSExportConfiguration 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="a180f-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="a180f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a180f-136">NOTES</span></span>

## <span data-ttu-id="a180f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a180f-137">RELATED LINKS</span></span>