---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: cd8834dd329ab82e98316cb0d94b554eb3bb6c13
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399646"
---
# <span data-ttu-id="29677-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="29677-101">New-AzADUser</span></span>

## <span data-ttu-id="29677-102">簡介</span><span class="sxs-lookup"><span data-stu-id="29677-102">SYNOPSIS</span></span>
<span data-ttu-id="29677-103">建立新 Active Directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="29677-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="29677-104">語法</span><span class="sxs-lookup"><span data-stu-id="29677-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29677-105">描述</span><span class="sxs-lookup"><span data-stu-id="29677-105">DESCRIPTION</span></span>
<span data-ttu-id="29677-106">在公司/學校 (建立新 Active Directory 使用者，也稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="29677-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="29677-107">詳細資訊： https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="29677-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="29677-108">例子</span><span class="sxs-lookup"><span data-stu-id="29677-108">EXAMPLES</span></span>

### <span data-ttu-id="29677-109">範例 1 - 建立新 AD 使用者</span><span class="sxs-lookup"><span data-stu-id="29677-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="29677-110">在租使用者中建立名稱為 "MyDisplayName" 和使用者主體名稱 " 的新 AD myemail@domain.com 使用者。</span><span class="sxs-lookup"><span data-stu-id="29677-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="29677-111">參數</span><span class="sxs-lookup"><span data-stu-id="29677-111">PARAMETERS</span></span>

### <span data-ttu-id="29677-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29677-112">-DefaultProfile</span></span>
<span data-ttu-id="29677-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="29677-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29677-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="29677-114">-DisplayName</span></span>
<span data-ttu-id="29677-115">要顯示在使用者通訊錄中的名稱。</span><span class="sxs-lookup"><span data-stu-id="29677-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="29677-116">範例 'Alex Wu'。</span><span class="sxs-lookup"><span data-stu-id="29677-116">example 'Alex Wu'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29677-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="29677-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="29677-118">必須指定使用者必須在下次成功登入時變更密碼， (密碼) 。</span><span class="sxs-lookup"><span data-stu-id="29677-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="29677-119">預設行為 (錯誤) ，不會在下次成功登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="29677-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29677-120">-一些卷心型</span><span class="sxs-lookup"><span data-stu-id="29677-120">-ImmutableId</span></span>
<span data-ttu-id="29677-121">您必須針對使用者的使用者主體名稱使用聯盟網域，才能指定 (屬性) 。</span><span class="sxs-lookup"><span data-stu-id="29677-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29677-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="29677-122">-MailNickname</span></span>
<span data-ttu-id="29677-123">使用者的郵件別名。</span><span class="sxs-lookup"><span data-stu-id="29677-123">The mail alias for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29677-124">-密碼</span><span class="sxs-lookup"><span data-stu-id="29677-124">-Password</span></span>
<span data-ttu-id="29677-125">使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="29677-125">Password for the user.</span></span>
<span data-ttu-id="29677-126">它必須符合租使用者的密碼複雜度需求。</span><span class="sxs-lookup"><span data-stu-id="29677-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="29677-127">建議您設定強式密碼。</span><span class="sxs-lookup"><span data-stu-id="29677-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29677-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="29677-128">-UserPrincipalName</span></span>
<span data-ttu-id="29677-129">使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="29677-129">The user principal name.</span></span>
<span data-ttu-id="29677-130">Example-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="29677-130">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29677-131">-確認</span><span class="sxs-lookup"><span data-stu-id="29677-131">-Confirm</span></span>
<span data-ttu-id="29677-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="29677-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29677-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29677-133">-WhatIf</span></span>
<span data-ttu-id="29677-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29677-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29677-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29677-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29677-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29677-136">CommonParameters</span></span>
<span data-ttu-id="29677-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="29677-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29677-138">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="29677-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29677-139">輸入</span><span class="sxs-lookup"><span data-stu-id="29677-139">INPUTS</span></span>

### <span data-ttu-id="29677-140">System.String</span><span class="sxs-lookup"><span data-stu-id="29677-140">System.String</span></span>

### <span data-ttu-id="29677-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="29677-141">System.Security.SecureString</span></span>

### <span data-ttu-id="29677-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="29677-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="29677-143">輸出</span><span class="sxs-lookup"><span data-stu-id="29677-143">OUTPUTS</span></span>

### <span data-ttu-id="29677-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="29677-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="29677-145">筆記</span><span class="sxs-lookup"><span data-stu-id="29677-145">NOTES</span></span>

## <span data-ttu-id="29677-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="29677-146">RELATED LINKS</span></span>

[<span data-ttu-id="29677-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="29677-147">Get-AzADUser</span></span>](./Get-AzADUser.md)


[<span data-ttu-id="29677-148">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="29677-148">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
