---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969271"
---
# <span data-ttu-id="4e6b8-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="4e6b8-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="4e6b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6b8-103">移除 datashare 帳戶</span><span class="sxs-lookup"><span data-stu-id="4e6b8-103">Removes a datashare account</span></span>

## <span data-ttu-id="4e6b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e6b8-104">SYNTAX</span></span>

### <span data-ttu-id="4e6b8-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4e6b8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e6b8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e6b8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e6b8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e6b8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e6b8-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e6b8-108">DESCRIPTION</span></span>
<span data-ttu-id="4e6b8-109">**AzDataShareAccount** Cmdlet 會移除 datashare 帳戶。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="4e6b8-110">示例</span><span class="sxs-lookup"><span data-stu-id="4e6b8-110">EXAMPLES</span></span>

### <span data-ttu-id="4e6b8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4e6b8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="4e6b8-112">這個命令會從名為 [ADS] 的資源群組中移除名為 WikiADS 的 datashare 帳戶。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="4e6b8-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="4e6b8-114">參數</span><span class="sxs-lookup"><span data-stu-id="4e6b8-114">PARAMETERS</span></span>

### <span data-ttu-id="4e6b8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e6b8-115">-AsJob</span></span>
<span data-ttu-id="4e6b8-116">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="4e6b8-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="4e6b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6b8-117">-DefaultProfile</span></span>
<span data-ttu-id="4e6b8-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e6b8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4e6b8-119">-Force</span></span>
<span data-ttu-id="4e6b8-120">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="4e6b8-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="4e6b8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e6b8-121">-InputObject</span></span>
<span data-ttu-id="4e6b8-122">Azure data share 帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-122">The azure data share account object.</span></span>


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

### <span data-ttu-id="4e6b8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e6b8-123">-Name</span></span>
<span data-ttu-id="4e6b8-124">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="4e6b8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e6b8-125">-PassThru</span></span>
<span data-ttu-id="4e6b8-126">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="4e6b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e6b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="4e6b8-128">Azure 資料共用帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="4e6b8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e6b8-129">-ResourceId</span></span>
<span data-ttu-id="4e6b8-130">Azure 資料共用帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="4e6b8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4e6b8-131">-Confirm</span></span>
<span data-ttu-id="4e6b8-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e6b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e6b8-133">-WhatIf</span></span>
<span data-ttu-id="4e6b8-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e6b8-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e6b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6b8-136">CommonParameters</span></span>
<span data-ttu-id="4e6b8-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6b8-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6b8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4e6b8-139">INPUTS</span></span>

### <span data-ttu-id="4e6b8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="4e6b8-140">System.String</span></span>

### <span data-ttu-id="4e6b8-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="4e6b8-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="4e6b8-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4e6b8-142">OUTPUTS</span></span>

### <span data-ttu-id="4e6b8-143">System.object</span><span class="sxs-lookup"><span data-stu-id="4e6b8-143">System.Boolean</span></span>

## <span data-ttu-id="4e6b8-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4e6b8-144">NOTES</span></span>

## <span data-ttu-id="4e6b8-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e6b8-145">RELATED LINKS</span></span>