---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 4cb023fecb020e37535f47823df6f02ee9f5050e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916421"
---
# <span data-ttu-id="57d70-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="57d70-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="57d70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57d70-102">SYNOPSIS</span></span>
<span data-ttu-id="57d70-103">移除共用訂閱</span><span class="sxs-lookup"><span data-stu-id="57d70-103">removes a share subscription</span></span>

## <span data-ttu-id="57d70-104">語法</span><span class="sxs-lookup"><span data-stu-id="57d70-104">SYNTAX</span></span>

### <span data-ttu-id="57d70-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="57d70-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57d70-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57d70-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57d70-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57d70-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57d70-108">描述</span><span class="sxs-lookup"><span data-stu-id="57d70-108">DESCRIPTION</span></span>
<span data-ttu-id="57d70-109">**Remove-AzDataShareSubscription** Cmdlet 會移除共用訂閱</span><span class="sxs-lookup"><span data-stu-id="57d70-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="57d70-110">例子</span><span class="sxs-lookup"><span data-stu-id="57d70-110">EXAMPLES</span></span>

### <span data-ttu-id="57d70-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="57d70-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="57d70-112">這個命令會從帳戶 WikiAds 移除名為 AdsShareSubscription 的共用訂閱。</span><span class="sxs-lookup"><span data-stu-id="57d70-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="57d70-113">參數</span><span class="sxs-lookup"><span data-stu-id="57d70-113">PARAMETERS</span></span>

### <span data-ttu-id="57d70-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57d70-114">-AccountName</span></span>
<span data-ttu-id="57d70-115">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="57d70-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="57d70-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57d70-116">-AsJob</span></span>
<span data-ttu-id="57d70-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="57d70-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="57d70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d70-118">-DefaultProfile</span></span>
<span data-ttu-id="57d70-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="57d70-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57d70-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57d70-120">-InputObject</span></span>
<span data-ttu-id="57d70-121">Azure 資料共用訂閱物件</span><span class="sxs-lookup"><span data-stu-id="57d70-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57d70-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="57d70-122">-Name</span></span>
<span data-ttu-id="57d70-123">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="57d70-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="57d70-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57d70-124">-PassThru</span></span>
<span data-ttu-id="57d70-125">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="57d70-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="57d70-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d70-126">-ResourceGroupName</span></span>
<span data-ttu-id="57d70-127">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="57d70-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="57d70-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57d70-128">-ResourceId</span></span>
<span data-ttu-id="57d70-129">Azure 資料共用訂閱的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="57d70-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="57d70-130">-確認</span><span class="sxs-lookup"><span data-stu-id="57d70-130">-Confirm</span></span>
<span data-ttu-id="57d70-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="57d70-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57d70-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d70-132">-WhatIf</span></span>
<span data-ttu-id="57d70-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57d70-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57d70-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57d70-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57d70-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d70-135">CommonParameters</span></span>
<span data-ttu-id="57d70-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57d70-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d70-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57d70-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d70-138">輸入</span><span class="sxs-lookup"><span data-stu-id="57d70-138">INPUTS</span></span>

### <span data-ttu-id="57d70-139">System.String</span><span class="sxs-lookup"><span data-stu-id="57d70-139">System.String</span></span>

### <span data-ttu-id="57d70-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="57d70-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="57d70-141">輸出</span><span class="sxs-lookup"><span data-stu-id="57d70-141">OUTPUTS</span></span>

### <span data-ttu-id="57d70-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57d70-142">System.Boolean</span></span>

## <span data-ttu-id="57d70-143">筆記</span><span class="sxs-lookup"><span data-stu-id="57d70-143">NOTES</span></span>

## <span data-ttu-id="57d70-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="57d70-144">RELATED LINKS</span></span>
