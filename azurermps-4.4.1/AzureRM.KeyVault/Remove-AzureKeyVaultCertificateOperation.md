---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: d40489471e94474e83243803b5c64cdad1d572d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454368"
---
# <span data-ttu-id="60fc5-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="60fc5-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="60fc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="60fc5-103">從金鑰保存庫刪除憑證操作。</span><span class="sxs-lookup"><span data-stu-id="60fc5-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60fc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="60fc5-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60fc5-105">說明</span><span class="sxs-lookup"><span data-stu-id="60fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="60fc5-106">**AzureKeyVaultCertificateOperation** Cmdlet 會從金鑰保存庫刪除憑證操作。</span><span class="sxs-lookup"><span data-stu-id="60fc5-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="60fc5-107">示例</span><span class="sxs-lookup"><span data-stu-id="60fc5-107">EXAMPLES</span></span>

### <span data-ttu-id="60fc5-108">範例1：移除憑證操作</span><span class="sxs-lookup"><span data-stu-id="60fc5-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="60fc5-109">這個命令會從 ContosoKV01 金鑰保存庫中移除名為 TestCert01 的憑證操作，而不需確認。</span><span class="sxs-lookup"><span data-stu-id="60fc5-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="60fc5-110">參數</span><span class="sxs-lookup"><span data-stu-id="60fc5-110">PARAMETERS</span></span>

### <span data-ttu-id="60fc5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="60fc5-111">-Force</span></span>
<span data-ttu-id="60fc5-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="60fc5-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fc5-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="60fc5-113">-Name</span></span>
<span data-ttu-id="60fc5-114">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="60fc5-114">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fc5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60fc5-115">-PassThru</span></span>
<span data-ttu-id="60fc5-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="60fc5-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="60fc5-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="60fc5-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fc5-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="60fc5-118">-VaultName</span></span>
<span data-ttu-id="60fc5-119">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="60fc5-119">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fc5-120">-確認</span><span class="sxs-lookup"><span data-stu-id="60fc5-120">-Confirm</span></span>
<span data-ttu-id="60fc5-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60fc5-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fc5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60fc5-122">-WhatIf</span></span>
<span data-ttu-id="60fc5-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60fc5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60fc5-124">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60fc5-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60fc5-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60fc5-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fc5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fc5-126">-DefaultProfile</span></span>
<span data-ttu-id="60fc5-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60fc5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60fc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fc5-128">CommonParameters</span></span>
<span data-ttu-id="60fc5-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60fc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fc5-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60fc5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fc5-131">輸入</span><span class="sxs-lookup"><span data-stu-id="60fc5-131">INPUTS</span></span>

## <span data-ttu-id="60fc5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="60fc5-132">OUTPUTS</span></span>

### <span data-ttu-id="60fc5-133">KeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="60fc5-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="60fc5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="60fc5-134">NOTES</span></span>

## <span data-ttu-id="60fc5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="60fc5-135">RELATED LINKS</span></span>

[<span data-ttu-id="60fc5-136">AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="60fc5-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="60fc5-137">停止 AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="60fc5-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

