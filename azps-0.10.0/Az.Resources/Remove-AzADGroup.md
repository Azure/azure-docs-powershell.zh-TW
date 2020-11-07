---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 4d285471632c9c4bc952b2dcdc0e4ce5147fac12
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795254"
---
# <span data-ttu-id="d3c9e-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="d3c9e-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="d3c9e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c9e-103">刪除 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="d3c9e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3c9e-104">SYNTAX</span></span>

### <span data-ttu-id="d3c9e-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d3c9e-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3c9e-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3c9e-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3c9e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3c9e-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c9e-108">說明</span><span class="sxs-lookup"><span data-stu-id="d3c9e-108">DESCRIPTION</span></span>
<span data-ttu-id="d3c9e-109">刪除 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="d3c9e-110">示例</span><span class="sxs-lookup"><span data-stu-id="d3c9e-110">EXAMPLES</span></span>

### <span data-ttu-id="d3c9e-111">範例 1-依物件識別碼移除群組</span><span class="sxs-lookup"><span data-stu-id="d3c9e-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="d3c9e-112">從租使用者移除物件 id 為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」的群組。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="d3c9e-113">範例 2-依管道移除群組</span><span class="sxs-lookup"><span data-stu-id="d3c9e-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="d3c9e-114">取得物件識別碼為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」的群組，以及要 Remove-AzADGroup 以從租使用者移除群組的管道。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="d3c9e-115">參數</span><span class="sxs-lookup"><span data-stu-id="d3c9e-115">PARAMETERS</span></span>

### <span data-ttu-id="d3c9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c9e-116">-DefaultProfile</span></span>
<span data-ttu-id="d3c9e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c9e-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d3c9e-118">-DisplayName</span></span>
<span data-ttu-id="d3c9e-119">要移除之群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="d3c9e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d3c9e-120">-Force</span></span>
<span data-ttu-id="d3c9e-121">如果已指定，就不會要求您刪除群組的確認。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c9e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3c9e-122">-InputObject</span></span>
<span data-ttu-id="d3c9e-123">要移除之群組的物件表示。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c9e-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d3c9e-124">-ObjectId</span></span>
<span data-ttu-id="d3c9e-125">要移除之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c9e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3c9e-126">-PassThru</span></span>
<span data-ttu-id="d3c9e-127">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c9e-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d3c9e-128">-Confirm</span></span>
<span data-ttu-id="d3c9e-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3c9e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3c9e-130">-WhatIf</span></span>
<span data-ttu-id="d3c9e-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3c9e-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3c9e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c9e-133">CommonParameters</span></span>
<span data-ttu-id="d3c9e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c9e-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d3c9e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c9e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d3c9e-136">INPUTS</span></span>

### <span data-ttu-id="d3c9e-137">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="d3c9e-137">System.Guid</span></span>

### <span data-ttu-id="d3c9e-138">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup</span><span class="sxs-lookup"><span data-stu-id="d3c9e-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="d3c9e-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d3c9e-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d3c9e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d3c9e-140">OUTPUTS</span></span>

### <span data-ttu-id="d3c9e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d3c9e-141">System.Boolean</span></span>

## <span data-ttu-id="d3c9e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d3c9e-142">NOTES</span></span>

## <span data-ttu-id="d3c9e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3c9e-143">RELATED LINKS</span></span>
