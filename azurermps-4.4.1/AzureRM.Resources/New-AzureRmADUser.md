---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: ec9c234a03180f20b1b0cf6a4f5004923f3eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456407"
---
# <span data-ttu-id="0b96e-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0b96e-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="0b96e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b96e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b96e-103">建立新的 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="0b96e-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b96e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b96e-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <String> [-ImmutableId <String>]
 [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b96e-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b96e-105">DESCRIPTION</span></span>
<span data-ttu-id="0b96e-106">建立新的 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="0b96e-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="0b96e-107">如需詳細資訊： https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="0b96e-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="0b96e-108">示例</span><span class="sxs-lookup"><span data-stu-id="0b96e-108">EXAMPLES</span></span>

### <span data-ttu-id="0b96e-109">範例1</span><span class="sxs-lookup"><span data-stu-id="0b96e-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0b96e-110">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="0b96e-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="0b96e-111">參數</span><span class="sxs-lookup"><span data-stu-id="0b96e-111">PARAMETERS</span></span>

### <span data-ttu-id="0b96e-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0b96e-112">-DisplayName</span></span>
<span data-ttu-id="0b96e-113">要顯示在使用者通訊錄中的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b96e-113">The name to display in the address book for the user.</span></span>
<span data-ttu-id="0b96e-114">範例「立民 Wu」。</span><span class="sxs-lookup"><span data-stu-id="0b96e-114">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="0b96e-115">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="0b96e-115">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="0b96e-116">如果使用者必須在下一次成功的登入 (true) 時變更密碼，則必須指定它。</span><span class="sxs-lookup"><span data-stu-id="0b96e-116">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="0b96e-117">預設行為是 (false) ，不會在下一次成功的登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="0b96e-117">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="0b96e-118">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="0b96e-118">-ImmutableId</span></span>
<span data-ttu-id="0b96e-119">只有在您針對使用者的使用者主要名稱 (upn) 屬性中使用聯盟網域時，才需要指定它。</span><span class="sxs-lookup"><span data-stu-id="0b96e-119">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="0b96e-120">-Password</span><span class="sxs-lookup"><span data-stu-id="0b96e-120">-Password</span></span>
<span data-ttu-id="0b96e-121">使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="0b96e-121">Password for the user.</span></span>
<span data-ttu-id="0b96e-122">它必須符合租使用者的密碼複雜性需求。</span><span class="sxs-lookup"><span data-stu-id="0b96e-122">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="0b96e-123">建議設定強式密碼。</span><span class="sxs-lookup"><span data-stu-id="0b96e-123">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="0b96e-124">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0b96e-124">-UserPrincipalName</span></span>
<span data-ttu-id="0b96e-125">使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="0b96e-125">The user principal name.</span></span>
<span data-ttu-id="0b96e-126">範例-" someuser@contoso.com "。</span><span class="sxs-lookup"><span data-stu-id="0b96e-126">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="0b96e-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0b96e-127">-Confirm</span></span>
<span data-ttu-id="0b96e-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b96e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b96e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b96e-129">-WhatIf</span></span>
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

### <span data-ttu-id="0b96e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b96e-130">-DefaultProfile</span></span>
<span data-ttu-id="0b96e-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b96e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b96e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b96e-132">CommonParameters</span></span>
<span data-ttu-id="0b96e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b96e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b96e-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b96e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b96e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0b96e-135">INPUTS</span></span>

## <span data-ttu-id="0b96e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0b96e-136">OUTPUTS</span></span>

### <span data-ttu-id="0b96e-137">Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser</span><span class="sxs-lookup"><span data-stu-id="0b96e-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="0b96e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0b96e-138">NOTES</span></span>

## <span data-ttu-id="0b96e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b96e-139">RELATED LINKS</span></span>

[<span data-ttu-id="0b96e-140">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0b96e-140">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="0b96e-141">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0b96e-141">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="0b96e-142">移除-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0b96e-142">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
