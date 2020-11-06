---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 91fee65a201de8babc7ef7aa09973f1e98f95cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455740"
---
# <span data-ttu-id="65d0e-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="65d0e-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="65d0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="65d0e-103">將 [金鑰 vault] 中已刪除的憑證恢復為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="65d0e-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="65d0e-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d0e-105">說明</span><span class="sxs-lookup"><span data-stu-id="65d0e-105">DESCRIPTION</span></span>
<span data-ttu-id="65d0e-106">**Undo AzureKeyVaultCertificateRemoval** Cmdlet 會復原先前刪除的憑證。</span><span class="sxs-lookup"><span data-stu-id="65d0e-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="65d0e-107">復原的憑證將是作用中的，可用於所有作業。</span><span class="sxs-lookup"><span data-stu-id="65d0e-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="65d0e-108">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="65d0e-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="65d0e-109">示例</span><span class="sxs-lookup"><span data-stu-id="65d0e-109">EXAMPLES</span></span>

### <span data-ttu-id="65d0e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="65d0e-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="65d0e-111">這個命令會將先前已刪除的憑證 ' MyCertificate ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="65d0e-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="65d0e-112">參數</span><span class="sxs-lookup"><span data-stu-id="65d0e-112">PARAMETERS</span></span>

### <span data-ttu-id="65d0e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="65d0e-113">-Name</span></span>
<span data-ttu-id="65d0e-114">憑證名。</span><span class="sxs-lookup"><span data-stu-id="65d0e-114">Certificate name.</span></span>
<span data-ttu-id="65d0e-115">Cmdlet 會從保存庫名稱、目前已選取的 [環境] 和 [憑證名稱] 構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="65d0e-115">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d0e-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="65d0e-116">-VaultName</span></span>
<span data-ttu-id="65d0e-117">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="65d0e-117">Vault name.</span></span>
<span data-ttu-id="65d0e-118">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="65d0e-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="65d0e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="65d0e-119">-Confirm</span></span>
<span data-ttu-id="65d0e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="65d0e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d0e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d0e-121">-WhatIf</span></span>
<span data-ttu-id="65d0e-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65d0e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d0e-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65d0e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d0e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d0e-124">-DefaultProfile</span></span>
<span data-ttu-id="65d0e-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65d0e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65d0e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d0e-126">CommonParameters</span></span>
<span data-ttu-id="65d0e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65d0e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d0e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65d0e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d0e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="65d0e-129">INPUTS</span></span>

### <span data-ttu-id="65d0e-130">System.object</span><span class="sxs-lookup"><span data-stu-id="65d0e-130">System.String</span></span>

## <span data-ttu-id="65d0e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="65d0e-131">OUTPUTS</span></span>

### <span data-ttu-id="65d0e-132">[KeyVault] 的憑證</span><span class="sxs-lookup"><span data-stu-id="65d0e-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="65d0e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="65d0e-133">NOTES</span></span>

## <span data-ttu-id="65d0e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="65d0e-134">RELATED LINKS</span></span>

[<span data-ttu-id="65d0e-135">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="65d0e-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="65d0e-136">AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="65d0e-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
