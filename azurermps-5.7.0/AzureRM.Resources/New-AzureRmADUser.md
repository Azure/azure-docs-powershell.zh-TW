---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 80a35ac1a1087d9e74cb47c3297af3ded491e701
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448566"
---
# <span data-ttu-id="99947-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="99947-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="99947-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99947-102">SYNOPSIS</span></span>
<span data-ttu-id="99947-103">建立新的 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="99947-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99947-104">句法</span><span class="sxs-lookup"><span data-stu-id="99947-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99947-105">說明</span><span class="sxs-lookup"><span data-stu-id="99947-105">DESCRIPTION</span></span>
<span data-ttu-id="99947-106">建立新的 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="99947-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="99947-107">如需詳細資訊： https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="99947-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="99947-108">示例</span><span class="sxs-lookup"><span data-stu-id="99947-108">EXAMPLES</span></span>

### <span data-ttu-id="99947-109">範例1</span><span class="sxs-lookup"><span data-stu-id="99947-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="99947-110">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="99947-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="99947-111">參數</span><span class="sxs-lookup"><span data-stu-id="99947-111">PARAMETERS</span></span>

### <span data-ttu-id="99947-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99947-112">-DefaultProfile</span></span>
<span data-ttu-id="99947-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="99947-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99947-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="99947-114">-DisplayName</span></span>
<span data-ttu-id="99947-115">要顯示在使用者通訊錄中的名稱。</span><span class="sxs-lookup"><span data-stu-id="99947-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="99947-116">範例「立民 Wu」。</span><span class="sxs-lookup"><span data-stu-id="99947-116">example 'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99947-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="99947-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="99947-118">如果使用者必須在下一次成功的登入 (true) 時變更密碼，則必須指定它。</span><span class="sxs-lookup"><span data-stu-id="99947-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="99947-119">預設行為是 (false) ，不會在下一次成功的登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="99947-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99947-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="99947-120">-ImmutableId</span></span>
<span data-ttu-id="99947-121">只有在您針對使用者的使用者主要名稱 (upn) 屬性中使用聯盟網域時，才需要指定它。</span><span class="sxs-lookup"><span data-stu-id="99947-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99947-122">-Password</span><span class="sxs-lookup"><span data-stu-id="99947-122">-Password</span></span>
<span data-ttu-id="99947-123">使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="99947-123">Password for the user.</span></span>
<span data-ttu-id="99947-124">它必須符合租使用者的密碼複雜性需求。</span><span class="sxs-lookup"><span data-stu-id="99947-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="99947-125">建議設定強式密碼。</span><span class="sxs-lookup"><span data-stu-id="99947-125">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99947-126">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="99947-126">-UserPrincipalName</span></span>
<span data-ttu-id="99947-127">使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="99947-127">The user principal name.</span></span>
<span data-ttu-id="99947-128">範例-" someuser@contoso.com "。</span><span class="sxs-lookup"><span data-stu-id="99947-128">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99947-129">-確認</span><span class="sxs-lookup"><span data-stu-id="99947-129">-Confirm</span></span>
<span data-ttu-id="99947-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99947-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99947-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99947-131">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99947-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99947-132">CommonParameters</span></span>
<span data-ttu-id="99947-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99947-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99947-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99947-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99947-135">輸入</span><span class="sxs-lookup"><span data-stu-id="99947-135">INPUTS</span></span>

### <span data-ttu-id="99947-136">所有</span><span class="sxs-lookup"><span data-stu-id="99947-136">None</span></span>
<span data-ttu-id="99947-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="99947-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99947-138">輸出</span><span class="sxs-lookup"><span data-stu-id="99947-138">OUTPUTS</span></span>

### <span data-ttu-id="99947-139">Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser</span><span class="sxs-lookup"><span data-stu-id="99947-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="99947-140">筆記</span><span class="sxs-lookup"><span data-stu-id="99947-140">NOTES</span></span>

## <span data-ttu-id="99947-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="99947-141">RELATED LINKS</span></span>

[<span data-ttu-id="99947-142">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="99947-142">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="99947-143">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="99947-143">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="99947-144">移除-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="99947-144">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
