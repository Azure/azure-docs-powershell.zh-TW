---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 5424c2b6332455c0b0cfa04526295d9e51f46fdc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956341"
---
# <span data-ttu-id="1c98b-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="1c98b-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="1c98b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c98b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c98b-103">將使用者新增至現有的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="1c98b-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="1c98b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c98b-104">SYNTAX</span></span>

### <span data-ttu-id="1c98b-105">MemberObjectIdWithGroupObjectId (預設) </span><span class="sxs-lookup"><span data-stu-id="1c98b-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c98b-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="1c98b-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c98b-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="1c98b-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c98b-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c98b-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c98b-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c98b-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c98b-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c98b-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c98b-111">說明</span><span class="sxs-lookup"><span data-stu-id="1c98b-111">DESCRIPTION</span></span>
<span data-ttu-id="1c98b-112">將使用者新增至現有的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="1c98b-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="1c98b-113">示例</span><span class="sxs-lookup"><span data-stu-id="1c98b-113">EXAMPLES</span></span>

### <span data-ttu-id="1c98b-114">範例 1-依物件識別碼將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="1c98b-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="1c98b-115">將物件 id 為 "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" 的使用者新增至物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的群組。</span><span class="sxs-lookup"><span data-stu-id="1c98b-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="1c98b-116">範例 2-依管道將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="1c98b-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="1c98b-117">取得物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的群組，並將其管道至 Add-AzADGroupMember Cmdlet，以將使用者新增至該群組。</span><span class="sxs-lookup"><span data-stu-id="1c98b-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="1c98b-118">範例 3-依主要名稱將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="1c98b-118">Example 3 - Add a user to a group by principal name</span></span>

```
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="1c98b-119">將使用者新增至群組，並列出群組的成員。</span><span class="sxs-lookup"><span data-stu-id="1c98b-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="1c98b-120">參數</span><span class="sxs-lookup"><span data-stu-id="1c98b-120">PARAMETERS</span></span>

### <span data-ttu-id="1c98b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c98b-121">-DefaultProfile</span></span>
<span data-ttu-id="1c98b-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c98b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c98b-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="1c98b-123">-MemberObjectId</span></span>
<span data-ttu-id="1c98b-124">成員的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c98b-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c98b-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1c98b-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="1c98b-126">成員 (s 的 UPN) 新增至群組。</span><span class="sxs-lookup"><span data-stu-id="1c98b-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="1c98b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c98b-127">-PassThru</span></span>
<span data-ttu-id="1c98b-128">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="1c98b-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1c98b-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="1c98b-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="1c98b-130">要新增 (s) 成員的群組顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1c98b-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="1c98b-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="1c98b-131">-TargetGroupObject</span></span>
<span data-ttu-id="1c98b-132">要新增 (s) 成員的群組物件表示。</span><span class="sxs-lookup"><span data-stu-id="1c98b-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="1c98b-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="1c98b-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="1c98b-134">要新增 (s) 成員之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c98b-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="1c98b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="1c98b-135">-Confirm</span></span>
<span data-ttu-id="1c98b-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1c98b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c98b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c98b-137">-WhatIf</span></span>
<span data-ttu-id="1c98b-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c98b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c98b-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c98b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c98b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c98b-140">CommonParameters</span></span>
<span data-ttu-id="1c98b-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c98b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c98b-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1c98b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c98b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="1c98b-143">INPUTS</span></span>

### <span data-ttu-id="1c98b-144">PSADGroup （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="1c98b-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="1c98b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="1c98b-145">OUTPUTS</span></span>

### <span data-ttu-id="1c98b-146">System.object</span><span class="sxs-lookup"><span data-stu-id="1c98b-146">System.Boolean</span></span>

## <span data-ttu-id="1c98b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="1c98b-147">NOTES</span></span>

## <span data-ttu-id="1c98b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c98b-148">RELATED LINKS</span></span>
