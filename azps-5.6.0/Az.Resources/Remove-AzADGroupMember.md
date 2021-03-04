---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7cc64ad6d0f17666ac1e97ae00473907c53a5552
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902838"
---
# <span data-ttu-id="c1488-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="c1488-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="c1488-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1488-102">SYNOPSIS</span></span>
<span data-ttu-id="c1488-103">從 AD 群組移除使用者。</span><span class="sxs-lookup"><span data-stu-id="c1488-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="c1488-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1488-104">SYNTAX</span></span>

### <span data-ttu-id="c1488-105">ExplicitParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c1488-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1488-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="c1488-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1488-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="c1488-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1488-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="c1488-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1488-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1488-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1488-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1488-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1488-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1488-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1488-112">描述</span><span class="sxs-lookup"><span data-stu-id="c1488-112">DESCRIPTION</span></span>
<span data-ttu-id="c1488-113">從 AD 群組移除使用者。</span><span class="sxs-lookup"><span data-stu-id="c1488-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="c1488-114">例子</span><span class="sxs-lookup"><span data-stu-id="c1488-114">EXAMPLES</span></span>

### <span data-ttu-id="c1488-115">範例 1：根據物件識別碼將使用者從群組移除</span><span class="sxs-lookup"><span data-stu-id="c1488-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c1488-116">將物件識別碼為 "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" 的使用者從物件識別碼為 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'的群組移除。</span><span class="sxs-lookup"><span data-stu-id="c1488-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="c1488-117">範例 2：使用管道將使用者從群組移除</span><span class="sxs-lookup"><span data-stu-id="c1488-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="c1488-118">使用物件識別碼為 '85F89C90-780E-4AA6-9F4F-6F268D322EEE' 的群組，並管道到 Remove-AzADGroupMember Cmdlet，將使用者移除至該群組。</span><span class="sxs-lookup"><span data-stu-id="c1488-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="c1488-119">參數</span><span class="sxs-lookup"><span data-stu-id="c1488-119">PARAMETERS</span></span>

### <span data-ttu-id="c1488-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1488-120">-DefaultProfile</span></span>
<span data-ttu-id="c1488-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1488-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1488-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="c1488-122">-GroupDisplayName</span></span>
<span data-ttu-id="c1488-123">移除其成員之 (的) 名稱。</span><span class="sxs-lookup"><span data-stu-id="c1488-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="c1488-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="c1488-124">-GroupObject</span></span>
<span data-ttu-id="c1488-125">要移除成員之群組的物件標記法。</span><span class="sxs-lookup"><span data-stu-id="c1488-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1488-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="c1488-126">-GroupObjectId</span></span>
<span data-ttu-id="c1488-127">要從移除成員之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1488-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1488-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="c1488-128">-MemberObjectId</span></span>
<span data-ttu-id="c1488-129">成員的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1488-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1488-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c1488-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="c1488-131">要移除之成員 (UPN) 移除。</span><span class="sxs-lookup"><span data-stu-id="c1488-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="c1488-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1488-132">-PassThru</span></span>
<span data-ttu-id="c1488-133">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="c1488-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c1488-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c1488-134">-Confirm</span></span>
<span data-ttu-id="c1488-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c1488-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1488-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1488-136">-WhatIf</span></span>
<span data-ttu-id="c1488-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1488-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1488-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1488-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1488-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1488-139">CommonParameters</span></span>
<span data-ttu-id="c1488-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1488-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1488-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1488-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1488-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c1488-142">INPUTS</span></span>

### <span data-ttu-id="c1488-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c1488-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c1488-144">輸出</span><span class="sxs-lookup"><span data-stu-id="c1488-144">OUTPUTS</span></span>

### <span data-ttu-id="c1488-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1488-145">System.Boolean</span></span>

## <span data-ttu-id="c1488-146">筆記</span><span class="sxs-lookup"><span data-stu-id="c1488-146">NOTES</span></span>

## <span data-ttu-id="c1488-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1488-147">RELATED LINKS</span></span>
