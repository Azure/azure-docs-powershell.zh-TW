---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 33024ce7002975848a98ff8bdfd6188196a96e6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625894"
---
# <span data-ttu-id="ac76a-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="ac76a-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="ac76a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac76a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac76a-103">將 [金鑰 vault] 中已刪除的憑證恢復為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="ac76a-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac76a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac76a-104">SYNTAX</span></span>

### <span data-ttu-id="ac76a-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="ac76a-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac76a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ac76a-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac76a-107">說明</span><span class="sxs-lookup"><span data-stu-id="ac76a-107">DESCRIPTION</span></span>
<span data-ttu-id="ac76a-108">**Undo AzureKeyVaultCertificateRemoval** Cmdlet 會復原先前刪除的憑證。</span><span class="sxs-lookup"><span data-stu-id="ac76a-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="ac76a-109">復原的憑證將是作用中的，可用於所有作業。</span><span class="sxs-lookup"><span data-stu-id="ac76a-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="ac76a-110">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="ac76a-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ac76a-111">示例</span><span class="sxs-lookup"><span data-stu-id="ac76a-111">EXAMPLES</span></span>

### <span data-ttu-id="ac76a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ac76a-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="ac76a-113">這個命令會將先前已刪除的憑證 ' MyCertificate ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="ac76a-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ac76a-114">參數</span><span class="sxs-lookup"><span data-stu-id="ac76a-114">PARAMETERS</span></span>

### <span data-ttu-id="ac76a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac76a-115">-DefaultProfile</span></span>
<span data-ttu-id="ac76a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ac76a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac76a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac76a-117">-InputObject</span></span>
<span data-ttu-id="ac76a-118">已刪除的憑證物件</span><span class="sxs-lookup"><span data-stu-id="ac76a-118">Deleted Certificate object</span></span>

```yaml
Type: PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac76a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac76a-119">-Name</span></span>
<span data-ttu-id="ac76a-120">憑證名。</span><span class="sxs-lookup"><span data-stu-id="ac76a-120">Certificate name.</span></span>
<span data-ttu-id="ac76a-121">Cmdlet 會從保存庫名稱、目前已選取的 [環境] 和 [憑證名稱] 構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ac76a-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac76a-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ac76a-122">-VaultName</span></span>
<span data-ttu-id="ac76a-123">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ac76a-123">Vault name.</span></span>
<span data-ttu-id="ac76a-124">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ac76a-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac76a-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ac76a-125">-Confirm</span></span>
<span data-ttu-id="ac76a-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac76a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac76a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac76a-127">-WhatIf</span></span>
<span data-ttu-id="ac76a-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac76a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac76a-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac76a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac76a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac76a-130">CommonParameters</span></span>
<span data-ttu-id="ac76a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac76a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac76a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac76a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac76a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ac76a-133">INPUTS</span></span>

### <span data-ttu-id="ac76a-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ac76a-134">System.String</span></span>

## <span data-ttu-id="ac76a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ac76a-135">OUTPUTS</span></span>

### <span data-ttu-id="ac76a-136">CertificateBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="ac76a-136">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="ac76a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ac76a-137">NOTES</span></span>

## <span data-ttu-id="ac76a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac76a-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac76a-139">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ac76a-139">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ac76a-140">AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ac76a-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
