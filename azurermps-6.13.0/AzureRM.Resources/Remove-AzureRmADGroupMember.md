---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
ms.openlocfilehash: 515591660abf34399caa5643c05478fd4295141a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623898"
---
# <span data-ttu-id="5edba-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="5edba-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="5edba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5edba-102">SYNOPSIS</span></span>
<span data-ttu-id="5edba-103">從 AD 群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="5edba-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5edba-104">句法</span><span class="sxs-lookup"><span data-stu-id="5edba-104">SYNTAX</span></span>

### <span data-ttu-id="5edba-105">ExplicitParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5edba-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edba-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="5edba-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5edba-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="5edba-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5edba-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="5edba-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5edba-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edba-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5edba-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edba-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5edba-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edba-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5edba-112">說明</span><span class="sxs-lookup"><span data-stu-id="5edba-112">DESCRIPTION</span></span>
<span data-ttu-id="5edba-113">從 AD 群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="5edba-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="5edba-114">示例</span><span class="sxs-lookup"><span data-stu-id="5edba-114">EXAMPLES</span></span>

### <span data-ttu-id="5edba-115">範例 1-依物件識別碼從群組移除使用者</span><span class="sxs-lookup"><span data-stu-id="5edba-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="5edba-116">從物件 id 為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 的群組中移除物件 id 為 ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405」的使用者。</span><span class="sxs-lookup"><span data-stu-id="5edba-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5edba-117">範例 2-依管道移除群組中的使用者</span><span class="sxs-lookup"><span data-stu-id="5edba-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="5edba-118">取得物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的群組，並將其管道至 Remove-AzureRmADGroupMember Cmdlet，以將使用者移至該群組。</span><span class="sxs-lookup"><span data-stu-id="5edba-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="5edba-119">參數</span><span class="sxs-lookup"><span data-stu-id="5edba-119">PARAMETERS</span></span>

### <span data-ttu-id="5edba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edba-120">-DefaultProfile</span></span>
<span data-ttu-id="5edba-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5edba-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5edba-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="5edba-122">-GroupDisplayName</span></span>
<span data-ttu-id="5edba-123">要移除成員 (s) 的群組顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5edba-123">The display name of the group to remove the member(s) from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edba-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="5edba-124">-GroupObject</span></span>
<span data-ttu-id="5edba-125">要移除成員的群組的物件表示。</span><span class="sxs-lookup"><span data-stu-id="5edba-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5edba-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="5edba-126">-GroupObjectId</span></span>
<span data-ttu-id="5edba-127">要從中移除成員之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5edba-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edba-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="5edba-128">-MemberObjectId</span></span>
<span data-ttu-id="5edba-129">成員的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5edba-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edba-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5edba-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="5edba-131">要移除之成員的 UPN)  (s。</span><span class="sxs-lookup"><span data-stu-id="5edba-131">The UPN of the member(s) to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edba-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5edba-132">-PassThru</span></span>
<span data-ttu-id="5edba-133">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="5edba-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5edba-134">-確認</span><span class="sxs-lookup"><span data-stu-id="5edba-134">-Confirm</span></span>
<span data-ttu-id="5edba-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5edba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5edba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5edba-136">-WhatIf</span></span>
<span data-ttu-id="5edba-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5edba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5edba-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5edba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5edba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edba-139">CommonParameters</span></span>
<span data-ttu-id="5edba-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5edba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edba-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5edba-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edba-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5edba-142">INPUTS</span></span>

### <span data-ttu-id="5edba-143">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5edba-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="5edba-144">參數： GroupObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5edba-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="5edba-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5edba-145">OUTPUTS</span></span>

### <span data-ttu-id="5edba-146">System.object</span><span class="sxs-lookup"><span data-stu-id="5edba-146">System.Boolean</span></span>

## <span data-ttu-id="5edba-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5edba-147">NOTES</span></span>

## <span data-ttu-id="5edba-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="5edba-148">RELATED LINKS</span></span>
