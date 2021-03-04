---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 74651ea4a9a108db9cc3f666ad6f78f494fcd676
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906702"
---
# <span data-ttu-id="69fbd-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="69fbd-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="69fbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="69fbd-103">移除資料共用帳戶</span><span class="sxs-lookup"><span data-stu-id="69fbd-103">Removes a datashare account</span></span>

## <span data-ttu-id="69fbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="69fbd-104">SYNTAX</span></span>

### <span data-ttu-id="69fbd-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="69fbd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69fbd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fbd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69fbd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fbd-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69fbd-108">描述</span><span class="sxs-lookup"><span data-stu-id="69fbd-108">DESCRIPTION</span></span>
<span data-ttu-id="69fbd-109">**Remove-AzDataShareAccount** Cmdlet 會移除資料共用帳戶。</span><span class="sxs-lookup"><span data-stu-id="69fbd-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="69fbd-110">例子</span><span class="sxs-lookup"><span data-stu-id="69fbd-110">EXAMPLES</span></span>

### <span data-ttu-id="69fbd-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="69fbd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="69fbd-112">此命令會從名為 ADS 的資源群組移除名為 WikiADS 的資料共用帳戶。</span><span class="sxs-lookup"><span data-stu-id="69fbd-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="69fbd-113">此命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="69fbd-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="69fbd-114">參數</span><span class="sxs-lookup"><span data-stu-id="69fbd-114">PARAMETERS</span></span>

### <span data-ttu-id="69fbd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69fbd-115">-AsJob</span></span>
<span data-ttu-id="69fbd-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="69fbd-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="69fbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fbd-117">-DefaultProfile</span></span>
<span data-ttu-id="69fbd-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="69fbd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69fbd-119">-強制</span><span class="sxs-lookup"><span data-stu-id="69fbd-119">-Force</span></span>
<span data-ttu-id="69fbd-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="69fbd-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="69fbd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69fbd-121">-InputObject</span></span>
<span data-ttu-id="69fbd-122">Azure 資料共用帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="69fbd-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69fbd-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="69fbd-123">-Name</span></span>
<span data-ttu-id="69fbd-124">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="69fbd-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="69fbd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69fbd-125">-PassThru</span></span>
<span data-ttu-id="69fbd-126">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="69fbd-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="69fbd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69fbd-127">-ResourceGroupName</span></span>
<span data-ttu-id="69fbd-128">Azure 資料共用帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="69fbd-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="69fbd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69fbd-129">-ResourceId</span></span>
<span data-ttu-id="69fbd-130">Azure 資料共用帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="69fbd-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="69fbd-131">-確認</span><span class="sxs-lookup"><span data-stu-id="69fbd-131">-Confirm</span></span>
<span data-ttu-id="69fbd-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="69fbd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69fbd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69fbd-133">-WhatIf</span></span>
<span data-ttu-id="69fbd-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69fbd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69fbd-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69fbd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69fbd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fbd-136">CommonParameters</span></span>
<span data-ttu-id="69fbd-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69fbd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fbd-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69fbd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fbd-139">輸入</span><span class="sxs-lookup"><span data-stu-id="69fbd-139">INPUTS</span></span>

### <span data-ttu-id="69fbd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="69fbd-140">System.String</span></span>

### <span data-ttu-id="69fbd-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="69fbd-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="69fbd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="69fbd-142">OUTPUTS</span></span>

### <span data-ttu-id="69fbd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69fbd-143">System.Boolean</span></span>

## <span data-ttu-id="69fbd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="69fbd-144">NOTES</span></span>

## <span data-ttu-id="69fbd-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="69fbd-145">RELATED LINKS</span></span>
