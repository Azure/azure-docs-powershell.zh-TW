---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 3875b697b801760b2db78ecfa55f3cbfc734b250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906501"
---
# <span data-ttu-id="746f1-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="746f1-101">Update-AzADUser</span></span>

## <span data-ttu-id="746f1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="746f1-102">SYNOPSIS</span></span>
<span data-ttu-id="746f1-103">更新現有的 Active Directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="746f1-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="746f1-104">語法</span><span class="sxs-lookup"><span data-stu-id="746f1-104">SYNTAX</span></span>

### <span data-ttu-id="746f1-105">UPNOrObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="746f1-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746f1-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="746f1-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746f1-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="746f1-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746f1-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="746f1-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="746f1-109">描述</span><span class="sxs-lookup"><span data-stu-id="746f1-109">DESCRIPTION</span></span>
<span data-ttu-id="746f1-110">更新公司/ (帳戶的現有 Active Directory 使用者，也稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="746f1-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="746f1-111">詳細資訊： https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="746f1-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="746f1-112">例子</span><span class="sxs-lookup"><span data-stu-id="746f1-112">EXAMPLES</span></span>

### <span data-ttu-id="746f1-113">範例 1：使用物件識別碼更新使用者的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="746f1-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="746f1-114">將使用者顯示名稱與物件識別碼 '155a5c10-93a9-4941-a0df-96d83ab5ab24' 更新為 'MyNewDisplayName'。</span><span class="sxs-lookup"><span data-stu-id="746f1-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="746f1-115">範例 2：使用使用者主體名稱更新使用者的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="746f1-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="746f1-116">將使用者主體名稱 '' 的顯示名稱 foo@domain.com 更新為 'MyNewDisplayName'。</span><span class="sxs-lookup"><span data-stu-id="746f1-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="746f1-117">範例 3：使用管線更新使用者的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="746f1-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="746f1-118">讓使用者使用物件識別碼 '155a5c10-93a9-4941-a0df-96d83ab5ab24'，以及管道到 Update-AzADUser Cmdlet，將該使用者的顯示名稱更新為 'MyNewDisplayName'。</span><span class="sxs-lookup"><span data-stu-id="746f1-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="746f1-119">參數</span><span class="sxs-lookup"><span data-stu-id="746f1-119">PARAMETERS</span></span>

### <span data-ttu-id="746f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746f1-120">-DefaultProfile</span></span>
<span data-ttu-id="746f1-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="746f1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="746f1-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="746f1-122">-DisplayName</span></span>
<span data-ttu-id="746f1-123">使用者的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="746f1-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746f1-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="746f1-124">-EnableAccount</span></span>
<span data-ttu-id="746f1-125">True 以啟用帳戶;否則，為 False。</span><span class="sxs-lookup"><span data-stu-id="746f1-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746f1-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="746f1-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="746f1-127">必須指定使用者是否應在下一次成功登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="746f1-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="746f1-128">只有在密碼更新時有效，否則系統將會忽略密碼。</span><span class="sxs-lookup"><span data-stu-id="746f1-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="746f1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="746f1-129">-InputObject</span></span>
<span data-ttu-id="746f1-130">代表要更新之使用者的物件。</span><span class="sxs-lookup"><span data-stu-id="746f1-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="746f1-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="746f1-131">-ObjectId</span></span>
<span data-ttu-id="746f1-132">要更新的使用者物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="746f1-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="746f1-133">-密碼</span><span class="sxs-lookup"><span data-stu-id="746f1-133">-Password</span></span>
<span data-ttu-id="746f1-134">使用者的新密碼。</span><span class="sxs-lookup"><span data-stu-id="746f1-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746f1-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="746f1-135">-UPNOrObjectId</span></span>
<span data-ttu-id="746f1-136">要更新的使用者主體名稱或物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="746f1-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="746f1-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="746f1-137">-UserPrincipalName</span></span>
<span data-ttu-id="746f1-138">要更新的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="746f1-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="746f1-139">-確認</span><span class="sxs-lookup"><span data-stu-id="746f1-139">-Confirm</span></span>
<span data-ttu-id="746f1-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="746f1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746f1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746f1-141">-WhatIf</span></span>
<span data-ttu-id="746f1-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="746f1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746f1-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="746f1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746f1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746f1-144">CommonParameters</span></span>
<span data-ttu-id="746f1-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="746f1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746f1-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="746f1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746f1-147">輸入</span><span class="sxs-lookup"><span data-stu-id="746f1-147">INPUTS</span></span>

### <span data-ttu-id="746f1-148">System.String</span><span class="sxs-lookup"><span data-stu-id="746f1-148">System.String</span></span>

### <span data-ttu-id="746f1-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="746f1-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="746f1-150">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="746f1-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="746f1-151">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="746f1-151">System.Security.SecureString</span></span>

## <span data-ttu-id="746f1-152">輸出</span><span class="sxs-lookup"><span data-stu-id="746f1-152">OUTPUTS</span></span>

### <span data-ttu-id="746f1-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="746f1-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="746f1-154">筆記</span><span class="sxs-lookup"><span data-stu-id="746f1-154">NOTES</span></span>

## <span data-ttu-id="746f1-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="746f1-155">RELATED LINKS</span></span>
