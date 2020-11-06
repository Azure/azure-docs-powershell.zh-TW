---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 9aee75f06ca1c97b691ae607e4c9eaa3accd74e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612631"
---
# <span data-ttu-id="c11b3-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="c11b3-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="c11b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c11b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c11b3-103">移除邀請</span><span class="sxs-lookup"><span data-stu-id="c11b3-103">removes an invitation</span></span>

## <span data-ttu-id="c11b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c11b3-104">SYNTAX</span></span>

### <span data-ttu-id="c11b3-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c11b3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c11b3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c11b3-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c11b3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c11b3-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c11b3-108">說明</span><span class="sxs-lookup"><span data-stu-id="c11b3-108">DESCRIPTION</span></span>
<span data-ttu-id="c11b3-109">**AzDataShareInvitation** Cmdlet 會移除 datashare 邀請。</span><span class="sxs-lookup"><span data-stu-id="c11b3-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="c11b3-110">示例</span><span class="sxs-lookup"><span data-stu-id="c11b3-110">EXAMPLES</span></span>

### <span data-ttu-id="c11b3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c11b3-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c11b3-112">這個命令會從 share AdsShare 中移除名為 ADSInvite 的邀請。</span><span class="sxs-lookup"><span data-stu-id="c11b3-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="c11b3-113">參數</span><span class="sxs-lookup"><span data-stu-id="c11b3-113">PARAMETERS</span></span>

### <span data-ttu-id="c11b3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c11b3-114">-AccountName</span></span>
<span data-ttu-id="c11b3-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="c11b3-115">Azure data share account name</span></span>

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

### <span data-ttu-id="c11b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11b3-116">-DefaultProfile</span></span>
<span data-ttu-id="c11b3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c11b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c11b3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c11b3-118">-InputObject</span></span>
<span data-ttu-id="c11b3-119">Azure 資料共用邀請物件</span><span class="sxs-lookup"><span data-stu-id="c11b3-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="c11b3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c11b3-120">-Name</span></span>
<span data-ttu-id="c11b3-121">Azure 資料共用邀請名稱</span><span class="sxs-lookup"><span data-stu-id="c11b3-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="c11b3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c11b3-122">-PassThru</span></span>
<span data-ttu-id="c11b3-123">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="c11b3-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="c11b3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c11b3-124">-ResourceGroupName</span></span>
<span data-ttu-id="c11b3-125">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="c11b3-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c11b3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c11b3-126">-ResourceId</span></span>
<span data-ttu-id="c11b3-127">Azure 資料共用邀請的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c11b3-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="c11b3-128">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="c11b3-128">-ShareName</span></span>
<span data-ttu-id="c11b3-129">Azure 資料共用名稱。</span><span class="sxs-lookup"><span data-stu-id="c11b3-129">Azure data share name.</span></span>

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

### <span data-ttu-id="c11b3-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c11b3-130">-Confirm</span></span>
<span data-ttu-id="c11b3-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c11b3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c11b3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c11b3-132">-WhatIf</span></span>
<span data-ttu-id="c11b3-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c11b3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c11b3-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c11b3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c11b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11b3-135">CommonParameters</span></span>
<span data-ttu-id="c11b3-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c11b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11b3-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c11b3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11b3-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c11b3-138">INPUTS</span></span>

### <span data-ttu-id="c11b3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="c11b3-139">System.String</span></span>

### <span data-ttu-id="c11b3-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="c11b3-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="c11b3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c11b3-141">OUTPUTS</span></span>

### <span data-ttu-id="c11b3-142">System.object</span><span class="sxs-lookup"><span data-stu-id="c11b3-142">System.Boolean</span></span>

## <span data-ttu-id="c11b3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c11b3-143">NOTES</span></span>

## <span data-ttu-id="c11b3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c11b3-144">RELATED LINKS</span></span>