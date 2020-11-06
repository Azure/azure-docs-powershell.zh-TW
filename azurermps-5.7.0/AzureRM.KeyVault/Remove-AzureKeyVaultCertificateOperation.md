---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448646"
---
# <span data-ttu-id="a7a9c-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a7a9c-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a7a9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a9c-103">從金鑰保存庫刪除憑證操作。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7a9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7a9c-104">SYNTAX</span></span>

### <span data-ttu-id="a7a9c-105">設置</span><span class="sxs-lookup"><span data-stu-id="a7a9c-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a9c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a7a9c-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a9c-107">說明</span><span class="sxs-lookup"><span data-stu-id="a7a9c-107">DESCRIPTION</span></span>
<span data-ttu-id="a7a9c-108">**AzureKeyVaultCertificateOperation** Cmdlet 會從金鑰保存庫刪除憑證操作。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="a7a9c-109">示例</span><span class="sxs-lookup"><span data-stu-id="a7a9c-109">EXAMPLES</span></span>

### <span data-ttu-id="a7a9c-110">範例1：移除憑證操作</span><span class="sxs-lookup"><span data-stu-id="a7a9c-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="a7a9c-111">這個命令會從 ContosoKV01 金鑰保存庫中移除名為 TestCert01 的憑證操作，而不需確認。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="a7a9c-112">參數</span><span class="sxs-lookup"><span data-stu-id="a7a9c-112">PARAMETERS</span></span>

### <span data-ttu-id="a7a9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a9c-113">-DefaultProfile</span></span>
<span data-ttu-id="a7a9c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a7a9c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7a9c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a7a9c-115">-Force</span></span>
<span data-ttu-id="a7a9c-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7a9c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7a9c-117">-InputObject</span></span>
<span data-ttu-id="a7a9c-118">Operation 物件</span><span class="sxs-lookup"><span data-stu-id="a7a9c-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a9c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7a9c-119">-Name</span></span>
<span data-ttu-id="a7a9c-120">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="a7a9c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7a9c-121">-PassThru</span></span>
<span data-ttu-id="a7a9c-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a7a9c-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7a9c-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a7a9c-124">-VaultName</span></span>
<span data-ttu-id="a7a9c-125">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a7a9c-126">-確認</span><span class="sxs-lookup"><span data-stu-id="a7a9c-126">-Confirm</span></span>
<span data-ttu-id="a7a9c-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a9c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a9c-128">-WhatIf</span></span>
<span data-ttu-id="a7a9c-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a9c-130">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a9c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a9c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a9c-132">CommonParameters</span></span>
<span data-ttu-id="a7a9c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a9c-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a9c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a7a9c-135">INPUTS</span></span>

### <span data-ttu-id="a7a9c-136">所有</span><span class="sxs-lookup"><span data-stu-id="a7a9c-136">None</span></span>
<span data-ttu-id="a7a9c-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7a9c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a7a9c-138">OUTPUTS</span></span>

### <span data-ttu-id="a7a9c-139">PSKeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a7a9c-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a7a9c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a7a9c-140">NOTES</span></span>

## <span data-ttu-id="a7a9c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7a9c-141">RELATED LINKS</span></span>

[<span data-ttu-id="a7a9c-142">AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a7a9c-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="a7a9c-143">停止 AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a7a9c-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)
