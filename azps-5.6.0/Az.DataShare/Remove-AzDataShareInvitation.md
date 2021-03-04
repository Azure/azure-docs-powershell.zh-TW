---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 4736a1b6e8d0a6d34cf1874868596d4139ad5e67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913533"
---
# <span data-ttu-id="06f09-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="06f09-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="06f09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06f09-102">SYNOPSIS</span></span>
<span data-ttu-id="06f09-103">移除邀請</span><span class="sxs-lookup"><span data-stu-id="06f09-103">removes an invitation</span></span>

## <span data-ttu-id="06f09-104">語法</span><span class="sxs-lookup"><span data-stu-id="06f09-104">SYNTAX</span></span>

### <span data-ttu-id="06f09-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="06f09-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06f09-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06f09-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f09-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06f09-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06f09-108">描述</span><span class="sxs-lookup"><span data-stu-id="06f09-108">DESCRIPTION</span></span>
<span data-ttu-id="06f09-109">**Remove-AzDataShareInvitation** Cmdlet 會移除資料共用邀請。</span><span class="sxs-lookup"><span data-stu-id="06f09-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="06f09-110">例子</span><span class="sxs-lookup"><span data-stu-id="06f09-110">EXAMPLES</span></span>

### <span data-ttu-id="06f09-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="06f09-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="06f09-112">這個命令會從 Share AdsShare 移除名為 ADSInvite 的邀請。</span><span class="sxs-lookup"><span data-stu-id="06f09-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="06f09-113">參數</span><span class="sxs-lookup"><span data-stu-id="06f09-113">PARAMETERS</span></span>

### <span data-ttu-id="06f09-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="06f09-114">-AccountName</span></span>
<span data-ttu-id="06f09-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="06f09-115">Azure data share account name</span></span>

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

### <span data-ttu-id="06f09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f09-116">-DefaultProfile</span></span>
<span data-ttu-id="06f09-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06f09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f09-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06f09-118">-InputObject</span></span>
<span data-ttu-id="06f09-119">Azure 資料共用邀請物件</span><span class="sxs-lookup"><span data-stu-id="06f09-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06f09-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="06f09-120">-Name</span></span>
<span data-ttu-id="06f09-121">Azure 資料共用邀請名稱</span><span class="sxs-lookup"><span data-stu-id="06f09-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="06f09-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06f09-122">-PassThru</span></span>
<span data-ttu-id="06f09-123">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="06f09-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="06f09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f09-124">-ResourceGroupName</span></span>
<span data-ttu-id="06f09-125">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="06f09-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="06f09-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06f09-126">-ResourceId</span></span>
<span data-ttu-id="06f09-127">Azure 資料共用邀請的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="06f09-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="06f09-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="06f09-128">-ShareName</span></span>
<span data-ttu-id="06f09-129">Azure 資料共用名稱。</span><span class="sxs-lookup"><span data-stu-id="06f09-129">Azure data share name.</span></span>

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

### <span data-ttu-id="06f09-130">-確認</span><span class="sxs-lookup"><span data-stu-id="06f09-130">-Confirm</span></span>
<span data-ttu-id="06f09-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06f09-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f09-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f09-132">-WhatIf</span></span>
<span data-ttu-id="06f09-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06f09-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f09-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06f09-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f09-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f09-135">CommonParameters</span></span>
<span data-ttu-id="06f09-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06f09-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f09-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06f09-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f09-138">輸入</span><span class="sxs-lookup"><span data-stu-id="06f09-138">INPUTS</span></span>

### <span data-ttu-id="06f09-139">System.String</span><span class="sxs-lookup"><span data-stu-id="06f09-139">System.String</span></span>

### <span data-ttu-id="06f09-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="06f09-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="06f09-141">輸出</span><span class="sxs-lookup"><span data-stu-id="06f09-141">OUTPUTS</span></span>

### <span data-ttu-id="06f09-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06f09-142">System.Boolean</span></span>

## <span data-ttu-id="06f09-143">筆記</span><span class="sxs-lookup"><span data-stu-id="06f09-143">NOTES</span></span>

## <span data-ttu-id="06f09-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="06f09-144">RELATED LINKS</span></span>
