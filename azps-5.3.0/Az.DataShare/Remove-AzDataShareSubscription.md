---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286328"
---
# <span data-ttu-id="538ba-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="538ba-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="538ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="538ba-102">SYNOPSIS</span></span>
<span data-ttu-id="538ba-103">移除共用訂閱</span><span class="sxs-lookup"><span data-stu-id="538ba-103">removes a share subscription</span></span>

## <span data-ttu-id="538ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="538ba-104">SYNTAX</span></span>

### <span data-ttu-id="538ba-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="538ba-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="538ba-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="538ba-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="538ba-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="538ba-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="538ba-108">說明</span><span class="sxs-lookup"><span data-stu-id="538ba-108">DESCRIPTION</span></span>
<span data-ttu-id="538ba-109">**AzDataShareSubscription** Cmdlet 會移除共用訂閱</span><span class="sxs-lookup"><span data-stu-id="538ba-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="538ba-110">示例</span><span class="sxs-lookup"><span data-stu-id="538ba-110">EXAMPLES</span></span>

### <span data-ttu-id="538ba-111">範例1</span><span class="sxs-lookup"><span data-stu-id="538ba-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="538ba-112">這個命令會從帳戶 WikiAds 中移除一個名為 AdsShareSubscription 的 sharesubscription。</span><span class="sxs-lookup"><span data-stu-id="538ba-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="538ba-113">參數</span><span class="sxs-lookup"><span data-stu-id="538ba-113">PARAMETERS</span></span>

### <span data-ttu-id="538ba-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="538ba-114">-AccountName</span></span>
<span data-ttu-id="538ba-115">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="538ba-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="538ba-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="538ba-116">-AsJob</span></span>
<span data-ttu-id="538ba-117">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="538ba-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="538ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538ba-118">-DefaultProfile</span></span>
<span data-ttu-id="538ba-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="538ba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="538ba-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="538ba-120">-InputObject</span></span>
<span data-ttu-id="538ba-121">Azure data share 訂閱物件</span><span class="sxs-lookup"><span data-stu-id="538ba-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="538ba-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="538ba-122">-Name</span></span>
<span data-ttu-id="538ba-123">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="538ba-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="538ba-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="538ba-124">-PassThru</span></span>
<span data-ttu-id="538ba-125">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="538ba-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="538ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="538ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="538ba-127">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="538ba-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="538ba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="538ba-128">-ResourceId</span></span>
<span data-ttu-id="538ba-129">Azure 資料共用訂閱的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="538ba-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="538ba-130">-確認</span><span class="sxs-lookup"><span data-stu-id="538ba-130">-Confirm</span></span>
<span data-ttu-id="538ba-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="538ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="538ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="538ba-132">-WhatIf</span></span>
<span data-ttu-id="538ba-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="538ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="538ba-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="538ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="538ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538ba-135">CommonParameters</span></span>
<span data-ttu-id="538ba-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="538ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538ba-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="538ba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538ba-138">輸入</span><span class="sxs-lookup"><span data-stu-id="538ba-138">INPUTS</span></span>

### <span data-ttu-id="538ba-139">System.object</span><span class="sxs-lookup"><span data-stu-id="538ba-139">System.String</span></span>

### <span data-ttu-id="538ba-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="538ba-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="538ba-141">輸出</span><span class="sxs-lookup"><span data-stu-id="538ba-141">OUTPUTS</span></span>

### <span data-ttu-id="538ba-142">System.object</span><span class="sxs-lookup"><span data-stu-id="538ba-142">System.Boolean</span></span>

## <span data-ttu-id="538ba-143">筆記</span><span class="sxs-lookup"><span data-stu-id="538ba-143">NOTES</span></span>

## <span data-ttu-id="538ba-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="538ba-144">RELATED LINKS</span></span>
