---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800941"
---
# <span data-ttu-id="2ff3c-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="2ff3c-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="2ff3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ff3c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff3c-103">將 [金鑰 vault] 中已刪除的憑證恢復為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ff3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ff3c-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ff3c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff3c-106">**Undo AzureKeyVaultCertificateRemoval** Cmdlet 會復原先前刪除的憑證。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="2ff3c-107">復原的憑證將是作用中的，可用於所有作業。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="2ff3c-108">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="2ff3c-109">示例</span><span class="sxs-lookup"><span data-stu-id="2ff3c-109">EXAMPLES</span></span>

### <span data-ttu-id="2ff3c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2ff3c-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="2ff3c-111">這個命令會將先前已刪除的憑證 ' MyCertificate ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="2ff3c-112">參數</span><span class="sxs-lookup"><span data-stu-id="2ff3c-112">PARAMETERS</span></span>

### <span data-ttu-id="2ff3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff3c-113">-DefaultProfile</span></span>
<span data-ttu-id="2ff3c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2ff3c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ff3c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ff3c-115">-Name</span></span>
<span data-ttu-id="2ff3c-116">憑證名。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-116">Certificate name.</span></span>
<span data-ttu-id="2ff3c-117">Cmdlet 會從保存庫名稱、目前已選取的 [環境] 和 [憑證名稱] 構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff3c-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2ff3c-118">-VaultName</span></span>
<span data-ttu-id="2ff3c-119">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-119">Vault name.</span></span>
<span data-ttu-id="2ff3c-120">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2ff3c-121">-確認</span><span class="sxs-lookup"><span data-stu-id="2ff3c-121">-Confirm</span></span>
<span data-ttu-id="2ff3c-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff3c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff3c-123">-WhatIf</span></span>
<span data-ttu-id="2ff3c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff3c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff3c-126">CommonParameters</span></span>
<span data-ttu-id="2ff3c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff3c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ff3c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff3c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2ff3c-129">INPUTS</span></span>

### <span data-ttu-id="2ff3c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="2ff3c-130">System.String</span></span>

## <span data-ttu-id="2ff3c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2ff3c-131">OUTPUTS</span></span>

### <span data-ttu-id="2ff3c-132">[KeyVault] 的憑證</span><span class="sxs-lookup"><span data-stu-id="2ff3c-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="2ff3c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2ff3c-133">NOTES</span></span>

## <span data-ttu-id="2ff3c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ff3c-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ff3c-135">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2ff3c-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="2ff3c-136">AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2ff3c-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
