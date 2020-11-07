---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7d5a575bfb5e26511f2051e8e45654af1e8c9f2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799874"
---
# <span data-ttu-id="afd66-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="afd66-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="afd66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="afd66-102">SYNOPSIS</span></span>
<span data-ttu-id="afd66-103">從金鑰保存庫刪除憑證操作。</span><span class="sxs-lookup"><span data-stu-id="afd66-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afd66-104">句法</span><span class="sxs-lookup"><span data-stu-id="afd66-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd66-105">說明</span><span class="sxs-lookup"><span data-stu-id="afd66-105">DESCRIPTION</span></span>
<span data-ttu-id="afd66-106">**AzureKeyVaultCertificateOperation** Cmdlet 會從金鑰保存庫刪除憑證操作。</span><span class="sxs-lookup"><span data-stu-id="afd66-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="afd66-107">示例</span><span class="sxs-lookup"><span data-stu-id="afd66-107">EXAMPLES</span></span>

### <span data-ttu-id="afd66-108">範例1：移除憑證操作</span><span class="sxs-lookup"><span data-stu-id="afd66-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="afd66-109">這個命令會從 ContosoKV01 金鑰保存庫中移除名為 TestCert01 的憑證操作，而不需確認。</span><span class="sxs-lookup"><span data-stu-id="afd66-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="afd66-110">參數</span><span class="sxs-lookup"><span data-stu-id="afd66-110">PARAMETERS</span></span>

### <span data-ttu-id="afd66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd66-111">-DefaultProfile</span></span>
<span data-ttu-id="afd66-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="afd66-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afd66-113">-Force</span><span class="sxs-lookup"><span data-stu-id="afd66-113">-Force</span></span>
<span data-ttu-id="afd66-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="afd66-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="afd66-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="afd66-115">-Name</span></span>
<span data-ttu-id="afd66-116">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="afd66-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="afd66-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afd66-117">-PassThru</span></span>
<span data-ttu-id="afd66-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="afd66-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="afd66-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="afd66-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="afd66-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="afd66-120">-VaultName</span></span>
<span data-ttu-id="afd66-121">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="afd66-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="afd66-122">-確認</span><span class="sxs-lookup"><span data-stu-id="afd66-122">-Confirm</span></span>
<span data-ttu-id="afd66-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="afd66-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afd66-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd66-124">-WhatIf</span></span>
<span data-ttu-id="afd66-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afd66-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd66-126">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afd66-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd66-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afd66-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afd66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd66-128">CommonParameters</span></span>
<span data-ttu-id="afd66-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="afd66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd66-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="afd66-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd66-131">輸入</span><span class="sxs-lookup"><span data-stu-id="afd66-131">INPUTS</span></span>

## <span data-ttu-id="afd66-132">輸出</span><span class="sxs-lookup"><span data-stu-id="afd66-132">OUTPUTS</span></span>

### <span data-ttu-id="afd66-133">KeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="afd66-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="afd66-134">筆記</span><span class="sxs-lookup"><span data-stu-id="afd66-134">NOTES</span></span>

## <span data-ttu-id="afd66-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="afd66-135">RELATED LINKS</span></span>

[<span data-ttu-id="afd66-136">AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="afd66-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="afd66-137">停止 AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="afd66-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

