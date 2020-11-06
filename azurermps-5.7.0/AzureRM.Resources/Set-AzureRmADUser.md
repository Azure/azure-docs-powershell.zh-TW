---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444375"
---
# <span data-ttu-id="207a9-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="207a9-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="207a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="207a9-102">SYNOPSIS</span></span>
<span data-ttu-id="207a9-103">更新現有的 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="207a9-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="207a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="207a9-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="207a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="207a9-105">DESCRIPTION</span></span>
<span data-ttu-id="207a9-106">更新現有的 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="207a9-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="207a9-107">如需詳細資訊： https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="207a9-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="207a9-108">示例</span><span class="sxs-lookup"><span data-stu-id="207a9-108">EXAMPLES</span></span>

### <span data-ttu-id="207a9-109">範例1</span><span class="sxs-lookup"><span data-stu-id="207a9-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="207a9-110">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="207a9-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="207a9-111">參數</span><span class="sxs-lookup"><span data-stu-id="207a9-111">PARAMETERS</span></span>

### <span data-ttu-id="207a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="207a9-112">-DefaultProfile</span></span>
<span data-ttu-id="207a9-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="207a9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="207a9-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="207a9-114">-DisplayName</span></span>
<span data-ttu-id="207a9-115">要顯示在使用者通訊錄中的新名稱。</span><span class="sxs-lookup"><span data-stu-id="207a9-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="207a9-116">範例-'Alex Wu」。</span><span class="sxs-lookup"><span data-stu-id="207a9-116">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="207a9-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="207a9-117">-EnableAccount</span></span>
<span data-ttu-id="207a9-118">啟用帳戶的 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="207a9-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207a9-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="207a9-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="207a9-120">只有在您更新密碼時，才能指定它。</span><span class="sxs-lookup"><span data-stu-id="207a9-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="207a9-121">否則將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="207a9-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="207a9-122">如果使用者必須在下一次成功的登入 (true) 時變更密碼，則必須指定它。</span><span class="sxs-lookup"><span data-stu-id="207a9-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="207a9-123">預設行為是 (false) ，不會在下一次成功的登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="207a9-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="207a9-124">-Password</span><span class="sxs-lookup"><span data-stu-id="207a9-124">-Password</span></span>
<span data-ttu-id="207a9-125">使用者的新密碼。</span><span class="sxs-lookup"><span data-stu-id="207a9-125">New password for the user.</span></span>
<span data-ttu-id="207a9-126">它必須符合租使用者的密碼複雜性需求。</span><span class="sxs-lookup"><span data-stu-id="207a9-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="207a9-127">建議設定強式密碼。</span><span class="sxs-lookup"><span data-stu-id="207a9-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207a9-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="207a9-128">-UPNOrObjectId</span></span>
<span data-ttu-id="207a9-129">使用者主體名稱 (例如 " someuser@contoso.com " ) ，或是需要更新屬性之使用者的 objectId。</span><span class="sxs-lookup"><span data-stu-id="207a9-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="207a9-130">-確認</span><span class="sxs-lookup"><span data-stu-id="207a9-130">-Confirm</span></span>
<span data-ttu-id="207a9-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="207a9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="207a9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="207a9-132">-WhatIf</span></span>
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

### <span data-ttu-id="207a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="207a9-133">CommonParameters</span></span>
<span data-ttu-id="207a9-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="207a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="207a9-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="207a9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="207a9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="207a9-136">INPUTS</span></span>

### <span data-ttu-id="207a9-137">所有</span><span class="sxs-lookup"><span data-stu-id="207a9-137">None</span></span>
<span data-ttu-id="207a9-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="207a9-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="207a9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="207a9-139">OUTPUTS</span></span>

### <span data-ttu-id="207a9-140">Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser</span><span class="sxs-lookup"><span data-stu-id="207a9-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="207a9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="207a9-141">NOTES</span></span>

## <span data-ttu-id="207a9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="207a9-142">RELATED LINKS</span></span>

[<span data-ttu-id="207a9-143">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="207a9-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="207a9-144">新-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="207a9-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="207a9-145">移除-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="207a9-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

