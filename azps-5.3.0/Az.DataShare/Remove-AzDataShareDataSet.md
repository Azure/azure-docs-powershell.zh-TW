---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286340"
---
# <span data-ttu-id="739af-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="739af-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="739af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="739af-102">SYNOPSIS</span></span>
<span data-ttu-id="739af-103">移除資料集對應</span><span class="sxs-lookup"><span data-stu-id="739af-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="739af-104">句法</span><span class="sxs-lookup"><span data-stu-id="739af-104">SYNTAX</span></span>

### <span data-ttu-id="739af-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="739af-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="739af-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="739af-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="739af-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="739af-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="739af-108">說明</span><span class="sxs-lookup"><span data-stu-id="739af-108">DESCRIPTION</span></span>
<span data-ttu-id="739af-109">**AzDataShareDataSet** Cmdlet 會移除資料集。</span><span class="sxs-lookup"><span data-stu-id="739af-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="739af-110">示例</span><span class="sxs-lookup"><span data-stu-id="739af-110">EXAMPLES</span></span>

### <span data-ttu-id="739af-111">範例1</span><span class="sxs-lookup"><span data-stu-id="739af-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="739af-112">這個命令會從 share WikiAds 中移除名為 DS 的資料集。</span><span class="sxs-lookup"><span data-stu-id="739af-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="739af-113">參數</span><span class="sxs-lookup"><span data-stu-id="739af-113">PARAMETERS</span></span>

### <span data-ttu-id="739af-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="739af-114">-AccountName</span></span>
<span data-ttu-id="739af-115">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="739af-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="739af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="739af-116">-DefaultProfile</span></span>
<span data-ttu-id="739af-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="739af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="739af-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="739af-118">-InputObject</span></span>
<span data-ttu-id="739af-119">Azure 資料集物件。</span><span class="sxs-lookup"><span data-stu-id="739af-119">The azure data set object.</span></span>


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

### <span data-ttu-id="739af-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="739af-120">-Name</span></span>
<span data-ttu-id="739af-121">Azure 資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="739af-121">Azure data set name.</span></span>

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

### <span data-ttu-id="739af-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="739af-122">-PassThru</span></span>
<span data-ttu-id="739af-123">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="739af-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="739af-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="739af-124">-ResourceGroupName</span></span>
<span data-ttu-id="739af-125">Azure 資料共用帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="739af-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="739af-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="739af-126">-ResourceId</span></span>
<span data-ttu-id="739af-127">Azure 資料集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="739af-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="739af-128">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="739af-128">-ShareName</span></span>
<span data-ttu-id="739af-129">Azure 資料共用名稱。</span><span class="sxs-lookup"><span data-stu-id="739af-129">Azure data share name.</span></span>

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

### <span data-ttu-id="739af-130">-確認</span><span class="sxs-lookup"><span data-stu-id="739af-130">-Confirm</span></span>
<span data-ttu-id="739af-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="739af-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="739af-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="739af-132">-WhatIf</span></span>
<span data-ttu-id="739af-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="739af-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="739af-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="739af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="739af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="739af-135">CommonParameters</span></span>
<span data-ttu-id="739af-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="739af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="739af-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="739af-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="739af-138">輸入</span><span class="sxs-lookup"><span data-stu-id="739af-138">INPUTS</span></span>

### <span data-ttu-id="739af-139">System.object</span><span class="sxs-lookup"><span data-stu-id="739af-139">System.String</span></span>

### <span data-ttu-id="739af-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="739af-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="739af-141">輸出</span><span class="sxs-lookup"><span data-stu-id="739af-141">OUTPUTS</span></span>

### <span data-ttu-id="739af-142">System.object</span><span class="sxs-lookup"><span data-stu-id="739af-142">System.Boolean</span></span>

## <span data-ttu-id="739af-143">筆記</span><span class="sxs-lookup"><span data-stu-id="739af-143">NOTES</span></span>

## <span data-ttu-id="739af-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="739af-144">RELATED LINKS</span></span>
