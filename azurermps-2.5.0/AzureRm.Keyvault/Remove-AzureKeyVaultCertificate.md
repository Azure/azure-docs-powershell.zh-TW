---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799893"
---
# <span data-ttu-id="59fcd-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="59fcd-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="59fcd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="59fcd-103">移除金鑰保存庫的憑證。</span><span class="sxs-lookup"><span data-stu-id="59fcd-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fcd-104">句法</span><span class="sxs-lookup"><span data-stu-id="59fcd-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59fcd-105">說明</span><span class="sxs-lookup"><span data-stu-id="59fcd-105">DESCRIPTION</span></span>
<span data-ttu-id="59fcd-106">**AzureKeyVaultCertificate** Cmdlet 會從金鑰保存庫中移除憑證。</span><span class="sxs-lookup"><span data-stu-id="59fcd-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="59fcd-107">示例</span><span class="sxs-lookup"><span data-stu-id="59fcd-107">EXAMPLES</span></span>

### <span data-ttu-id="59fcd-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="59fcd-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="59fcd-109">這個命令會從名為 ContosoKV01 的主要電子倉庫中移除名為 SelfSigned01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="59fcd-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="59fcd-110">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="59fcd-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="59fcd-111">因此，Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59fcd-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="59fcd-112">範例3：從金鑰保存庫永久清除已刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="59fcd-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="59fcd-113">這個命令會永久移除名為「Contoso」的金鑰保存庫中名為「MyCert」的憑證。</span><span class="sxs-lookup"><span data-stu-id="59fcd-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="59fcd-114">執行此 Cmdlet 需要「清除」許可權，該許可權必須在此金鑰保存庫上預先授與使用者。</span><span class="sxs-lookup"><span data-stu-id="59fcd-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="59fcd-115">參數</span><span class="sxs-lookup"><span data-stu-id="59fcd-115">PARAMETERS</span></span>

### <span data-ttu-id="59fcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fcd-116">-DefaultProfile</span></span>
<span data-ttu-id="59fcd-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="59fcd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59fcd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="59fcd-118">-Force</span></span>
<span data-ttu-id="59fcd-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="59fcd-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fcd-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="59fcd-120">-InRemovedState</span></span>
<span data-ttu-id="59fcd-121">如果有，則會永久移除先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="59fcd-121">If present, removes the previously deleted certificate permanently</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fcd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="59fcd-122">-Name</span></span>
<span data-ttu-id="59fcd-123">指定此 Cmdlet 從金鑰保存庫移除之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="59fcd-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="59fcd-124">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造完整的功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="59fcd-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fcd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59fcd-125">-PassThru</span></span>
<span data-ttu-id="59fcd-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="59fcd-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59fcd-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="59fcd-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fcd-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="59fcd-128">-VaultName</span></span>
<span data-ttu-id="59fcd-129">指定此 Cmdlet 移除憑證的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="59fcd-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="59fcd-130">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="59fcd-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="59fcd-131">-確認</span><span class="sxs-lookup"><span data-stu-id="59fcd-131">-Confirm</span></span>
<span data-ttu-id="59fcd-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59fcd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fcd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59fcd-133">-WhatIf</span></span>
<span data-ttu-id="59fcd-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59fcd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59fcd-135">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59fcd-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59fcd-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59fcd-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fcd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fcd-137">CommonParameters</span></span>
<span data-ttu-id="59fcd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59fcd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fcd-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59fcd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fcd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="59fcd-140">INPUTS</span></span>

## <span data-ttu-id="59fcd-141">輸出</span><span class="sxs-lookup"><span data-stu-id="59fcd-141">OUTPUTS</span></span>

### <span data-ttu-id="59fcd-142">CertificateBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="59fcd-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="59fcd-143">筆記</span><span class="sxs-lookup"><span data-stu-id="59fcd-143">NOTES</span></span>

## <span data-ttu-id="59fcd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="59fcd-144">RELATED LINKS</span></span>

[<span data-ttu-id="59fcd-145">附加 AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="59fcd-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="59fcd-146">AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="59fcd-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="59fcd-147">匯入-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="59fcd-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="59fcd-148">復原-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="59fcd-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
