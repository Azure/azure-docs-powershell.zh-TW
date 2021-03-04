---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 535a3ea9eb0b0227be10475e4faffea5d9b697b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913674"
---
# <span data-ttu-id="c9341-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="c9341-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="c9341-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c9341-102">SYNOPSIS</span></span>
<span data-ttu-id="c9341-103">刪除 Active Directory 群組。</span><span class="sxs-lookup"><span data-stu-id="c9341-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="c9341-104">語法</span><span class="sxs-lookup"><span data-stu-id="c9341-104">SYNTAX</span></span>

### <span data-ttu-id="c9341-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c9341-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9341-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9341-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9341-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9341-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9341-108">描述</span><span class="sxs-lookup"><span data-stu-id="c9341-108">DESCRIPTION</span></span>
<span data-ttu-id="c9341-109">刪除 Active Directory 群組。</span><span class="sxs-lookup"><span data-stu-id="c9341-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="c9341-110">例子</span><span class="sxs-lookup"><span data-stu-id="c9341-110">EXAMPLES</span></span>

### <span data-ttu-id="c9341-111">範例 1：根據物件識別碼移除群組</span><span class="sxs-lookup"><span data-stu-id="c9341-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c9341-112">從租使用者移除物件識別碼為 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'的群組。</span><span class="sxs-lookup"><span data-stu-id="c9341-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="c9341-113">範例 2：使用管道移除群組</span><span class="sxs-lookup"><span data-stu-id="c9341-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="c9341-114">使用物件識別碼為 '85F89C90-780E-4AA6-9F4F-6F268D322EEE' 和管道到 Remove-AzADGroup 從租使用者移除群組的群組。</span><span class="sxs-lookup"><span data-stu-id="c9341-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="c9341-115">參數</span><span class="sxs-lookup"><span data-stu-id="c9341-115">PARAMETERS</span></span>

### <span data-ttu-id="c9341-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9341-116">-DefaultProfile</span></span>
<span data-ttu-id="c9341-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9341-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9341-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c9341-118">-DisplayName</span></span>
<span data-ttu-id="c9341-119">要移除之群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c9341-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9341-120">-強制</span><span class="sxs-lookup"><span data-stu-id="c9341-120">-Force</span></span>
<span data-ttu-id="c9341-121">如果指定，不會要求刪除群組的確認。</span><span class="sxs-lookup"><span data-stu-id="c9341-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="c9341-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9341-122">-InputObject</span></span>
<span data-ttu-id="c9341-123">要移除之群組的物件標記法。</span><span class="sxs-lookup"><span data-stu-id="c9341-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9341-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c9341-124">-ObjectId</span></span>
<span data-ttu-id="c9341-125">要移除之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9341-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9341-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9341-126">-PassThru</span></span>
<span data-ttu-id="c9341-127">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="c9341-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c9341-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c9341-128">-Confirm</span></span>
<span data-ttu-id="c9341-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c9341-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9341-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9341-130">-WhatIf</span></span>
<span data-ttu-id="c9341-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9341-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9341-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9341-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9341-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9341-133">CommonParameters</span></span>
<span data-ttu-id="c9341-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c9341-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9341-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9341-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9341-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c9341-136">INPUTS</span></span>

### <span data-ttu-id="c9341-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c9341-137">System.String</span></span>

### <span data-ttu-id="c9341-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c9341-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c9341-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c9341-139">OUTPUTS</span></span>

### <span data-ttu-id="c9341-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9341-140">System.Boolean</span></span>

## <span data-ttu-id="c9341-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c9341-141">NOTES</span></span>

## <span data-ttu-id="c9341-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9341-142">RELATED LINKS</span></span>