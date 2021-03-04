---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 56c573f6806acf2d9c45f583bbbb880aa6fc5638
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913549"
---
# <span data-ttu-id="9ce1a-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="9ce1a-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="9ce1a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9ce1a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce1a-103">建立共用訂閱的資料集地圖。</span><span class="sxs-lookup"><span data-stu-id="9ce1a-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="9ce1a-104">語法</span><span class="sxs-lookup"><span data-stu-id="9ce1a-104">SYNTAX</span></span>

### <span data-ttu-id="9ce1a-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9ce1a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ce1a-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="9ce1a-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ce1a-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ce1a-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ce1a-108">描述</span><span class="sxs-lookup"><span data-stu-id="9ce1a-108">DESCRIPTION</span></span>
<span data-ttu-id="9ce1a-109">**New-AzDataShareDataSetMadlet** 會建立源資料集與共享訂閱中儲存空間帳戶之間的資料集地圖。</span><span class="sxs-lookup"><span data-stu-id="9ce1a-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="9ce1a-110">例子</span><span class="sxs-lookup"><span data-stu-id="9ce1a-110">EXAMPLES</span></span>

### <span data-ttu-id="9ce1a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9ce1a-111">Example 1</span></span>
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

<span data-ttu-id="9ce1a-112">此命令會建立一組資料集，將 AdsDataSetMapping 與儲存帳戶 AdsStorage 進行資料共用帳戶 WikiAdsAccount 中的共用訂閱 AdsShareSubscription。</span><span class="sxs-lookup"><span data-stu-id="9ce1a-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="9ce1a-113">參數</span><span class="sxs-lookup"><span data-stu-id="9ce1a-113">PARAMETERS</span></span>

### <span data-ttu-id="9ce1a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ce1a-114">-AccountName</span></span>
<span data-ttu-id="9ce1a-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="9ce1a-115">Azure data share account name</span></span>

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

### <span data-ttu-id="9ce1a-116">-Container</span><span class="sxs-lookup"><span data-stu-id="9ce1a-116">-Container</span></span>
<span data-ttu-id="9ce1a-117">Azure 儲存帳戶容器名稱</span><span class="sxs-lookup"><span data-stu-id="9ce1a-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="9ce1a-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="9ce1a-118">-DataSetId</span></span>
<span data-ttu-id="9ce1a-119">消費者資料集識別碼</span><span class="sxs-lookup"><span data-stu-id="9ce1a-119">Consumer data set id</span></span>

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

### <span data-ttu-id="9ce1a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce1a-120">-DefaultProfile</span></span>
<span data-ttu-id="9ce1a-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ce1a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ce1a-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="9ce1a-122">-FilePath</span></span>
<span data-ttu-id="9ce1a-123">Azure 儲存檔案路徑</span><span class="sxs-lookup"><span data-stu-id="9ce1a-123">Azure storage file path</span></span>

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

### <span data-ttu-id="9ce1a-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="9ce1a-124">-FileSystem</span></span>
<span data-ttu-id="9ce1a-125">Azure ADLS gen2 檔案系統名稱</span><span class="sxs-lookup"><span data-stu-id="9ce1a-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="9ce1a-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="9ce1a-126">-FolderPath</span></span>
<span data-ttu-id="9ce1a-127">Azure 儲存資料夾路徑</span><span class="sxs-lookup"><span data-stu-id="9ce1a-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="9ce1a-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ce1a-128">-Name</span></span>
<span data-ttu-id="9ce1a-129">Azure 資料集的映射名稱</span><span class="sxs-lookup"><span data-stu-id="9ce1a-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="9ce1a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ce1a-130">-ResourceGroupName</span></span>
<span data-ttu-id="9ce1a-131">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="9ce1a-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9ce1a-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9ce1a-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="9ce1a-133">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="9ce1a-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9ce1a-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9ce1a-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="9ce1a-135">Azure 儲存體帳戶 ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ce1a-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="9ce1a-136">-確認</span><span class="sxs-lookup"><span data-stu-id="9ce1a-136">-Confirm</span></span>
<span data-ttu-id="9ce1a-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9ce1a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ce1a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ce1a-138">-WhatIf</span></span>
<span data-ttu-id="9ce1a-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ce1a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ce1a-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ce1a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ce1a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce1a-141">CommonParameters</span></span>
<span data-ttu-id="9ce1a-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9ce1a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce1a-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ce1a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce1a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="9ce1a-144">INPUTS</span></span>

### <span data-ttu-id="9ce1a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9ce1a-145">System.String</span></span>

## <span data-ttu-id="9ce1a-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9ce1a-146">OUTPUTS</span></span>

### <span data-ttu-id="9ce1a-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="9ce1a-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="9ce1a-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9ce1a-148">NOTES</span></span>

## <span data-ttu-id="9ce1a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ce1a-149">RELATED LINKS</span></span>
