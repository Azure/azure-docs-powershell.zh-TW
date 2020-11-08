---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7450588905deeb900efbffffa253f5c06ae63272
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137331"
---
# <span data-ttu-id="29fce-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="29fce-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="29fce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29fce-102">SYNOPSIS</span></span>
<span data-ttu-id="29fce-103">從 AD 群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="29fce-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="29fce-104">句法</span><span class="sxs-lookup"><span data-stu-id="29fce-104">SYNTAX</span></span>

### <span data-ttu-id="29fce-105">ExplicitParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="29fce-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29fce-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="29fce-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29fce-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="29fce-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29fce-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="29fce-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29fce-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="29fce-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29fce-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29fce-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29fce-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29fce-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29fce-112">說明</span><span class="sxs-lookup"><span data-stu-id="29fce-112">DESCRIPTION</span></span>
<span data-ttu-id="29fce-113">從 AD 群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="29fce-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="29fce-114">示例</span><span class="sxs-lookup"><span data-stu-id="29fce-114">EXAMPLES</span></span>

### <span data-ttu-id="29fce-115">範例1：依物件識別碼從群組移除使用者</span><span class="sxs-lookup"><span data-stu-id="29fce-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="29fce-116">從物件 id 為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 的群組中移除物件 id 為 ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405」的使用者。</span><span class="sxs-lookup"><span data-stu-id="29fce-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="29fce-117">範例2：依管道移除群組中的使用者</span><span class="sxs-lookup"><span data-stu-id="29fce-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="29fce-118">取得物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的群組，並將其管道至 Remove-AzADGroupMember Cmdlet，以將使用者移至該群組。</span><span class="sxs-lookup"><span data-stu-id="29fce-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="29fce-119">參數</span><span class="sxs-lookup"><span data-stu-id="29fce-119">PARAMETERS</span></span>

### <span data-ttu-id="29fce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fce-120">-DefaultProfile</span></span>
<span data-ttu-id="29fce-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29fce-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29fce-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="29fce-122">-GroupDisplayName</span></span>
<span data-ttu-id="29fce-123">要移除成員 (s) 的群組顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="29fce-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="29fce-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="29fce-124">-GroupObject</span></span>
<span data-ttu-id="29fce-125">要移除成員的群組的物件表示。</span><span class="sxs-lookup"><span data-stu-id="29fce-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="29fce-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="29fce-126">-GroupObjectId</span></span>
<span data-ttu-id="29fce-127">要從中移除成員之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="29fce-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="29fce-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="29fce-128">-MemberObjectId</span></span>
<span data-ttu-id="29fce-129">成員的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="29fce-129">The object id of the member.</span></span>

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

### <span data-ttu-id="29fce-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="29fce-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="29fce-131">要移除之成員的 UPN)  (s。</span><span class="sxs-lookup"><span data-stu-id="29fce-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="29fce-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29fce-132">-PassThru</span></span>
<span data-ttu-id="29fce-133">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="29fce-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="29fce-134">-確認</span><span class="sxs-lookup"><span data-stu-id="29fce-134">-Confirm</span></span>
<span data-ttu-id="29fce-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29fce-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29fce-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29fce-136">-WhatIf</span></span>
<span data-ttu-id="29fce-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29fce-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29fce-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29fce-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29fce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fce-139">CommonParameters</span></span>
<span data-ttu-id="29fce-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29fce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fce-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="29fce-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fce-142">輸入</span><span class="sxs-lookup"><span data-stu-id="29fce-142">INPUTS</span></span>

### <span data-ttu-id="29fce-143">PSADGroup （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="29fce-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="29fce-144">輸出</span><span class="sxs-lookup"><span data-stu-id="29fce-144">OUTPUTS</span></span>

### <span data-ttu-id="29fce-145">System.object</span><span class="sxs-lookup"><span data-stu-id="29fce-145">System.Boolean</span></span>

## <span data-ttu-id="29fce-146">筆記</span><span class="sxs-lookup"><span data-stu-id="29fce-146">NOTES</span></span>

## <span data-ttu-id="29fce-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="29fce-147">RELATED LINKS</span></span>