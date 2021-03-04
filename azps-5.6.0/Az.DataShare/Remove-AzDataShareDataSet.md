---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 8ede4fe94eccd9d9f08977a0af9cc8847e4aca1f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915513"
---
# <span data-ttu-id="33e34-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="33e34-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="33e34-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33e34-102">SYNOPSIS</span></span>
<span data-ttu-id="33e34-103">移除資料集地圖</span><span class="sxs-lookup"><span data-stu-id="33e34-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="33e34-104">語法</span><span class="sxs-lookup"><span data-stu-id="33e34-104">SYNTAX</span></span>

### <span data-ttu-id="33e34-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="33e34-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33e34-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33e34-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33e34-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33e34-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33e34-108">描述</span><span class="sxs-lookup"><span data-stu-id="33e34-108">DESCRIPTION</span></span>
<span data-ttu-id="33e34-109">**Remove-AzDataShareDataSet** Cmdlet 會移除資料集。</span><span class="sxs-lookup"><span data-stu-id="33e34-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="33e34-110">例子</span><span class="sxs-lookup"><span data-stu-id="33e34-110">EXAMPLES</span></span>

### <span data-ttu-id="33e34-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="33e34-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="33e34-112">這個命令會從共用 WikiAds 移除名為 DS 的資料集。</span><span class="sxs-lookup"><span data-stu-id="33e34-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="33e34-113">參數</span><span class="sxs-lookup"><span data-stu-id="33e34-113">PARAMETERS</span></span>

### <span data-ttu-id="33e34-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33e34-114">-AccountName</span></span>
<span data-ttu-id="33e34-115">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="33e34-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e34-116">-DefaultProfile</span></span>
<span data-ttu-id="33e34-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33e34-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33e34-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33e34-118">-InputObject</span></span>
<span data-ttu-id="33e34-119">Azure 資料集物件。</span><span class="sxs-lookup"><span data-stu-id="33e34-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33e34-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="33e34-120">-Name</span></span>
<span data-ttu-id="33e34-121">Azure 資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="33e34-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e34-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33e34-122">-PassThru</span></span>
<span data-ttu-id="33e34-123">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="33e34-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="33e34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e34-124">-ResourceGroupName</span></span>
<span data-ttu-id="33e34-125">Azure 資料共用帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="33e34-125">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e34-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33e34-126">-ResourceId</span></span>
<span data-ttu-id="33e34-127">Azure 資料集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="33e34-127">The resource id of the azure data set.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e34-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="33e34-128">-ShareName</span></span>
<span data-ttu-id="33e34-129">Azure 資料共用名稱。</span><span class="sxs-lookup"><span data-stu-id="33e34-129">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e34-130">-確認</span><span class="sxs-lookup"><span data-stu-id="33e34-130">-Confirm</span></span>
<span data-ttu-id="33e34-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="33e34-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33e34-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33e34-132">-WhatIf</span></span>
<span data-ttu-id="33e34-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33e34-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33e34-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33e34-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33e34-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e34-135">CommonParameters</span></span>
<span data-ttu-id="33e34-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33e34-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e34-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33e34-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e34-138">輸入</span><span class="sxs-lookup"><span data-stu-id="33e34-138">INPUTS</span></span>

### <span data-ttu-id="33e34-139">System.String</span><span class="sxs-lookup"><span data-stu-id="33e34-139">System.String</span></span>

### <span data-ttu-id="33e34-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="33e34-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="33e34-141">輸出</span><span class="sxs-lookup"><span data-stu-id="33e34-141">OUTPUTS</span></span>

### <span data-ttu-id="33e34-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33e34-142">System.Boolean</span></span>

## <span data-ttu-id="33e34-143">筆記</span><span class="sxs-lookup"><span data-stu-id="33e34-143">NOTES</span></span>

## <span data-ttu-id="33e34-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="33e34-144">RELATED LINKS</span></span>
