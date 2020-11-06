---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454371"
---
# <span data-ttu-id="3c442-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c442-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3c442-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c442-102">SYNOPSIS</span></span>
<span data-ttu-id="3c442-103">從金鑰保存庫刪除憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="3c442-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c442-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c442-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c442-105">說明</span><span class="sxs-lookup"><span data-stu-id="3c442-105">DESCRIPTION</span></span>
<span data-ttu-id="3c442-106">**AzureKeyVaultCertificateIssuer** Cmdlet 會從金鑰保存庫刪除憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="3c442-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="3c442-107">示例</span><span class="sxs-lookup"><span data-stu-id="3c442-107">EXAMPLES</span></span>

### <span data-ttu-id="3c442-108">範例1：移除憑證頒發者</span><span class="sxs-lookup"><span data-stu-id="3c442-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="3c442-109">這個命令會從 [ContosoKV01] 金鑰保存庫中移除名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="3c442-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="3c442-110">參數</span><span class="sxs-lookup"><span data-stu-id="3c442-110">PARAMETERS</span></span>

### <span data-ttu-id="3c442-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3c442-111">-Force</span></span>
<span data-ttu-id="3c442-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3c442-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c442-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c442-113">-Name</span></span>
<span data-ttu-id="3c442-114">指定要移除之頒發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c442-114">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c442-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c442-115">-PassThru</span></span>
<span data-ttu-id="3c442-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3c442-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c442-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3c442-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c442-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3c442-118">-VaultName</span></span>
<span data-ttu-id="3c442-119">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c442-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3c442-120">-確認</span><span class="sxs-lookup"><span data-stu-id="3c442-120">-Confirm</span></span>
<span data-ttu-id="3c442-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3c442-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c442-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c442-122">-WhatIf</span></span>
<span data-ttu-id="3c442-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c442-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c442-124">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c442-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c442-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c442-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c442-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c442-126">-DefaultProfile</span></span>
<span data-ttu-id="3c442-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c442-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c442-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c442-128">CommonParameters</span></span>
<span data-ttu-id="3c442-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c442-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c442-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c442-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c442-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3c442-131">INPUTS</span></span>

## <span data-ttu-id="3c442-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3c442-132">OUTPUTS</span></span>

### <span data-ttu-id="3c442-133">KeyVaultCertificateIssuer 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="3c442-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3c442-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3c442-134">NOTES</span></span>

## <span data-ttu-id="3c442-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c442-135">RELATED LINKS</span></span>

[<span data-ttu-id="3c442-136">AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c442-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="3c442-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c442-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


