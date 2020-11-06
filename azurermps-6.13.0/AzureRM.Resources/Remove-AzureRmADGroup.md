---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
ms.openlocfilehash: f9aa1f3d45a50a59c118abea4278bfed1725fa9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448251"
---
# <span data-ttu-id="6cea6-101">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="6cea6-101">Remove-AzureRmADGroup</span></span>

## <span data-ttu-id="6cea6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6cea6-102">SYNOPSIS</span></span>
<span data-ttu-id="6cea6-103">刪除 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="6cea6-103">Deletes an active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cea6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6cea6-104">SYNTAX</span></span>

### <span data-ttu-id="6cea6-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6cea6-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cea6-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cea6-106">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cea6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cea6-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cea6-108">說明</span><span class="sxs-lookup"><span data-stu-id="6cea6-108">DESCRIPTION</span></span>
<span data-ttu-id="6cea6-109">刪除 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="6cea6-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="6cea6-110">示例</span><span class="sxs-lookup"><span data-stu-id="6cea6-110">EXAMPLES</span></span>

### <span data-ttu-id="6cea6-111">範例 1-依物件識別碼移除群組</span><span class="sxs-lookup"><span data-stu-id="6cea6-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="6cea6-112">從租使用者移除物件 id 為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」的群組。</span><span class="sxs-lookup"><span data-stu-id="6cea6-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="6cea6-113">範例 2-依管道移除群組</span><span class="sxs-lookup"><span data-stu-id="6cea6-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroup
```

<span data-ttu-id="6cea6-114">取得物件識別碼為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」的群組，以及要 Remove-AzureRmADGroup 以從租使用者移除群組的管道。</span><span class="sxs-lookup"><span data-stu-id="6cea6-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzureRmADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="6cea6-115">參數</span><span class="sxs-lookup"><span data-stu-id="6cea6-115">PARAMETERS</span></span>

### <span data-ttu-id="6cea6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cea6-116">-DefaultProfile</span></span>
<span data-ttu-id="6cea6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6cea6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cea6-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6cea6-118">-DisplayName</span></span>
<span data-ttu-id="6cea6-119">要移除之群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="6cea6-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="6cea6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6cea6-120">-Force</span></span>
<span data-ttu-id="6cea6-121">如果已指定，就不會要求您刪除群組的確認。</span><span class="sxs-lookup"><span data-stu-id="6cea6-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="6cea6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cea6-122">-InputObject</span></span>
<span data-ttu-id="6cea6-123">要移除之群組的物件表示。</span><span class="sxs-lookup"><span data-stu-id="6cea6-123">The object representation of the group to be removed.</span></span>

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

### <span data-ttu-id="6cea6-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6cea6-124">-ObjectId</span></span>
<span data-ttu-id="6cea6-125">要移除之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cea6-125">The object id of the group to be removed.</span></span>

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

### <span data-ttu-id="6cea6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cea6-126">-PassThru</span></span>
<span data-ttu-id="6cea6-127">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6cea6-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6cea6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6cea6-128">-Confirm</span></span>
<span data-ttu-id="6cea6-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6cea6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cea6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cea6-130">-WhatIf</span></span>
<span data-ttu-id="6cea6-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6cea6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cea6-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6cea6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cea6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cea6-133">CommonParameters</span></span>
<span data-ttu-id="6cea6-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6cea6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cea6-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6cea6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cea6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6cea6-136">INPUTS</span></span>

### <span data-ttu-id="6cea6-137">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="6cea6-137">System.Guid</span></span>

### <span data-ttu-id="6cea6-138">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup</span><span class="sxs-lookup"><span data-stu-id="6cea6-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="6cea6-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6cea6-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6cea6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="6cea6-140">OUTPUTS</span></span>

### <span data-ttu-id="6cea6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="6cea6-141">System.Boolean</span></span>

## <span data-ttu-id="6cea6-142">筆記</span><span class="sxs-lookup"><span data-stu-id="6cea6-142">NOTES</span></span>

## <span data-ttu-id="6cea6-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cea6-143">RELATED LINKS</span></span>
