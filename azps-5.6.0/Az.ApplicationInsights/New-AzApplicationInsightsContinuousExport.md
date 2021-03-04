---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 4c00bfec7ab026478c4b05b55ce27b812af37486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903366"
---
# <span data-ttu-id="55bae-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="55bae-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="55bae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55bae-102">SYNOPSIS</span></span>
<span data-ttu-id="55bae-103">為應用程式深入資訊資源建立新的應用程式深入資訊連續匯出組</span><span class="sxs-lookup"><span data-stu-id="55bae-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="55bae-104">語法</span><span class="sxs-lookup"><span data-stu-id="55bae-104">SYNTAX</span></span>

### <span data-ttu-id="55bae-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="55bae-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55bae-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55bae-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55bae-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55bae-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55bae-108">描述</span><span class="sxs-lookup"><span data-stu-id="55bae-108">DESCRIPTION</span></span>
<span data-ttu-id="55bae-109">為應用程式深入資訊資源建立新的應用程式深入資訊連續匯出組</span><span class="sxs-lookup"><span data-stu-id="55bae-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="55bae-110">例子</span><span class="sxs-lookup"><span data-stu-id="55bae-110">EXAMPLES</span></span>

### <span data-ttu-id="55bae-111">範例 1 為應用程式深入資訊資源建立新的連續匯出組</span><span class="sxs-lookup"><span data-stu-id="55bae-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
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

<span data-ttu-id="55bae-112">建立新的應用程式深入資訊連續匯出組，以將「要求」和「追蹤」檔案類型匯出至儲存空間群組「testtorageaccount」中的「testcontainer」。</span><span class="sxs-lookup"><span data-stu-id="55bae-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="55bae-113">SAS 權杖必須有效且具有容器的寫入權限，否則無法使用連續匯出功能。如果 SAS 權杖已過期，連續匯出功能將會停止工作。</span><span class="sxs-lookup"><span data-stu-id="55bae-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="55bae-114">參數</span><span class="sxs-lookup"><span data-stu-id="55bae-114">PARAMETERS</span></span>

### <span data-ttu-id="55bae-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="55bae-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="55bae-116">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="55bae-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="55bae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55bae-117">-DefaultProfile</span></span>
<span data-ttu-id="55bae-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55bae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55bae-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="55bae-119">-DocumentType</span></span>
<span data-ttu-id="55bae-120">需要匯出的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="55bae-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="55bae-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="55bae-121">-Name</span></span>
<span data-ttu-id="55bae-122">元件名稱。</span><span class="sxs-lookup"><span data-stu-id="55bae-122">Component Name.</span></span>

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

### <span data-ttu-id="55bae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55bae-123">-ResourceGroupName</span></span>
<span data-ttu-id="55bae-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="55bae-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="55bae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55bae-125">-ResourceId</span></span>
<span data-ttu-id="55bae-126">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="55bae-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="55bae-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="55bae-127">-StorageAccountId</span></span>
<span data-ttu-id="55bae-128">目的地儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="55bae-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="55bae-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="55bae-129">-StorageLocation</span></span>
<span data-ttu-id="55bae-130">目的地儲存位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="55bae-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="55bae-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="55bae-131">-StorageSASUri</span></span>
<span data-ttu-id="55bae-132">目的地儲存空間 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="55bae-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="55bae-133">-確認</span><span class="sxs-lookup"><span data-stu-id="55bae-133">-Confirm</span></span>
<span data-ttu-id="55bae-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="55bae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55bae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55bae-135">-WhatIf</span></span>
<span data-ttu-id="55bae-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55bae-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55bae-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55bae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55bae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55bae-138">CommonParameters</span></span>
<span data-ttu-id="55bae-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55bae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55bae-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="55bae-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55bae-141">輸入</span><span class="sxs-lookup"><span data-stu-id="55bae-141">INPUTS</span></span>

### <span data-ttu-id="55bae-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="55bae-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="55bae-143">System.String</span><span class="sxs-lookup"><span data-stu-id="55bae-143">System.String</span></span>

## <span data-ttu-id="55bae-144">輸出</span><span class="sxs-lookup"><span data-stu-id="55bae-144">OUTPUTS</span></span>

### <span data-ttu-id="55bae-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="55bae-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="55bae-146">筆記</span><span class="sxs-lookup"><span data-stu-id="55bae-146">NOTES</span></span>

## <span data-ttu-id="55bae-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="55bae-147">RELATED LINKS</span></span>
