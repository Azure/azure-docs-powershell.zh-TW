---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: f30d5da085658c979a52f166469e4e548afdaf7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788706"
---
# <span data-ttu-id="2a613-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="2a613-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="2a613-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a613-102">SYNOPSIS</span></span>
<span data-ttu-id="2a613-103">為 application insights 資源建立新的 application insights 連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="2a613-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="2a613-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a613-104">SYNTAX</span></span>

### <span data-ttu-id="2a613-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2a613-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a613-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a613-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a613-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a613-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a613-108">說明</span><span class="sxs-lookup"><span data-stu-id="2a613-108">DESCRIPTION</span></span>
<span data-ttu-id="2a613-109">為 application insights 資源建立新的 application insights 連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="2a613-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="2a613-110">示例</span><span class="sxs-lookup"><span data-stu-id="2a613-110">EXAMPLES</span></span>

### <span data-ttu-id="2a613-111">範例1為 application insights 資源建立新的連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="2a613-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="2a613-112">建立新的 application insights 連續匯出設定，以將 "Request" 和 "Trace" 檔案類型匯出至儲存空間在資源群組 "testgroup" 中，在儲存帳戶 "teststorageaccount" 中包含 "testcontainer"。</span><span class="sxs-lookup"><span data-stu-id="2a613-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="2a613-113">SAS 權杖必須是有效的，且擁有對容器的寫入權限，否則連續匯出功能將無法運作。如果 SAS 權杖已過期，連續匯出功能將會停止運作。</span><span class="sxs-lookup"><span data-stu-id="2a613-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="2a613-114">參數</span><span class="sxs-lookup"><span data-stu-id="2a613-114">PARAMETERS</span></span>

### <span data-ttu-id="2a613-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2a613-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="2a613-116">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="2a613-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="2a613-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a613-117">-DefaultProfile</span></span>
<span data-ttu-id="2a613-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a613-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a613-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="2a613-119">-DocumentType</span></span>
<span data-ttu-id="2a613-120">需要匯出的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="2a613-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a613-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a613-121">-Name</span></span>
<span data-ttu-id="2a613-122">元件名稱。</span><span class="sxs-lookup"><span data-stu-id="2a613-122">Component Name.</span></span>

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

### <span data-ttu-id="2a613-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a613-123">-ResourceGroupName</span></span>
<span data-ttu-id="2a613-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2a613-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="2a613-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a613-125">-ResourceId</span></span>
<span data-ttu-id="2a613-126">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a613-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="2a613-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2a613-127">-StorageAccountId</span></span>
<span data-ttu-id="2a613-128">[目的地儲存空間帳戶識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2a613-128">Destination Storage Account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a613-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="2a613-129">-StorageLocation</span></span>
<span data-ttu-id="2a613-130">[目的地儲存位置識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2a613-130">Destination Storage Location Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a613-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="2a613-131">-StorageSASUri</span></span>
<span data-ttu-id="2a613-132">目的地儲存體 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="2a613-132">Destination Storage SAS Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a613-133">-確認</span><span class="sxs-lookup"><span data-stu-id="2a613-133">-Confirm</span></span>
<span data-ttu-id="2a613-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a613-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a613-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a613-135">-WhatIf</span></span>
<span data-ttu-id="2a613-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a613-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a613-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a613-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a613-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a613-138">CommonParameters</span></span>
<span data-ttu-id="2a613-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a613-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a613-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a613-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a613-141">輸入</span><span class="sxs-lookup"><span data-stu-id="2a613-141">INPUTS</span></span>

### <span data-ttu-id="2a613-142">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="2a613-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="2a613-143">System.object</span><span class="sxs-lookup"><span data-stu-id="2a613-143">System.String</span></span>

## <span data-ttu-id="2a613-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2a613-144">OUTPUTS</span></span>

### <span data-ttu-id="2a613-145">PSExportConfiguration 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="2a613-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="2a613-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2a613-146">NOTES</span></span>

## <span data-ttu-id="2a613-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a613-147">RELATED LINKS</span></span>