---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 12c0c4832d13e3e8637ab1cdb36a1f3fe3abb7d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906230"
---
# <span data-ttu-id="eac8b-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="eac8b-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="eac8b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eac8b-102">SYNOPSIS</span></span>
<span data-ttu-id="eac8b-103">新增資料集至 Azure 資料共用。</span><span class="sxs-lookup"><span data-stu-id="eac8b-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="eac8b-104">語法</span><span class="sxs-lookup"><span data-stu-id="eac8b-104">SYNTAX</span></span>

### <span data-ttu-id="eac8b-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eac8b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac8b-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="eac8b-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac8b-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac8b-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac8b-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac8b-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac8b-109">描述</span><span class="sxs-lookup"><span data-stu-id="eac8b-109">DESCRIPTION</span></span>
<span data-ttu-id="eac8b-110">**New-AzDataShareDataSet** Cmdlet 在資料共用帳戶的 azure 資料共用中新增資料集。</span><span class="sxs-lookup"><span data-stu-id="eac8b-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="eac8b-111">您可以新增類型為 Blob、ADLS Gen2 和 ADLS Gen1 的資料集。</span><span class="sxs-lookup"><span data-stu-id="eac8b-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="eac8b-112">例子</span><span class="sxs-lookup"><span data-stu-id="eac8b-112">EXAMPLES</span></span>

### <span data-ttu-id="eac8b-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="eac8b-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="eac8b-114">此命令會將類型 Blob 容器的 AdsDataSet 資料集新增到 Azure 資料共用 AdsShare。</span><span class="sxs-lookup"><span data-stu-id="eac8b-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="eac8b-115">參數</span><span class="sxs-lookup"><span data-stu-id="eac8b-115">PARAMETERS</span></span>

### <span data-ttu-id="eac8b-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eac8b-116">-AccountName</span></span>
<span data-ttu-id="eac8b-117">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="eac8b-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac8b-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="eac8b-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="eac8b-119">Azure 儲存體 ADLS 第 1 代資料夾路徑</span><span class="sxs-lookup"><span data-stu-id="eac8b-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac8b-120">-Container</span><span class="sxs-lookup"><span data-stu-id="eac8b-120">-Container</span></span>
<span data-ttu-id="eac8b-121">Azure 儲存帳戶容器名稱</span><span class="sxs-lookup"><span data-stu-id="eac8b-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="eac8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac8b-122">-DefaultProfile</span></span>
<span data-ttu-id="eac8b-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eac8b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eac8b-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="eac8b-124">-FileName</span></span>
<span data-ttu-id="eac8b-125">Azure 儲存體 ADLS 第 1 代檔案名</span><span class="sxs-lookup"><span data-stu-id="eac8b-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac8b-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="eac8b-126">-FilePath</span></span>
<span data-ttu-id="eac8b-127">Azure 儲存檔案路徑</span><span class="sxs-lookup"><span data-stu-id="eac8b-127">Azure storage file path</span></span>

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

### <span data-ttu-id="eac8b-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="eac8b-128">-FileSystem</span></span>
<span data-ttu-id="eac8b-129">Azure ADLS gen2 檔案系統名稱</span><span class="sxs-lookup"><span data-stu-id="eac8b-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="eac8b-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="eac8b-130">-FolderPath</span></span>
<span data-ttu-id="eac8b-131">Azure 儲存資料夾路徑</span><span class="sxs-lookup"><span data-stu-id="eac8b-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="eac8b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="eac8b-132">-Name</span></span>
<span data-ttu-id="eac8b-133">Azure 資料集名稱</span><span class="sxs-lookup"><span data-stu-id="eac8b-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac8b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac8b-134">-ResourceGroupName</span></span>
<span data-ttu-id="eac8b-135">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="eac8b-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac8b-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="eac8b-136">-ShareName</span></span>
<span data-ttu-id="eac8b-137">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="eac8b-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac8b-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="eac8b-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="eac8b-139">Azure 儲存體帳戶 resourceId</span><span class="sxs-lookup"><span data-stu-id="eac8b-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac8b-140">-確認</span><span class="sxs-lookup"><span data-stu-id="eac8b-140">-Confirm</span></span>
<span data-ttu-id="eac8b-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eac8b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac8b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac8b-142">-WhatIf</span></span>
<span data-ttu-id="eac8b-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eac8b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac8b-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eac8b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac8b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac8b-145">CommonParameters</span></span>
<span data-ttu-id="eac8b-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eac8b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac8b-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eac8b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac8b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="eac8b-148">INPUTS</span></span>

### <span data-ttu-id="eac8b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="eac8b-149">System.String</span></span>

## <span data-ttu-id="eac8b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="eac8b-150">OUTPUTS</span></span>

### <span data-ttu-id="eac8b-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="eac8b-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="eac8b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="eac8b-152">NOTES</span></span>

## <span data-ttu-id="eac8b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="eac8b-153">RELATED LINKS</span></span>
