---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 98d5433ca2a8d557c7ca1924b9edb6e4fdca2b2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906505"
---
# <span data-ttu-id="ead80-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ead80-101">Remove-AzADUser</span></span>

## <span data-ttu-id="ead80-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ead80-102">SYNOPSIS</span></span>
<span data-ttu-id="ead80-103">刪除 Active Directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="ead80-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="ead80-104">語法</span><span class="sxs-lookup"><span data-stu-id="ead80-104">SYNTAX</span></span>

### <span data-ttu-id="ead80-105">UPNOrObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ead80-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead80-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead80-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead80-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead80-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead80-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead80-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead80-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead80-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead80-110">描述</span><span class="sxs-lookup"><span data-stu-id="ead80-110">DESCRIPTION</span></span>
<span data-ttu-id="ead80-111">刪除公司/ (帳戶的活動目錄使用者，也稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="ead80-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="ead80-112">例子</span><span class="sxs-lookup"><span data-stu-id="ead80-112">EXAMPLES</span></span>

### <span data-ttu-id="ead80-113">範例 1：根據使用者主體名稱移除使用者</span><span class="sxs-lookup"><span data-stu-id="ead80-113">Example 1: Remove a user by user principal name</span></span>

```powershell
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="ead80-114">從租使用者移除具有使用者主體名稱 foo@domain.com "" 的使用者。</span><span class="sxs-lookup"><span data-stu-id="ead80-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="ead80-115">範例 2：根據物件識別碼移除使用者</span><span class="sxs-lookup"><span data-stu-id="ead80-115">Example 2: Remove a user by object id</span></span>

```powershell
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="ead80-116">從租使用者移除物件識別碼為 '7a9582cf-88c4-4319-842b-7a5d60967a69'的使用者。</span><span class="sxs-lookup"><span data-stu-id="ead80-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="ead80-117">範例 3：使用管道移除使用者</span><span class="sxs-lookup"><span data-stu-id="ead80-117">Example 3: Remove a user by piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="ead80-118">將使用者物件識別碼 '7a9582cf-88c4-4319-842b-7a5d60967a69' 和管道移至 Remove-AzADUser Cmdlet，將使用者從租使用者移除。</span><span class="sxs-lookup"><span data-stu-id="ead80-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="ead80-119">參數</span><span class="sxs-lookup"><span data-stu-id="ead80-119">PARAMETERS</span></span>

### <span data-ttu-id="ead80-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead80-120">-DefaultProfile</span></span>
<span data-ttu-id="ead80-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ead80-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ead80-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ead80-122">-DisplayName</span></span>
<span data-ttu-id="ead80-123">要刪除之使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ead80-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="ead80-124">-強制</span><span class="sxs-lookup"><span data-stu-id="ead80-124">-Force</span></span>
<span data-ttu-id="ead80-125">如果指定，不會要求刪除使用者的確認。</span><span class="sxs-lookup"><span data-stu-id="ead80-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="ead80-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ead80-126">-InputObject</span></span>
<span data-ttu-id="ead80-127">要刪除的使用者物件。</span><span class="sxs-lookup"><span data-stu-id="ead80-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead80-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ead80-128">-ObjectId</span></span>
<span data-ttu-id="ead80-129">要刪除之使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead80-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="ead80-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ead80-130">-PassThru</span></span>
<span data-ttu-id="ead80-131">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="ead80-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ead80-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="ead80-132">-UPNOrObjectId</span></span>
<span data-ttu-id="ead80-133">要刪除的使用者主體名稱或 objectId。</span><span class="sxs-lookup"><span data-stu-id="ead80-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="ead80-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ead80-134">-UserPrincipalName</span></span>
<span data-ttu-id="ead80-135">要刪除的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="ead80-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="ead80-136">-確認</span><span class="sxs-lookup"><span data-stu-id="ead80-136">-Confirm</span></span>
<span data-ttu-id="ead80-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ead80-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead80-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead80-138">-WhatIf</span></span>
<span data-ttu-id="ead80-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ead80-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead80-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ead80-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead80-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead80-141">CommonParameters</span></span>
<span data-ttu-id="ead80-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ead80-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead80-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ead80-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead80-144">輸入</span><span class="sxs-lookup"><span data-stu-id="ead80-144">INPUTS</span></span>

### <span data-ttu-id="ead80-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ead80-145">System.String</span></span>

### <span data-ttu-id="ead80-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="ead80-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ead80-147">輸出</span><span class="sxs-lookup"><span data-stu-id="ead80-147">OUTPUTS</span></span>

### <span data-ttu-id="ead80-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ead80-148">System.Boolean</span></span>

## <span data-ttu-id="ead80-149">筆記</span><span class="sxs-lookup"><span data-stu-id="ead80-149">NOTES</span></span>

## <span data-ttu-id="ead80-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="ead80-150">RELATED LINKS</span></span>

[<span data-ttu-id="ead80-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ead80-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="ead80-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ead80-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="ead80-153">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ead80-153">Update-AzADUser</span></span>](./Update-AzADUser.md)

