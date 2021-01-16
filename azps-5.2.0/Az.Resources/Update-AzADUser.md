---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273928"
---
# <span data-ttu-id="b4d28-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b4d28-101">Update-AzADUser</span></span>

## <span data-ttu-id="b4d28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4d28-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d28-103">更新現有的 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="b4d28-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="b4d28-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4d28-104">SYNTAX</span></span>

### <span data-ttu-id="b4d28-105">UPNOrObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b4d28-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d28-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d28-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d28-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d28-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d28-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d28-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4d28-109">說明</span><span class="sxs-lookup"><span data-stu-id="b4d28-109">DESCRIPTION</span></span>
<span data-ttu-id="b4d28-110">更新現有的 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="b4d28-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="b4d28-111">如需詳細資訊： https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="b4d28-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="b4d28-112">示例</span><span class="sxs-lookup"><span data-stu-id="b4d28-112">EXAMPLES</span></span>

### <span data-ttu-id="b4d28-113">範例1：使用物件識別碼更新使用者的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b4d28-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="b4d28-114">將物件 id 為 ' 155a5c10-93a9-4941-a0df-96d83ab5ab24 ' 的使用者的顯示名稱更新為「MyNewDisplayName」。</span><span class="sxs-lookup"><span data-stu-id="b4d28-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="b4d28-115">範例2：使用使用者主要名稱更新使用者的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b4d28-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="b4d28-116">將使用者主要名稱為 ' "的使用者顯示名稱更新 foo@domain.com 為 ' MyNewDisplayName」。</span><span class="sxs-lookup"><span data-stu-id="b4d28-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="b4d28-117">範例3：使用管道更新使用者的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b4d28-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="b4d28-118">取得物件識別碼為 ' 155a5c10-93a9-4941-a0df-96d83ab5ab24 ' 的使用者，以及 Update-AzADUser Cmdlet 的管道，以將該使用者的顯示名稱更新為「MyNewDisplayName」。</span><span class="sxs-lookup"><span data-stu-id="b4d28-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="b4d28-119">參數</span><span class="sxs-lookup"><span data-stu-id="b4d28-119">PARAMETERS</span></span>

### <span data-ttu-id="b4d28-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d28-120">-DefaultProfile</span></span>
<span data-ttu-id="b4d28-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4d28-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d28-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b4d28-122">-DisplayName</span></span>
<span data-ttu-id="b4d28-123">使用者的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b4d28-123">New display name for the user.</span></span>

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

### <span data-ttu-id="b4d28-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="b4d28-124">-EnableAccount</span></span>
<span data-ttu-id="b4d28-125">啟用帳戶的 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="b4d28-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="b4d28-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="b4d28-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="b4d28-127">如果使用者應該在下一次成功的登入時變更密碼，則必須指定它。</span><span class="sxs-lookup"><span data-stu-id="b4d28-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="b4d28-128">只有在更新密碼時才有效，否則將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b4d28-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="b4d28-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d28-129">-InputObject</span></span>
<span data-ttu-id="b4d28-130">代表要更新之使用者的物件。</span><span class="sxs-lookup"><span data-stu-id="b4d28-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="b4d28-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b4d28-131">-ObjectId</span></span>
<span data-ttu-id="b4d28-132">要更新之使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4d28-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="b4d28-133">-Password</span><span class="sxs-lookup"><span data-stu-id="b4d28-133">-Password</span></span>
<span data-ttu-id="b4d28-134">使用者的新密碼。</span><span class="sxs-lookup"><span data-stu-id="b4d28-134">New password for the user.</span></span>

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

### <span data-ttu-id="b4d28-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="b4d28-135">-UPNOrObjectId</span></span>
<span data-ttu-id="b4d28-136">要更新之使用者的使用者主要名稱或物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4d28-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="b4d28-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b4d28-137">-UserPrincipalName</span></span>
<span data-ttu-id="b4d28-138">要更新之使用者的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="b4d28-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="b4d28-139">-確認</span><span class="sxs-lookup"><span data-stu-id="b4d28-139">-Confirm</span></span>
<span data-ttu-id="b4d28-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b4d28-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d28-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d28-141">-WhatIf</span></span>
<span data-ttu-id="b4d28-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4d28-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4d28-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4d28-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d28-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d28-144">CommonParameters</span></span>
<span data-ttu-id="b4d28-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4d28-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d28-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b4d28-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d28-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b4d28-147">INPUTS</span></span>

### <span data-ttu-id="b4d28-148">System.object</span><span class="sxs-lookup"><span data-stu-id="b4d28-148">System.String</span></span>

### <span data-ttu-id="b4d28-149">PSADUser （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="b4d28-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="b4d28-150">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b4d28-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b4d28-151">SecureString</span><span class="sxs-lookup"><span data-stu-id="b4d28-151">System.Security.SecureString</span></span>

## <span data-ttu-id="b4d28-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b4d28-152">OUTPUTS</span></span>

### <span data-ttu-id="b4d28-153">PSADUser （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="b4d28-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="b4d28-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b4d28-154">NOTES</span></span>

## <span data-ttu-id="b4d28-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4d28-155">RELATED LINKS</span></span>
