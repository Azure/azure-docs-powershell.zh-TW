---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: a401471840821c5ec3292c8a40d6226d355e01b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956746"
---
# <span data-ttu-id="c8c1c-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="c8c1c-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="c8c1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c1c-103">刪除 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="c8c1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8c1c-104">SYNTAX</span></span>

### <span data-ttu-id="c8c1c-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8c1c-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8c1c-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8c1c-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8c1c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8c1c-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8c1c-108">說明</span><span class="sxs-lookup"><span data-stu-id="c8c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c8c1c-109">刪除 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="c8c1c-110">示例</span><span class="sxs-lookup"><span data-stu-id="c8c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="c8c1c-111">範例 1-依物件識別碼移除群組</span><span class="sxs-lookup"><span data-stu-id="c8c1c-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c8c1c-112">從租使用者移除物件 id 為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」的群組。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="c8c1c-113">範例 2-依管道移除群組</span><span class="sxs-lookup"><span data-stu-id="c8c1c-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="c8c1c-114">取得物件識別碼為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」的群組，以及要 Remove-AzADGroup 以從租使用者移除群組的管道。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="c8c1c-115">參數</span><span class="sxs-lookup"><span data-stu-id="c8c1c-115">PARAMETERS</span></span>

### <span data-ttu-id="c8c1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c1c-116">-DefaultProfile</span></span>
<span data-ttu-id="c8c1c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c1c-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c8c1c-118">-DisplayName</span></span>
<span data-ttu-id="c8c1c-119">要移除之群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="c8c1c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c8c1c-120">-Force</span></span>
<span data-ttu-id="c8c1c-121">如果已指定，就不會要求您刪除群組的確認。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="c8c1c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8c1c-122">-InputObject</span></span>
<span data-ttu-id="c8c1c-123">要移除之群組的物件表示。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-123">The object representation of the group to be removed.</span></span>

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

### <span data-ttu-id="c8c1c-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c8c1c-124">-ObjectId</span></span>
<span data-ttu-id="c8c1c-125">要移除之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-125">The object id of the group to be removed.</span></span>

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

### <span data-ttu-id="c8c1c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8c1c-126">-PassThru</span></span>
<span data-ttu-id="c8c1c-127">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c8c1c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c8c1c-128">-Confirm</span></span>
<span data-ttu-id="c8c1c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8c1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8c1c-130">-WhatIf</span></span>
<span data-ttu-id="c8c1c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8c1c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8c1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c1c-133">CommonParameters</span></span>
<span data-ttu-id="c8c1c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c1c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c1c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c8c1c-136">INPUTS</span></span>

### <span data-ttu-id="c8c1c-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c8c1c-137">System.String</span></span>

### <span data-ttu-id="c8c1c-138">PSADGroup （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c8c1c-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c8c1c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c8c1c-139">OUTPUTS</span></span>

### <span data-ttu-id="c8c1c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="c8c1c-140">System.Boolean</span></span>

## <span data-ttu-id="c8c1c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c8c1c-141">NOTES</span></span>

## <span data-ttu-id="c8c1c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8c1c-142">RELATED LINKS</span></span>
