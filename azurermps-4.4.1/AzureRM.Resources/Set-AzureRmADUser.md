---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623641"
---
# <span data-ttu-id="02fb1-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="02fb1-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="02fb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="02fb1-103">更新現有的 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="02fb1-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02fb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="02fb1-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02fb1-105">說明</span><span class="sxs-lookup"><span data-stu-id="02fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="02fb1-106">更新現有的 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="02fb1-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="02fb1-107">如需詳細資訊： https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="02fb1-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="02fb1-108">示例</span><span class="sxs-lookup"><span data-stu-id="02fb1-108">EXAMPLES</span></span>

### <span data-ttu-id="02fb1-109">範例1</span><span class="sxs-lookup"><span data-stu-id="02fb1-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="02fb1-110">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="02fb1-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="02fb1-111">參數</span><span class="sxs-lookup"><span data-stu-id="02fb1-111">PARAMETERS</span></span>

### <span data-ttu-id="02fb1-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02fb1-112">-DisplayName</span></span>
<span data-ttu-id="02fb1-113">要顯示在使用者通訊錄中的新名稱。</span><span class="sxs-lookup"><span data-stu-id="02fb1-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="02fb1-114">範例-'Alex Wu」。</span><span class="sxs-lookup"><span data-stu-id="02fb1-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="02fb1-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="02fb1-115">-EnableAccount</span></span>
<span data-ttu-id="02fb1-116">啟用帳戶的 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="02fb1-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02fb1-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="02fb1-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="02fb1-118">只有在您更新密碼時，才能指定它。</span><span class="sxs-lookup"><span data-stu-id="02fb1-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="02fb1-119">否則將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="02fb1-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="02fb1-120">如果使用者必須在下一次成功的登入 (true) 時變更密碼，則必須指定它。</span><span class="sxs-lookup"><span data-stu-id="02fb1-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="02fb1-121">預設行為是 (false) ，不會在下一次成功的登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="02fb1-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="02fb1-122">-Password</span><span class="sxs-lookup"><span data-stu-id="02fb1-122">-Password</span></span>
<span data-ttu-id="02fb1-123">使用者的新密碼。</span><span class="sxs-lookup"><span data-stu-id="02fb1-123">New password for the user.</span></span>
<span data-ttu-id="02fb1-124">它必須符合租使用者的密碼複雜性需求。</span><span class="sxs-lookup"><span data-stu-id="02fb1-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="02fb1-125">建議設定強式密碼。</span><span class="sxs-lookup"><span data-stu-id="02fb1-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="02fb1-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="02fb1-126">-UPNOrObjectId</span></span>
<span data-ttu-id="02fb1-127">使用者主體名稱 (例如 " someuser@contoso.com " ) ，或是需要更新屬性之使用者的 objectId。</span><span class="sxs-lookup"><span data-stu-id="02fb1-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="02fb1-128">-確認</span><span class="sxs-lookup"><span data-stu-id="02fb1-128">-Confirm</span></span>
<span data-ttu-id="02fb1-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02fb1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02fb1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02fb1-130">-WhatIf</span></span>
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

### <span data-ttu-id="02fb1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02fb1-131">-DefaultProfile</span></span>
<span data-ttu-id="02fb1-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02fb1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02fb1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02fb1-133">CommonParameters</span></span>
<span data-ttu-id="02fb1-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02fb1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02fb1-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02fb1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02fb1-136">輸入</span><span class="sxs-lookup"><span data-stu-id="02fb1-136">INPUTS</span></span>

## <span data-ttu-id="02fb1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="02fb1-137">OUTPUTS</span></span>

### <span data-ttu-id="02fb1-138">Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser</span><span class="sxs-lookup"><span data-stu-id="02fb1-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="02fb1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="02fb1-139">NOTES</span></span>

## <span data-ttu-id="02fb1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="02fb1-140">RELATED LINKS</span></span>

[<span data-ttu-id="02fb1-141">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="02fb1-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="02fb1-142">新-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="02fb1-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="02fb1-143">移除-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="02fb1-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

