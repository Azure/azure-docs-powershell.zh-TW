---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: e16adfe6db006af0c1f49992d5aff39412d4d4d3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398201"
---
# <span data-ttu-id="e32e8-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e32e8-101">Remove-AzADUser</span></span>

## <span data-ttu-id="e32e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e32e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e32e8-103">刪除 Active Directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="e32e8-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="e32e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="e32e8-104">SYNTAX</span></span>

### <span data-ttu-id="e32e8-105">UPNOrObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e32e8-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e32e8-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e32e8-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e32e8-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e32e8-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e32e8-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e32e8-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e32e8-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e32e8-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e32e8-110">描述</span><span class="sxs-lookup"><span data-stu-id="e32e8-110">DESCRIPTION</span></span>
<span data-ttu-id="e32e8-111">刪除公司/ (帳戶的活動目錄使用者，也稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="e32e8-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="e32e8-112">例子</span><span class="sxs-lookup"><span data-stu-id="e32e8-112">EXAMPLES</span></span>

### <span data-ttu-id="e32e8-113">範例 1 - 根據使用者主體名稱移除使用者</span><span class="sxs-lookup"><span data-stu-id="e32e8-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="e32e8-114">從租使用者移除具有使用者主體名稱 foo@domain.com "" 的使用者。</span><span class="sxs-lookup"><span data-stu-id="e32e8-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="e32e8-115">範例 2 - 根據物件識別碼移除使用者</span><span class="sxs-lookup"><span data-stu-id="e32e8-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="e32e8-116">從租使用者移除物件識別碼為 '7a9582cf-88c4-4319-842b-7a5d60967a69'的使用者。</span><span class="sxs-lookup"><span data-stu-id="e32e8-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="e32e8-117">範例 3 - 使用管道移除使用者</span><span class="sxs-lookup"><span data-stu-id="e32e8-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="e32e8-118">讓使用者使用物件識別碼 '7a9582cf-88c4-4319-842b-7a5d60967a69'，以及將使用者從租使用者移除之 Remove-AzADUser Cmdlet 的管道。</span><span class="sxs-lookup"><span data-stu-id="e32e8-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="e32e8-119">參數</span><span class="sxs-lookup"><span data-stu-id="e32e8-119">PARAMETERS</span></span>

### <span data-ttu-id="e32e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32e8-120">-DefaultProfile</span></span>
<span data-ttu-id="e32e8-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e32e8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e32e8-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e32e8-122">-DisplayName</span></span>
<span data-ttu-id="e32e8-123">要刪除之使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e32e8-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32e8-124">-強制</span><span class="sxs-lookup"><span data-stu-id="e32e8-124">-Force</span></span>
<span data-ttu-id="e32e8-125">如果指定，不會要求刪除使用者的確認。</span><span class="sxs-lookup"><span data-stu-id="e32e8-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="e32e8-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e32e8-126">-InputObject</span></span>
<span data-ttu-id="e32e8-127">要刪除的使用者物件。</span><span class="sxs-lookup"><span data-stu-id="e32e8-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e32e8-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e32e8-128">-ObjectId</span></span>
<span data-ttu-id="e32e8-129">要刪除之使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e32e8-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="e32e8-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e32e8-130">-PassThru</span></span>
<span data-ttu-id="e32e8-131">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="e32e8-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e32e8-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="e32e8-132">-UPNOrObjectId</span></span>
<span data-ttu-id="e32e8-133">要刪除的使用者主體名稱或 objectId。</span><span class="sxs-lookup"><span data-stu-id="e32e8-133">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32e8-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e32e8-134">-UserPrincipalName</span></span>
<span data-ttu-id="e32e8-135">要刪除的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="e32e8-135">The user principal name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32e8-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e32e8-136">-Confirm</span></span>
<span data-ttu-id="e32e8-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e32e8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e32e8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e32e8-138">-WhatIf</span></span>
<span data-ttu-id="e32e8-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e32e8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e32e8-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e32e8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e32e8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32e8-141">CommonParameters</span></span>
<span data-ttu-id="e32e8-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e32e8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32e8-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e32e8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32e8-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e32e8-144">INPUTS</span></span>

### <span data-ttu-id="e32e8-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e32e8-145">System.String</span></span>

### <span data-ttu-id="e32e8-146">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e32e8-146">System.Guid</span></span>

### <span data-ttu-id="e32e8-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="e32e8-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="e32e8-148">參數：InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e32e8-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e32e8-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e32e8-149">OUTPUTS</span></span>

### <span data-ttu-id="e32e8-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e32e8-150">System.Boolean</span></span>

## <span data-ttu-id="e32e8-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e32e8-151">NOTES</span></span>

## <span data-ttu-id="e32e8-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e32e8-152">RELATED LINKS</span></span>

[<span data-ttu-id="e32e8-153">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e32e8-153">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="e32e8-154">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e32e8-154">Get-AzADUser</span></span>](./Get-AzADUser.md)


