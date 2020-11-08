---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971121"
---
# <span data-ttu-id="10b48-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="10b48-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="10b48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10b48-102">SYNOPSIS</span></span>
<span data-ttu-id="10b48-103">建立共用訂閱的資料集對應。</span><span class="sxs-lookup"><span data-stu-id="10b48-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="10b48-104">句法</span><span class="sxs-lookup"><span data-stu-id="10b48-104">SYNTAX</span></span>

### <span data-ttu-id="10b48-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="10b48-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10b48-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="10b48-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b48-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b48-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10b48-108">說明</span><span class="sxs-lookup"><span data-stu-id="10b48-108">DESCRIPTION</span></span>
<span data-ttu-id="10b48-109">**AzDataShareDataSetMapping** Cmdlet 會在 [共用訂閱] 中的 [源資料集] 和 [接收] 儲存空間帳戶之間建立資料集對應。</span><span class="sxs-lookup"><span data-stu-id="10b48-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="10b48-110">示例</span><span class="sxs-lookup"><span data-stu-id="10b48-110">EXAMPLES</span></span>

### <span data-ttu-id="10b48-111">範例1</span><span class="sxs-lookup"><span data-stu-id="10b48-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="10b48-112">這個命令會針對 [資料共用帳戶 WikiAdsAccount] 中的 [共用訂閱 AdsShareSubscription] 建立資料集對應 AdsDataSetMapping 至儲存帳戶 AdsStorage。</span><span class="sxs-lookup"><span data-stu-id="10b48-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="10b48-113">參數</span><span class="sxs-lookup"><span data-stu-id="10b48-113">PARAMETERS</span></span>

### <span data-ttu-id="10b48-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="10b48-114">-AccountName</span></span>
<span data-ttu-id="10b48-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="10b48-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-116">-容器</span><span class="sxs-lookup"><span data-stu-id="10b48-116">-Container</span></span>
<span data-ttu-id="10b48-117">Azure 儲存空間帳戶容器名稱</span><span class="sxs-lookup"><span data-stu-id="10b48-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="10b48-118">-DataSetId</span></span>
<span data-ttu-id="10b48-119">消費者資料集識別碼</span><span class="sxs-lookup"><span data-stu-id="10b48-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b48-120">-DefaultProfile</span></span>
<span data-ttu-id="10b48-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10b48-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10b48-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="10b48-122">-FilePath</span></span>
<span data-ttu-id="10b48-123">Azure 儲存空間路徑</span><span class="sxs-lookup"><span data-stu-id="10b48-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="10b48-124">-FileSystem</span></span>
<span data-ttu-id="10b48-125">Azure ADLS gen2 file system name</span><span class="sxs-lookup"><span data-stu-id="10b48-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="10b48-126">-FolderPath</span></span>
<span data-ttu-id="10b48-127">Azure 儲存空間資料夾路徑</span><span class="sxs-lookup"><span data-stu-id="10b48-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="10b48-128">-Name</span></span>
<span data-ttu-id="10b48-129">Azure 資料集對應名稱</span><span class="sxs-lookup"><span data-stu-id="10b48-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b48-130">-ResourceGroupName</span></span>
<span data-ttu-id="10b48-131">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="10b48-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="10b48-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="10b48-133">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="10b48-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="10b48-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="10b48-135">Azure 儲存空間帳戶 ResourceId</span><span class="sxs-lookup"><span data-stu-id="10b48-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b48-136">-確認</span><span class="sxs-lookup"><span data-stu-id="10b48-136">-Confirm</span></span>
<span data-ttu-id="10b48-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10b48-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10b48-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10b48-138">-WhatIf</span></span>
<span data-ttu-id="10b48-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10b48-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10b48-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10b48-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10b48-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b48-141">CommonParameters</span></span>
<span data-ttu-id="10b48-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10b48-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b48-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="10b48-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b48-144">輸入</span><span class="sxs-lookup"><span data-stu-id="10b48-144">INPUTS</span></span>

### <span data-ttu-id="10b48-145">System.object</span><span class="sxs-lookup"><span data-stu-id="10b48-145">System.String</span></span>

## <span data-ttu-id="10b48-146">輸出</span><span class="sxs-lookup"><span data-stu-id="10b48-146">OUTPUTS</span></span>

### <span data-ttu-id="10b48-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="10b48-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="10b48-148">筆記</span><span class="sxs-lookup"><span data-stu-id="10b48-148">NOTES</span></span>

## <span data-ttu-id="10b48-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="10b48-149">RELATED LINKS</span></span>
