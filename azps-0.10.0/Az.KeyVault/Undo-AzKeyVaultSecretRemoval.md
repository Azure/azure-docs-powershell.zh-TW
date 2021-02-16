---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9c240d3902aeba38af4281ba31bacea76bad0a58
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399085"
---
# <span data-ttu-id="50753-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="50753-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="50753-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50753-102">SYNOPSIS</span></span>
<span data-ttu-id="50753-103">將金鑰庫中已刪除的機密復原為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="50753-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="50753-104">語法</span><span class="sxs-lookup"><span data-stu-id="50753-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50753-105">描述</span><span class="sxs-lookup"><span data-stu-id="50753-105">DESCRIPTION</span></span>
<span data-ttu-id="50753-106">**Undo-AzKeyVaultSecretRemoval** Cmdlet 會復原先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="50753-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="50753-107">已復原的機密將會為使用中，而且可用於所有一般機密作業。</span><span class="sxs-lookup"><span data-stu-id="50753-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="50753-108">來電者必須擁有復原許可權，才能執行此作業。</span><span class="sxs-lookup"><span data-stu-id="50753-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="50753-109">例子</span><span class="sxs-lookup"><span data-stu-id="50753-109">EXAMPLES</span></span>

### <span data-ttu-id="50753-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="50753-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="50753-111">此命令將會將先前刪除的機密 MySecret 復原為使用中且可使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="50753-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="50753-112">參數</span><span class="sxs-lookup"><span data-stu-id="50753-112">PARAMETERS</span></span>

### <span data-ttu-id="50753-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50753-113">-DefaultProfile</span></span>
<span data-ttu-id="50753-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="50753-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50753-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="50753-115">-Name</span></span>
<span data-ttu-id="50753-116">機密名稱。</span><span class="sxs-lookup"><span data-stu-id="50753-116">Secret name.</span></span>
<span data-ttu-id="50753-117">Cmdlet 會從儲存庫名稱、目前選取的環境和機密名稱建構一個機密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="50753-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="50753-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="50753-118">-VaultName</span></span>
<span data-ttu-id="50753-119">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="50753-119">Vault name.</span></span>
<span data-ttu-id="50753-120">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="50753-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="50753-121">-確認</span><span class="sxs-lookup"><span data-stu-id="50753-121">-Confirm</span></span>
<span data-ttu-id="50753-122">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="50753-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50753-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50753-123">-WhatIf</span></span>
<span data-ttu-id="50753-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50753-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50753-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50753-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50753-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50753-126">CommonParameters</span></span>
<span data-ttu-id="50753-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50753-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50753-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="50753-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50753-129">輸入</span><span class="sxs-lookup"><span data-stu-id="50753-129">INPUTS</span></span>

### <span data-ttu-id="50753-130">System.String</span><span class="sxs-lookup"><span data-stu-id="50753-130">System.String</span></span>

## <span data-ttu-id="50753-131">輸出</span><span class="sxs-lookup"><span data-stu-id="50753-131">OUTPUTS</span></span>

### <span data-ttu-id="50753-132">Microsoft.Azure.Commands.KeyVault.models.Secret</span><span class="sxs-lookup"><span data-stu-id="50753-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="50753-133">筆記</span><span class="sxs-lookup"><span data-stu-id="50753-133">NOTES</span></span>

## <span data-ttu-id="50753-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="50753-134">RELATED LINKS</span></span>

[<span data-ttu-id="50753-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="50753-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="50753-136">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="50753-136">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
