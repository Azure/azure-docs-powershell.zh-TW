---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 069705ffc119fae964e931164f97bfbae72eca35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795351"
---
# <span data-ttu-id="296ea-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="296ea-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="296ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="296ea-102">SYNOPSIS</span></span>
<span data-ttu-id="296ea-103">將使用者新增至現有的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="296ea-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="296ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="296ea-104">SYNTAX</span></span>

### <span data-ttu-id="296ea-105">MemberObjectIdWithGroupObjectId (預設) </span><span class="sxs-lookup"><span data-stu-id="296ea-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296ea-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="296ea-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296ea-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="296ea-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296ea-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="296ea-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296ea-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="296ea-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296ea-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="296ea-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="296ea-111">說明</span><span class="sxs-lookup"><span data-stu-id="296ea-111">DESCRIPTION</span></span>
<span data-ttu-id="296ea-112">將使用者新增至現有的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="296ea-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="296ea-113">示例</span><span class="sxs-lookup"><span data-stu-id="296ea-113">EXAMPLES</span></span>

### <span data-ttu-id="296ea-114">範例 1-依物件識別碼將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="296ea-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="296ea-115">將物件 id 為 "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" 的使用者新增至物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的群組。</span><span class="sxs-lookup"><span data-stu-id="296ea-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="296ea-116">範例 2-依管道將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="296ea-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="296ea-117">取得物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的群組，並將其管道至 Add-AzADGroupMember Cmdlet，以將使用者新增至該群組。</span><span class="sxs-lookup"><span data-stu-id="296ea-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="296ea-118">參數</span><span class="sxs-lookup"><span data-stu-id="296ea-118">PARAMETERS</span></span>

### <span data-ttu-id="296ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="296ea-119">-DefaultProfile</span></span>
<span data-ttu-id="296ea-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="296ea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="296ea-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="296ea-121">-MemberObjectId</span></span>
<span data-ttu-id="296ea-122">成員的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="296ea-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="296ea-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="296ea-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="296ea-124">成員 (s 的 UPN) 新增至群組。</span><span class="sxs-lookup"><span data-stu-id="296ea-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="296ea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="296ea-125">-PassThru</span></span>
<span data-ttu-id="296ea-126">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="296ea-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="296ea-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="296ea-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="296ea-128">要新增 (s) 成員的群組顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="296ea-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="296ea-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="296ea-129">-TargetGroupObject</span></span>
<span data-ttu-id="296ea-130">要新增 (s) 成員的群組物件表示。</span><span class="sxs-lookup"><span data-stu-id="296ea-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="296ea-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="296ea-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="296ea-132">要新增 (s) 成員之群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="296ea-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="296ea-133">-確認</span><span class="sxs-lookup"><span data-stu-id="296ea-133">-Confirm</span></span>
<span data-ttu-id="296ea-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="296ea-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="296ea-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="296ea-135">-WhatIf</span></span>
<span data-ttu-id="296ea-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="296ea-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="296ea-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="296ea-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="296ea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="296ea-138">CommonParameters</span></span>
<span data-ttu-id="296ea-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="296ea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="296ea-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="296ea-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="296ea-141">輸入</span><span class="sxs-lookup"><span data-stu-id="296ea-141">INPUTS</span></span>

### <span data-ttu-id="296ea-142">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup</span><span class="sxs-lookup"><span data-stu-id="296ea-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="296ea-143">參數： TargetGroupObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="296ea-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="296ea-144">輸出</span><span class="sxs-lookup"><span data-stu-id="296ea-144">OUTPUTS</span></span>

### <span data-ttu-id="296ea-145">System.object</span><span class="sxs-lookup"><span data-stu-id="296ea-145">System.Boolean</span></span>

## <span data-ttu-id="296ea-146">筆記</span><span class="sxs-lookup"><span data-stu-id="296ea-146">NOTES</span></span>

## <span data-ttu-id="296ea-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="296ea-147">RELATED LINKS</span></span>
