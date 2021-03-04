---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 7184ee532335d7db84792bf2234d8cbafa9ad201
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914413"
---
# <span data-ttu-id="de94b-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="de94b-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="de94b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de94b-102">SYNOPSIS</span></span>
<span data-ttu-id="de94b-103">將使用者新增到現有的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="de94b-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="de94b-104">語法</span><span class="sxs-lookup"><span data-stu-id="de94b-104">SYNTAX</span></span>

### <span data-ttu-id="de94b-105">MemberObjectIdWithGroupObjectId (預設) </span><span class="sxs-lookup"><span data-stu-id="de94b-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de94b-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="de94b-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de94b-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="de94b-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de94b-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="de94b-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de94b-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de94b-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de94b-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de94b-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de94b-111">描述</span><span class="sxs-lookup"><span data-stu-id="de94b-111">DESCRIPTION</span></span>
<span data-ttu-id="de94b-112">將使用者新增到現有的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="de94b-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="de94b-113">例子</span><span class="sxs-lookup"><span data-stu-id="de94b-113">EXAMPLES</span></span>

### <span data-ttu-id="de94b-114">範例 1：根據物件識別碼將使用者新增到群組</span><span class="sxs-lookup"><span data-stu-id="de94b-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="de94b-115">將具有物件識別碼 "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" 的使用者新增到物件識別碼為 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'的群組。</span><span class="sxs-lookup"><span data-stu-id="de94b-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="de94b-116">範例 2：使用管道將使用者新增到群組</span><span class="sxs-lookup"><span data-stu-id="de94b-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="de94b-117">使用物件識別碼為 '85F89C90-780E-4AA6-9F4F-6F268D322EEE' 的群組，並管道到 Add-AzADGroupMember Cmdlet，將使用者新增到該群組。</span><span class="sxs-lookup"><span data-stu-id="de94b-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="de94b-118">範例 3：根據主體名稱將使用者新增到群組</span><span class="sxs-lookup"><span data-stu-id="de94b-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="de94b-119">將使用者新增到群組，並列出群組的成員。</span><span class="sxs-lookup"><span data-stu-id="de94b-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="de94b-120">參數</span><span class="sxs-lookup"><span data-stu-id="de94b-120">PARAMETERS</span></span>

### <span data-ttu-id="de94b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de94b-121">-DefaultProfile</span></span>
<span data-ttu-id="de94b-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="de94b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de94b-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="de94b-123">-MemberObjectId</span></span>
<span data-ttu-id="de94b-124">成員的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="de94b-124">The object id of the member.</span></span>

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

### <span data-ttu-id="de94b-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="de94b-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="de94b-126">要新 (群組) 成員 UPN。</span><span class="sxs-lookup"><span data-stu-id="de94b-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="de94b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de94b-127">-PassThru</span></span>
<span data-ttu-id="de94b-128">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="de94b-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="de94b-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="de94b-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="de94b-130">要新增其成員 (群組) 名稱。</span><span class="sxs-lookup"><span data-stu-id="de94b-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="de94b-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="de94b-131">-TargetGroupObject</span></span>
<span data-ttu-id="de94b-132">要新增成員 (群組) 表示。</span><span class="sxs-lookup"><span data-stu-id="de94b-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="de94b-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="de94b-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="de94b-134">要新增成員 (群組) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="de94b-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="de94b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="de94b-135">-Confirm</span></span>
<span data-ttu-id="de94b-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="de94b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de94b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de94b-137">-WhatIf</span></span>
<span data-ttu-id="de94b-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de94b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de94b-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de94b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de94b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de94b-140">CommonParameters</span></span>
<span data-ttu-id="de94b-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de94b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de94b-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de94b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de94b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="de94b-143">INPUTS</span></span>

### <span data-ttu-id="de94b-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="de94b-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="de94b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="de94b-145">OUTPUTS</span></span>

### <span data-ttu-id="de94b-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de94b-146">System.Boolean</span></span>

## <span data-ttu-id="de94b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="de94b-147">NOTES</span></span>

## <span data-ttu-id="de94b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="de94b-148">RELATED LINKS</span></span>
