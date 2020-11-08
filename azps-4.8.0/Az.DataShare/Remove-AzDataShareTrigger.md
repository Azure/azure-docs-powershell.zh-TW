---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: f4eff969d93f1c243b9dc15652249bc9800bfd45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969262"
---
# <span data-ttu-id="e46ef-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="e46ef-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="e46ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e46ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e46ef-103">移除觸發程式</span><span class="sxs-lookup"><span data-stu-id="e46ef-103">removes a trigger</span></span>

## <span data-ttu-id="e46ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="e46ef-104">SYNTAX</span></span>

### <span data-ttu-id="e46ef-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e46ef-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e46ef-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e46ef-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e46ef-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e46ef-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e46ef-108">說明</span><span class="sxs-lookup"><span data-stu-id="e46ef-108">DESCRIPTION</span></span>
<span data-ttu-id="e46ef-109">AzDataShareTrigger Cmdlet 會移除 datashare 觸發 **程式**</span><span class="sxs-lookup"><span data-stu-id="e46ef-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="e46ef-110">示例</span><span class="sxs-lookup"><span data-stu-id="e46ef-110">EXAMPLES</span></span>

### <span data-ttu-id="e46ef-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e46ef-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="e46ef-112">這個命令會從 [共用訂閱 AdsShareSubscription] 移除名為 AdsTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e46ef-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="e46ef-113">參數</span><span class="sxs-lookup"><span data-stu-id="e46ef-113">PARAMETERS</span></span>

### <span data-ttu-id="e46ef-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e46ef-114">-AccountName</span></span>
<span data-ttu-id="e46ef-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="e46ef-115">Azure data share account name</span></span>

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

### <span data-ttu-id="e46ef-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e46ef-116">-AsJob</span></span>
<span data-ttu-id="e46ef-117">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="e46ef-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="e46ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46ef-118">-DefaultProfile</span></span>
<span data-ttu-id="e46ef-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e46ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e46ef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e46ef-120">-InputObject</span></span>
<span data-ttu-id="e46ef-121">Azure 資料共用觸發程式物件</span><span class="sxs-lookup"><span data-stu-id="e46ef-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e46ef-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e46ef-122">-Name</span></span>
<span data-ttu-id="e46ef-123">Azure 資料共用觸發程式名稱</span><span class="sxs-lookup"><span data-stu-id="e46ef-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="e46ef-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e46ef-124">-PassThru</span></span>
<span data-ttu-id="e46ef-125">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="e46ef-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="e46ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="e46ef-127">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="e46ef-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e46ef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e46ef-128">-ResourceId</span></span>
<span data-ttu-id="e46ef-129">Azure 資料共用觸發程式的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e46ef-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="e46ef-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e46ef-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="e46ef-131">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="e46ef-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46ef-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e46ef-132">-Confirm</span></span>
<span data-ttu-id="e46ef-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e46ef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e46ef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e46ef-134">-WhatIf</span></span>
<span data-ttu-id="e46ef-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e46ef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e46ef-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e46ef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e46ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46ef-137">CommonParameters</span></span>
<span data-ttu-id="e46ef-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e46ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46ef-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e46ef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46ef-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e46ef-140">INPUTS</span></span>

### <span data-ttu-id="e46ef-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e46ef-141">System.String</span></span>

### <span data-ttu-id="e46ef-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="e46ef-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="e46ef-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e46ef-143">OUTPUTS</span></span>

### <span data-ttu-id="e46ef-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e46ef-144">System.Boolean</span></span>

## <span data-ttu-id="e46ef-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e46ef-145">NOTES</span></span>

## <span data-ttu-id="e46ef-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e46ef-146">RELATED LINKS</span></span>
