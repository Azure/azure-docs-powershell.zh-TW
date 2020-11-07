---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958749"
---
# <span data-ttu-id="8934c-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="8934c-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="8934c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8934c-102">SYNOPSIS</span></span>
<span data-ttu-id="8934c-103">更新 application insights 資源中的連續匯出設定</span><span class="sxs-lookup"><span data-stu-id="8934c-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="8934c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8934c-104">SYNTAX</span></span>

### <span data-ttu-id="8934c-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8934c-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8934c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8934c-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8934c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8934c-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8934c-108">說明</span><span class="sxs-lookup"><span data-stu-id="8934c-108">DESCRIPTION</span></span>
<span data-ttu-id="8934c-109">更新 application insights 資源中的連續匯出設定</span><span class="sxs-lookup"><span data-stu-id="8934c-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="8934c-110">示例</span><span class="sxs-lookup"><span data-stu-id="8934c-110">EXAMPLES</span></span>

### <span data-ttu-id="8934c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8934c-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="8934c-112">更新資源群組 "testgroup" 中資源 "test" 的連續匯出設定 "jlTFEiBg1rkDXOCIeJQ2mB2TxZg ="，即可在 "teststorageaccount" 中將 "Request" 和 "Trace" 檔匯出至儲存容器 "testcontainer"。SAS 權杖必須是有效的，且擁有對容器的寫入權限，否則連續匯出功能將無法運作。</span><span class="sxs-lookup"><span data-stu-id="8934c-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="8934c-113">如果 SAS 權杖已過期，連續匯出功能將會停止運作。</span><span class="sxs-lookup"><span data-stu-id="8934c-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="8934c-114">參數</span><span class="sxs-lookup"><span data-stu-id="8934c-114">PARAMETERS</span></span>

### <span data-ttu-id="8934c-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8934c-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8934c-116">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="8934c-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8934c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8934c-117">-DefaultProfile</span></span>
<span data-ttu-id="8934c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8934c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8934c-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="8934c-119">-DisableConfiguration</span></span>
<span data-ttu-id="8934c-120">停用連續匯出。</span><span class="sxs-lookup"><span data-stu-id="8934c-120">Disable continuous export or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8934c-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="8934c-121">-DocumentType</span></span>
<span data-ttu-id="8934c-122">需要匯出的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8934c-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="8934c-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="8934c-123">-ExportId</span></span>
<span data-ttu-id="8934c-124">Application Insights 連續匯出 Id。</span><span class="sxs-lookup"><span data-stu-id="8934c-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="8934c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="8934c-125">-Name</span></span>
<span data-ttu-id="8934c-126">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="8934c-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8934c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8934c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8934c-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8934c-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="8934c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8934c-129">-ResourceId</span></span>
<span data-ttu-id="8934c-130">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8934c-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8934c-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8934c-131">-StorageAccountId</span></span>
<span data-ttu-id="8934c-132">[目的地儲存空間帳戶識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8934c-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="8934c-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="8934c-133">-StorageLocation</span></span>
<span data-ttu-id="8934c-134">[目的地儲存位置識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8934c-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="8934c-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="8934c-135">-StorageSASUri</span></span>
<span data-ttu-id="8934c-136">目的地儲存體 SAS uri。</span><span class="sxs-lookup"><span data-stu-id="8934c-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="8934c-137">-確認</span><span class="sxs-lookup"><span data-stu-id="8934c-137">-Confirm</span></span>
<span data-ttu-id="8934c-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8934c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8934c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8934c-139">-WhatIf</span></span>
<span data-ttu-id="8934c-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8934c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8934c-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8934c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8934c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8934c-142">CommonParameters</span></span>
<span data-ttu-id="8934c-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8934c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8934c-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8934c-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8934c-145">輸入</span><span class="sxs-lookup"><span data-stu-id="8934c-145">INPUTS</span></span>

### <span data-ttu-id="8934c-146">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="8934c-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8934c-147">System.object</span><span class="sxs-lookup"><span data-stu-id="8934c-147">System.String</span></span>

## <span data-ttu-id="8934c-148">輸出</span><span class="sxs-lookup"><span data-stu-id="8934c-148">OUTPUTS</span></span>

### <span data-ttu-id="8934c-149">PSExportConfiguration 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="8934c-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="8934c-150">筆記</span><span class="sxs-lookup"><span data-stu-id="8934c-150">NOTES</span></span>

## <span data-ttu-id="8934c-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="8934c-151">RELATED LINKS</span></span>
