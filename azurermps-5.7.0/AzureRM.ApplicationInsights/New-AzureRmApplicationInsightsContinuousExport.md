---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 1e4dd5f65789751f9a28deb9e10c37221f45b97b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625037"
---
# <span data-ttu-id="8fd90-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="8fd90-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="8fd90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fd90-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd90-103">為 application insights 資源建立新的 application insights 連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="8fd90-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd90-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fd90-104">SYNTAX</span></span>

### <span data-ttu-id="8fd90-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8fd90-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd90-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd90-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd90-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd90-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd90-108">說明</span><span class="sxs-lookup"><span data-stu-id="8fd90-108">DESCRIPTION</span></span>
<span data-ttu-id="8fd90-109">為 application insights 資源建立新的 application insights 連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="8fd90-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="8fd90-110">示例</span><span class="sxs-lookup"><span data-stu-id="8fd90-110">EXAMPLES</span></span>

### <span data-ttu-id="8fd90-111">範例1為 application insights 資源建立新的連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="8fd90-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="8fd90-112">建立新的 application insights 連續匯出設定，以將 "Request" 和 "Trace" 檔案類型匯出至儲存空間在資源群組 "testgroup" 中，在儲存帳戶 "teststorageaccount" 中包含 "testcontainer"。</span><span class="sxs-lookup"><span data-stu-id="8fd90-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="8fd90-113">SAS 權杖必須是有效的，且擁有對容器的寫入權限，否則連續匯出功能將無法運作。如果 SAS 權杖已過期，連續匯出功能將會停止運作。</span><span class="sxs-lookup"><span data-stu-id="8fd90-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="8fd90-114">參數</span><span class="sxs-lookup"><span data-stu-id="8fd90-114">PARAMETERS</span></span>

### <span data-ttu-id="8fd90-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8fd90-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8fd90-116">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="8fd90-116">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-117">-確認</span><span class="sxs-lookup"><span data-stu-id="8fd90-117">-Confirm</span></span>
<span data-ttu-id="8fd90-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8fd90-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd90-119">-DefaultProfile</span></span>
<span data-ttu-id="8fd90-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8fd90-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="8fd90-121">-DocumentType</span></span>
<span data-ttu-id="8fd90-122">需要匯出的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8fd90-122">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8fd90-123">-Name</span></span>
<span data-ttu-id="8fd90-124">元件名稱。</span><span class="sxs-lookup"><span data-stu-id="8fd90-124">Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd90-125">-ResourceGroupName</span></span>
<span data-ttu-id="8fd90-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8fd90-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fd90-127">-ResourceId</span></span>
<span data-ttu-id="8fd90-128">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fd90-128">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-129">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8fd90-129">-StorageAccountId</span></span>
<span data-ttu-id="8fd90-130">[目的地儲存空間帳戶識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8fd90-130">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-131">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="8fd90-131">-StorageLocation</span></span>
<span data-ttu-id="8fd90-132">[目的地儲存位置識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8fd90-132">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-133">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="8fd90-133">-StorageSASUri</span></span>
<span data-ttu-id="8fd90-134">目的地儲存體 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="8fd90-134">Destination Storage SAS Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd90-135">-WhatIf</span></span>
<span data-ttu-id="8fd90-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8fd90-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fd90-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8fd90-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd90-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd90-138">CommonParameters</span></span>
<span data-ttu-id="8fd90-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fd90-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd90-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fd90-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd90-141">輸入</span><span class="sxs-lookup"><span data-stu-id="8fd90-141">INPUTS</span></span>

### <span data-ttu-id="8fd90-142">System.object</span><span class="sxs-lookup"><span data-stu-id="8fd90-142">System.String</span></span>
<span data-ttu-id="8fd90-143">System.object []</span><span class="sxs-lookup"><span data-stu-id="8fd90-143">System.String[]</span></span>

## <span data-ttu-id="8fd90-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8fd90-144">OUTPUTS</span></span>

### <span data-ttu-id="8fd90-145">PSExportConfiguration 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="8fd90-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="8fd90-146">筆記</span><span class="sxs-lookup"><span data-stu-id="8fd90-146">NOTES</span></span>

## <span data-ttu-id="8fd90-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fd90-147">RELATED LINKS</span></span>

