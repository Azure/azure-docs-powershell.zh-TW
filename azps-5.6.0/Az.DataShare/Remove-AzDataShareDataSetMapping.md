---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 8e3513621b94a7fc98a00b7eb443bef18d2a8141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911118"
---
# <span data-ttu-id="66af0-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="66af0-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="66af0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66af0-102">SYNOPSIS</span></span>
<span data-ttu-id="66af0-103">移除資料集地圖</span><span class="sxs-lookup"><span data-stu-id="66af0-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="66af0-104">語法</span><span class="sxs-lookup"><span data-stu-id="66af0-104">SYNTAX</span></span>

### <span data-ttu-id="66af0-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="66af0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66af0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66af0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66af0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66af0-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66af0-108">描述</span><span class="sxs-lookup"><span data-stu-id="66af0-108">DESCRIPTION</span></span>
<span data-ttu-id="66af0-109">**Remove-AzDataShareDataSetMapping** Cmdlet 會移除資料集的映射。</span><span class="sxs-lookup"><span data-stu-id="66af0-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="66af0-110">例子</span><span class="sxs-lookup"><span data-stu-id="66af0-110">EXAMPLES</span></span>

### <span data-ttu-id="66af0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="66af0-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="66af0-112">這個命令會從共用訂閱 WikiAds 移除名為 DSM 的資料集。</span><span class="sxs-lookup"><span data-stu-id="66af0-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="66af0-113">參數</span><span class="sxs-lookup"><span data-stu-id="66af0-113">PARAMETERS</span></span>

### <span data-ttu-id="66af0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66af0-114">-AccountName</span></span>
<span data-ttu-id="66af0-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="66af0-115">Azure data share account name</span></span>

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

### <span data-ttu-id="66af0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66af0-116">-DefaultProfile</span></span>
<span data-ttu-id="66af0-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="66af0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66af0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66af0-118">-InputObject</span></span>
<span data-ttu-id="66af0-119">Azure 資料集地圖物件</span><span class="sxs-lookup"><span data-stu-id="66af0-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66af0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="66af0-120">-Name</span></span>
<span data-ttu-id="66af0-121">Azure 資料集的映射名稱</span><span class="sxs-lookup"><span data-stu-id="66af0-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="66af0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66af0-122">-PassThru</span></span>
<span data-ttu-id="66af0-123">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="66af0-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="66af0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66af0-124">-ResourceGroupName</span></span>
<span data-ttu-id="66af0-125">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="66af0-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="66af0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66af0-126">-ResourceId</span></span>
<span data-ttu-id="66af0-127">Azure 資料集地圖的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="66af0-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="66af0-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="66af0-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="66af0-129">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="66af0-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="66af0-130">-確認</span><span class="sxs-lookup"><span data-stu-id="66af0-130">-Confirm</span></span>
<span data-ttu-id="66af0-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="66af0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66af0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66af0-132">-WhatIf</span></span>
<span data-ttu-id="66af0-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66af0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66af0-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66af0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66af0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66af0-135">CommonParameters</span></span>
<span data-ttu-id="66af0-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66af0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66af0-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66af0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66af0-138">輸入</span><span class="sxs-lookup"><span data-stu-id="66af0-138">INPUTS</span></span>

### <span data-ttu-id="66af0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="66af0-139">System.String</span></span>

### <span data-ttu-id="66af0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="66af0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="66af0-141">輸出</span><span class="sxs-lookup"><span data-stu-id="66af0-141">OUTPUTS</span></span>

### <span data-ttu-id="66af0-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66af0-142">System.Boolean</span></span>

## <span data-ttu-id="66af0-143">筆記</span><span class="sxs-lookup"><span data-stu-id="66af0-143">NOTES</span></span>

## <span data-ttu-id="66af0-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="66af0-144">RELATED LINKS</span></span>
