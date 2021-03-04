---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 144200f95ca7cff8b4fa541666912d62ba6bd0b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905626"
---
# <span data-ttu-id="28998-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="28998-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="28998-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28998-102">SYNOPSIS</span></span>
<span data-ttu-id="28998-103">更新應用程式深入資訊資源中的連續匯出組</span><span class="sxs-lookup"><span data-stu-id="28998-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="28998-104">語法</span><span class="sxs-lookup"><span data-stu-id="28998-104">SYNTAX</span></span>

### <span data-ttu-id="28998-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28998-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28998-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28998-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28998-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28998-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28998-108">描述</span><span class="sxs-lookup"><span data-stu-id="28998-108">DESCRIPTION</span></span>
<span data-ttu-id="28998-109">更新應用程式深入資訊資源中的連續匯出組</span><span class="sxs-lookup"><span data-stu-id="28998-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="28998-110">例子</span><span class="sxs-lookup"><span data-stu-id="28998-110">EXAMPLES</span></span>

### <span data-ttu-id="28998-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="28998-111">Example 1</span></span>
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

<span data-ttu-id="28998-112">更新資源群組 "testgroup" 中資源 "test" 的連續匯出組"jlTFEiBg1rkDXOCIeJQ2mB2TxZg="，將「要求」和「追蹤」檔匯出至「testtorageaccount」中的儲存容器「testcontainer」。SAS 權杖必須有效且具有容器的寫入權限，否則無法使用連續匯出功能。</span><span class="sxs-lookup"><span data-stu-id="28998-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="28998-113">如果 SAS 權杖已過期，連續匯出功能將會停止工作。</span><span class="sxs-lookup"><span data-stu-id="28998-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="28998-114">參數</span><span class="sxs-lookup"><span data-stu-id="28998-114">PARAMETERS</span></span>

### <span data-ttu-id="28998-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="28998-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="28998-116">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="28998-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="28998-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28998-117">-DefaultProfile</span></span>
<span data-ttu-id="28998-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28998-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28998-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="28998-119">-DisableConfiguration</span></span>
<span data-ttu-id="28998-120">停用連續匯出或不停用。</span><span class="sxs-lookup"><span data-stu-id="28998-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="28998-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="28998-121">-DocumentType</span></span>
<span data-ttu-id="28998-122">需要匯出的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="28998-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="28998-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="28998-123">-ExportId</span></span>
<span data-ttu-id="28998-124">應用程式深入資訊連續匯出識別碼。</span><span class="sxs-lookup"><span data-stu-id="28998-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="28998-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="28998-125">-Name</span></span>
<span data-ttu-id="28998-126">應用程式深入資訊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="28998-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="28998-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28998-127">-ResourceGroupName</span></span>
<span data-ttu-id="28998-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="28998-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="28998-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28998-129">-ResourceId</span></span>
<span data-ttu-id="28998-130">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="28998-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="28998-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="28998-131">-StorageAccountId</span></span>
<span data-ttu-id="28998-132">目的地儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="28998-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="28998-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="28998-133">-StorageLocation</span></span>
<span data-ttu-id="28998-134">目的地儲存位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="28998-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="28998-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="28998-135">-StorageSASUri</span></span>
<span data-ttu-id="28998-136">目的地儲存空間 SAS uri。</span><span class="sxs-lookup"><span data-stu-id="28998-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="28998-137">-確認</span><span class="sxs-lookup"><span data-stu-id="28998-137">-Confirm</span></span>
<span data-ttu-id="28998-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28998-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28998-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28998-139">-WhatIf</span></span>
<span data-ttu-id="28998-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28998-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28998-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28998-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28998-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28998-142">CommonParameters</span></span>
<span data-ttu-id="28998-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28998-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28998-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="28998-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28998-145">輸入</span><span class="sxs-lookup"><span data-stu-id="28998-145">INPUTS</span></span>

### <span data-ttu-id="28998-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="28998-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="28998-147">System.String</span><span class="sxs-lookup"><span data-stu-id="28998-147">System.String</span></span>

## <span data-ttu-id="28998-148">輸出</span><span class="sxs-lookup"><span data-stu-id="28998-148">OUTPUTS</span></span>

### <span data-ttu-id="28998-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="28998-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="28998-150">筆記</span><span class="sxs-lookup"><span data-stu-id="28998-150">NOTES</span></span>

## <span data-ttu-id="28998-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="28998-151">RELATED LINKS</span></span>
