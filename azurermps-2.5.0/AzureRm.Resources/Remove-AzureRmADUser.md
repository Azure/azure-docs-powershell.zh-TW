---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 51758c5b51c358a60be310405a89666cc56bac2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800037"
---
# <span data-ttu-id="41c29-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="41c29-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="41c29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41c29-102">SYNOPSIS</span></span>
<span data-ttu-id="41c29-103">刪除 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="41c29-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c29-104">句法</span><span class="sxs-lookup"><span data-stu-id="41c29-104">SYNTAX</span></span>

### <span data-ttu-id="41c29-105">UPNOrObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="41c29-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c29-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="41c29-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c29-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41c29-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c29-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="41c29-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c29-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41c29-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c29-110">說明</span><span class="sxs-lookup"><span data-stu-id="41c29-110">DESCRIPTION</span></span>
<span data-ttu-id="41c29-111">刪除 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="41c29-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="41c29-112">示例</span><span class="sxs-lookup"><span data-stu-id="41c29-112">EXAMPLES</span></span>

### <span data-ttu-id="41c29-113">範例 1-依使用者主要名稱移除使用者</span><span class="sxs-lookup"><span data-stu-id="41c29-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="41c29-114">從租使用者中移除使用者主要名稱為 "" 的使用者 foo@domain.com 。</span><span class="sxs-lookup"><span data-stu-id="41c29-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="41c29-115">範例 2-依物件識別碼移除使用者</span><span class="sxs-lookup"><span data-stu-id="41c29-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="41c29-116">從租使用者移除物件 id 為 ' 7a9582cf-88c4-4319-842b-7a5d60967a69」的使用者。</span><span class="sxs-lookup"><span data-stu-id="41c29-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="41c29-117">範例 3-依管道移除使用者</span><span class="sxs-lookup"><span data-stu-id="41c29-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="41c29-118">取得物件識別碼為 ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' 的使用者，以及 Remove-AzureRmADUser Cmdlet 的管道，以從租使用者中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="41c29-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="41c29-119">參數</span><span class="sxs-lookup"><span data-stu-id="41c29-119">PARAMETERS</span></span>

### <span data-ttu-id="41c29-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c29-120">-DefaultProfile</span></span>
<span data-ttu-id="41c29-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="41c29-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41c29-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="41c29-122">-DisplayName</span></span>
<span data-ttu-id="41c29-123">要刪除之使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="41c29-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="41c29-124">-Force</span><span class="sxs-lookup"><span data-stu-id="41c29-124">-Force</span></span>
<span data-ttu-id="41c29-125">如果已指定，就不要求確認刪除使用者。</span><span class="sxs-lookup"><span data-stu-id="41c29-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="41c29-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41c29-126">-InputObject</span></span>
<span data-ttu-id="41c29-127">要刪除的使用者物件。</span><span class="sxs-lookup"><span data-stu-id="41c29-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="41c29-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="41c29-128">-ObjectId</span></span>
<span data-ttu-id="41c29-129">要刪除之使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="41c29-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="41c29-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41c29-130">-PassThru</span></span>
<span data-ttu-id="41c29-131">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="41c29-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="41c29-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="41c29-132">-UPNOrObjectId</span></span>
<span data-ttu-id="41c29-133">要刪除之使用者的使用者主要名稱或 objectId。</span><span class="sxs-lookup"><span data-stu-id="41c29-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="41c29-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="41c29-134">-UserPrincipalName</span></span>
<span data-ttu-id="41c29-135">要刪除之使用者的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="41c29-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="41c29-136">-確認</span><span class="sxs-lookup"><span data-stu-id="41c29-136">-Confirm</span></span>
<span data-ttu-id="41c29-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41c29-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c29-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c29-138">-WhatIf</span></span>
<span data-ttu-id="41c29-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41c29-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c29-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41c29-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c29-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c29-141">CommonParameters</span></span>
<span data-ttu-id="41c29-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41c29-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c29-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41c29-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c29-144">輸入</span><span class="sxs-lookup"><span data-stu-id="41c29-144">INPUTS</span></span>

### <span data-ttu-id="41c29-145">System.object</span><span class="sxs-lookup"><span data-stu-id="41c29-145">System.String</span></span>

### <span data-ttu-id="41c29-146">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="41c29-146">System.Guid</span></span>

### <span data-ttu-id="41c29-147">Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser</span><span class="sxs-lookup"><span data-stu-id="41c29-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="41c29-148">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="41c29-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="41c29-149">輸出</span><span class="sxs-lookup"><span data-stu-id="41c29-149">OUTPUTS</span></span>

### <span data-ttu-id="41c29-150">System.object</span><span class="sxs-lookup"><span data-stu-id="41c29-150">System.Boolean</span></span>

## <span data-ttu-id="41c29-151">筆記</span><span class="sxs-lookup"><span data-stu-id="41c29-151">NOTES</span></span>

## <span data-ttu-id="41c29-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="41c29-152">RELATED LINKS</span></span>

[<span data-ttu-id="41c29-153">新-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="41c29-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="41c29-154">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="41c29-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)



