---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 39413c8279b84bb75d3e86bbf41ff40afe05ad06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132210"
---
# <span data-ttu-id="a5b31-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a5b31-101">Remove-AzADUser</span></span>

## <span data-ttu-id="a5b31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5b31-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b31-103">刪除 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="a5b31-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="a5b31-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5b31-104">SYNTAX</span></span>

### <span data-ttu-id="a5b31-105">UPNOrObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a5b31-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b31-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b31-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b31-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b31-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b31-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b31-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b31-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b31-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b31-110">說明</span><span class="sxs-lookup"><span data-stu-id="a5b31-110">DESCRIPTION</span></span>
<span data-ttu-id="a5b31-111">刪除 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="a5b31-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="a5b31-112">示例</span><span class="sxs-lookup"><span data-stu-id="a5b31-112">EXAMPLES</span></span>

### <span data-ttu-id="a5b31-113">範例1：依使用者主要名稱移除使用者</span><span class="sxs-lookup"><span data-stu-id="a5b31-113">Example 1: Remove a user by user principal name</span></span>

```powershell
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="a5b31-114">從租使用者中移除使用者主要名稱為 "" 的使用者 foo@domain.com 。</span><span class="sxs-lookup"><span data-stu-id="a5b31-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="a5b31-115">範例2：依物件識別碼移除使用者</span><span class="sxs-lookup"><span data-stu-id="a5b31-115">Example 2: Remove a user by object id</span></span>

```powershell
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="a5b31-116">從租使用者移除物件 id 為 ' 7a9582cf-88c4-4319-842b-7a5d60967a69」的使用者。</span><span class="sxs-lookup"><span data-stu-id="a5b31-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="a5b31-117">範例3：依管道移除使用者</span><span class="sxs-lookup"><span data-stu-id="a5b31-117">Example 3: Remove a user by piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="a5b31-118">取得物件識別碼為 ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' 的使用者，以及 Remove-AzADUser Cmdlet 的管道，以從租使用者中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="a5b31-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="a5b31-119">參數</span><span class="sxs-lookup"><span data-stu-id="a5b31-119">PARAMETERS</span></span>

### <span data-ttu-id="a5b31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b31-120">-DefaultProfile</span></span>
<span data-ttu-id="a5b31-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a5b31-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5b31-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a5b31-122">-DisplayName</span></span>
<span data-ttu-id="a5b31-123">要刪除之使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a5b31-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="a5b31-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a5b31-124">-Force</span></span>
<span data-ttu-id="a5b31-125">如果已指定，就不要求確認刪除使用者。</span><span class="sxs-lookup"><span data-stu-id="a5b31-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="a5b31-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5b31-126">-InputObject</span></span>
<span data-ttu-id="a5b31-127">要刪除的使用者物件。</span><span class="sxs-lookup"><span data-stu-id="a5b31-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="a5b31-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a5b31-128">-ObjectId</span></span>
<span data-ttu-id="a5b31-129">要刪除之使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5b31-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="a5b31-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5b31-130">-PassThru</span></span>
<span data-ttu-id="a5b31-131">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a5b31-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a5b31-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="a5b31-132">-UPNOrObjectId</span></span>
<span data-ttu-id="a5b31-133">要刪除之使用者的使用者主要名稱或 objectId。</span><span class="sxs-lookup"><span data-stu-id="a5b31-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="a5b31-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a5b31-134">-UserPrincipalName</span></span>
<span data-ttu-id="a5b31-135">要刪除之使用者的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="a5b31-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="a5b31-136">-確認</span><span class="sxs-lookup"><span data-stu-id="a5b31-136">-Confirm</span></span>
<span data-ttu-id="a5b31-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5b31-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b31-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b31-138">-WhatIf</span></span>
<span data-ttu-id="a5b31-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5b31-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b31-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5b31-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b31-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b31-141">CommonParameters</span></span>
<span data-ttu-id="a5b31-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5b31-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b31-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5b31-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b31-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a5b31-144">INPUTS</span></span>

### <span data-ttu-id="a5b31-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a5b31-145">System.String</span></span>

### <span data-ttu-id="a5b31-146">PSADUser （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a5b31-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a5b31-147">輸出</span><span class="sxs-lookup"><span data-stu-id="a5b31-147">OUTPUTS</span></span>

### <span data-ttu-id="a5b31-148">System.object</span><span class="sxs-lookup"><span data-stu-id="a5b31-148">System.Boolean</span></span>

## <span data-ttu-id="a5b31-149">筆記</span><span class="sxs-lookup"><span data-stu-id="a5b31-149">NOTES</span></span>

## <span data-ttu-id="a5b31-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5b31-150">RELATED LINKS</span></span>

[<span data-ttu-id="a5b31-151">新-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a5b31-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="a5b31-152">AzADUser</span><span class="sxs-lookup"><span data-stu-id="a5b31-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="a5b31-153">更新-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a5b31-153">Update-AzADUser</span></span>](./Update-AzADUser.md)

