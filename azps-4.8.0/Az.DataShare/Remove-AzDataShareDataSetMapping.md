---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969268"
---
# <span data-ttu-id="89405-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="89405-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="89405-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89405-102">SYNOPSIS</span></span>
<span data-ttu-id="89405-103">移除資料集對應</span><span class="sxs-lookup"><span data-stu-id="89405-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="89405-104">句法</span><span class="sxs-lookup"><span data-stu-id="89405-104">SYNTAX</span></span>

### <span data-ttu-id="89405-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="89405-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89405-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89405-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89405-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89405-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89405-108">說明</span><span class="sxs-lookup"><span data-stu-id="89405-108">DESCRIPTION</span></span>
<span data-ttu-id="89405-109">**AzDataShareDataSetMapping** Cmdlet 會移除資料集對應。</span><span class="sxs-lookup"><span data-stu-id="89405-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="89405-110">示例</span><span class="sxs-lookup"><span data-stu-id="89405-110">EXAMPLES</span></span>

### <span data-ttu-id="89405-111">範例1</span><span class="sxs-lookup"><span data-stu-id="89405-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="89405-112">這個命令會從 sharesubscription WikiAds 中移除名為 DSM 的資料集。</span><span class="sxs-lookup"><span data-stu-id="89405-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="89405-113">參數</span><span class="sxs-lookup"><span data-stu-id="89405-113">PARAMETERS</span></span>

### <span data-ttu-id="89405-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89405-114">-AccountName</span></span>
<span data-ttu-id="89405-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="89405-115">Azure data share account name</span></span>

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

### <span data-ttu-id="89405-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89405-116">-DefaultProfile</span></span>
<span data-ttu-id="89405-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89405-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89405-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89405-118">-InputObject</span></span>
<span data-ttu-id="89405-119">Azure 資料集對應物件</span><span class="sxs-lookup"><span data-stu-id="89405-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="89405-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="89405-120">-Name</span></span>
<span data-ttu-id="89405-121">Azure 資料集對應名稱</span><span class="sxs-lookup"><span data-stu-id="89405-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="89405-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89405-122">-PassThru</span></span>
<span data-ttu-id="89405-123">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="89405-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="89405-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89405-124">-ResourceGroupName</span></span>
<span data-ttu-id="89405-125">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="89405-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="89405-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89405-126">-ResourceId</span></span>
<span data-ttu-id="89405-127">Azure 資料集對應的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="89405-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="89405-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="89405-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="89405-129">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="89405-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="89405-130">-確認</span><span class="sxs-lookup"><span data-stu-id="89405-130">-Confirm</span></span>
<span data-ttu-id="89405-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89405-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89405-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89405-132">-WhatIf</span></span>
<span data-ttu-id="89405-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89405-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89405-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89405-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89405-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89405-135">CommonParameters</span></span>
<span data-ttu-id="89405-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89405-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89405-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="89405-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89405-138">輸入</span><span class="sxs-lookup"><span data-stu-id="89405-138">INPUTS</span></span>

### <span data-ttu-id="89405-139">System.object</span><span class="sxs-lookup"><span data-stu-id="89405-139">System.String</span></span>

### <span data-ttu-id="89405-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="89405-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="89405-141">輸出</span><span class="sxs-lookup"><span data-stu-id="89405-141">OUTPUTS</span></span>

### <span data-ttu-id="89405-142">System.object</span><span class="sxs-lookup"><span data-stu-id="89405-142">System.Boolean</span></span>

## <span data-ttu-id="89405-143">筆記</span><span class="sxs-lookup"><span data-stu-id="89405-143">NOTES</span></span>

## <span data-ttu-id="89405-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="89405-144">RELATED LINKS</span></span>
