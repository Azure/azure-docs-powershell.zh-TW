---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795520"
---
# <span data-ttu-id="036d2-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="036d2-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="036d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="036d2-102">SYNOPSIS</span></span>
<span data-ttu-id="036d2-103">將 [金鑰 vault] 中已刪除的機密恢復為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="036d2-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="036d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="036d2-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="036d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="036d2-105">DESCRIPTION</span></span>
<span data-ttu-id="036d2-106">**Undo AzKeyVaultSecretRemoval** Cmdlet 會復原先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="036d2-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="036d2-107">復原的秘密將是作用中的，而且可用於所有正常的機密作業。</span><span class="sxs-lookup"><span data-stu-id="036d2-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="036d2-108">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="036d2-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="036d2-109">示例</span><span class="sxs-lookup"><span data-stu-id="036d2-109">EXAMPLES</span></span>

### <span data-ttu-id="036d2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="036d2-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="036d2-111">這個命令會將先前刪除的秘密「MySecret」復原成作用中且可用的狀態。</span><span class="sxs-lookup"><span data-stu-id="036d2-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="036d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="036d2-112">PARAMETERS</span></span>

### <span data-ttu-id="036d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036d2-113">-DefaultProfile</span></span>
<span data-ttu-id="036d2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="036d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="036d2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="036d2-115">-Name</span></span>
<span data-ttu-id="036d2-116">[秘密名稱]。</span><span class="sxs-lookup"><span data-stu-id="036d2-116">Secret name.</span></span>
<span data-ttu-id="036d2-117">Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="036d2-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036d2-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="036d2-118">-VaultName</span></span>
<span data-ttu-id="036d2-119">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="036d2-119">Vault name.</span></span>
<span data-ttu-id="036d2-120">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="036d2-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="036d2-121">-確認</span><span class="sxs-lookup"><span data-stu-id="036d2-121">-Confirm</span></span>
<span data-ttu-id="036d2-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="036d2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="036d2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="036d2-123">-WhatIf</span></span>
<span data-ttu-id="036d2-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="036d2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="036d2-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="036d2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="036d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036d2-126">CommonParameters</span></span>
<span data-ttu-id="036d2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="036d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036d2-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="036d2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036d2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="036d2-129">INPUTS</span></span>

### <span data-ttu-id="036d2-130">System.object</span><span class="sxs-lookup"><span data-stu-id="036d2-130">System.String</span></span>

## <span data-ttu-id="036d2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="036d2-131">OUTPUTS</span></span>

### <span data-ttu-id="036d2-132">KeyVault （密碼）。</span><span class="sxs-lookup"><span data-stu-id="036d2-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="036d2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="036d2-133">NOTES</span></span>

## <span data-ttu-id="036d2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="036d2-134">RELATED LINKS</span></span>

[<span data-ttu-id="036d2-135">移除-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="036d2-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="036d2-136">附加 AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="036d2-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="036d2-137">AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="036d2-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
