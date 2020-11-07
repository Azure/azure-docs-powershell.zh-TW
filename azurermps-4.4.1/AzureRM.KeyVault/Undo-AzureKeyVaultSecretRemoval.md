---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: e71fa3098003f6fb713c90903eee6e97ca4f42ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625168"
---
# <span data-ttu-id="03a81-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="03a81-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="03a81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03a81-102">SYNOPSIS</span></span>
<span data-ttu-id="03a81-103">將 [金鑰 vault] 中已刪除的機密恢復為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="03a81-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03a81-104">句法</span><span class="sxs-lookup"><span data-stu-id="03a81-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a81-105">說明</span><span class="sxs-lookup"><span data-stu-id="03a81-105">DESCRIPTION</span></span>
<span data-ttu-id="03a81-106">**Undo AzureKeyVaultSecretRemoval** Cmdlet 會復原先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="03a81-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="03a81-107">復原的秘密將是作用中的，而且可用於所有正常的機密作業。</span><span class="sxs-lookup"><span data-stu-id="03a81-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="03a81-108">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="03a81-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="03a81-109">示例</span><span class="sxs-lookup"><span data-stu-id="03a81-109">EXAMPLES</span></span>

### <span data-ttu-id="03a81-110">範例1</span><span class="sxs-lookup"><span data-stu-id="03a81-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="03a81-111">這個命令會將先前刪除的秘密「MySecret」復原成作用中且可用的狀態。</span><span class="sxs-lookup"><span data-stu-id="03a81-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="03a81-112">參數</span><span class="sxs-lookup"><span data-stu-id="03a81-112">PARAMETERS</span></span>

### <span data-ttu-id="03a81-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="03a81-113">-Name</span></span>
<span data-ttu-id="03a81-114">[秘密名稱]。</span><span class="sxs-lookup"><span data-stu-id="03a81-114">Secret name.</span></span>
<span data-ttu-id="03a81-115">Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="03a81-115">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a81-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="03a81-116">-VaultName</span></span>
<span data-ttu-id="03a81-117">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="03a81-117">Vault name.</span></span>
<span data-ttu-id="03a81-118">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="03a81-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a81-119">-確認</span><span class="sxs-lookup"><span data-stu-id="03a81-119">-Confirm</span></span>
<span data-ttu-id="03a81-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03a81-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03a81-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a81-121">-WhatIf</span></span>
<span data-ttu-id="03a81-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03a81-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a81-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03a81-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03a81-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a81-124">-DefaultProfile</span></span>
<span data-ttu-id="03a81-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03a81-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03a81-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a81-126">CommonParameters</span></span>
<span data-ttu-id="03a81-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03a81-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a81-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03a81-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a81-129">輸入</span><span class="sxs-lookup"><span data-stu-id="03a81-129">INPUTS</span></span>

### <span data-ttu-id="03a81-130">System.object</span><span class="sxs-lookup"><span data-stu-id="03a81-130">System.String</span></span>

## <span data-ttu-id="03a81-131">輸出</span><span class="sxs-lookup"><span data-stu-id="03a81-131">OUTPUTS</span></span>

### <span data-ttu-id="03a81-132">KeyVault （密碼）。</span><span class="sxs-lookup"><span data-stu-id="03a81-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="03a81-133">筆記</span><span class="sxs-lookup"><span data-stu-id="03a81-133">NOTES</span></span>

## <span data-ttu-id="03a81-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="03a81-134">RELATED LINKS</span></span>

[<span data-ttu-id="03a81-135">移除-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03a81-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="03a81-136">附加 AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03a81-136">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="03a81-137">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03a81-137">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
