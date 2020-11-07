---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: b2e7264b5c0f54f18e295a86f9abb1cbd51dc4b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794665"
---
# <span data-ttu-id="b88c1-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b88c1-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="b88c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b88c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b88c1-103">移除金鑰保存庫的憑證。</span><span class="sxs-lookup"><span data-stu-id="b88c1-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="b88c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b88c1-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b88c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="b88c1-105">DESCRIPTION</span></span>
<span data-ttu-id="b88c1-106">**AzKeyVaultCertificate** Cmdlet 會從金鑰保存庫中移除憑證。</span><span class="sxs-lookup"><span data-stu-id="b88c1-106">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="b88c1-107">示例</span><span class="sxs-lookup"><span data-stu-id="b88c1-107">EXAMPLES</span></span>

### <span data-ttu-id="b88c1-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="b88c1-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="b88c1-109">這個命令會從名為 ContosoKV01 的主要電子倉庫中移除名為 SelfSigned01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="b88c1-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="b88c1-110">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="b88c1-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b88c1-111">因此，Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b88c1-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="b88c1-112">範例3：從金鑰保存庫永久清除已刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="b88c1-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="b88c1-113">這個命令會永久移除名為「Contoso」的金鑰保存庫中名為「MyCert」的憑證。</span><span class="sxs-lookup"><span data-stu-id="b88c1-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="b88c1-114">執行此 Cmdlet 需要「清除」許可權，該許可權必須在此金鑰保存庫上預先授與使用者。</span><span class="sxs-lookup"><span data-stu-id="b88c1-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="b88c1-115">參數</span><span class="sxs-lookup"><span data-stu-id="b88c1-115">PARAMETERS</span></span>

### <span data-ttu-id="b88c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88c1-116">-DefaultProfile</span></span>
<span data-ttu-id="b88c1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b88c1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b88c1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b88c1-118">-Force</span></span>
<span data-ttu-id="b88c1-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b88c1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b88c1-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b88c1-120">-InRemovedState</span></span>
<span data-ttu-id="b88c1-121">如果有，則會永久移除先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="b88c1-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="b88c1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b88c1-122">-Name</span></span>
<span data-ttu-id="b88c1-123">指定此 Cmdlet 從金鑰保存庫移除之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="b88c1-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="b88c1-124">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造完整的功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="b88c1-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="b88c1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b88c1-125">-PassThru</span></span>
<span data-ttu-id="b88c1-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b88c1-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b88c1-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b88c1-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b88c1-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b88c1-128">-VaultName</span></span>
<span data-ttu-id="b88c1-129">指定此 Cmdlet 移除憑證的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b88c1-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="b88c1-130">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b88c1-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="b88c1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b88c1-131">-Confirm</span></span>
<span data-ttu-id="b88c1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b88c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b88c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b88c1-133">-WhatIf</span></span>
<span data-ttu-id="b88c1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b88c1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b88c1-135">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b88c1-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b88c1-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b88c1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b88c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88c1-137">CommonParameters</span></span>
<span data-ttu-id="b88c1-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b88c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88c1-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b88c1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88c1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b88c1-140">INPUTS</span></span>

### <span data-ttu-id="b88c1-141">所有</span><span class="sxs-lookup"><span data-stu-id="b88c1-141">None</span></span>
<span data-ttu-id="b88c1-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b88c1-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b88c1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b88c1-143">OUTPUTS</span></span>

### <span data-ttu-id="b88c1-144">CertificateBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="b88c1-144">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="b88c1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b88c1-145">NOTES</span></span>

## <span data-ttu-id="b88c1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b88c1-146">RELATED LINKS</span></span>

[<span data-ttu-id="b88c1-147">附加 AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b88c1-147">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="b88c1-148">AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b88c1-148">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="b88c1-149">匯入-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b88c1-149">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="b88c1-150">復原-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="b88c1-150">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
