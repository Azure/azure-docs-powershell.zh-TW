---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc49237d4722384d04228d3b8e9736411ed41bde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624164"
---
# <span data-ttu-id="dc4c5-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="dc4c5-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="dc4c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="dc4c5-103">從金鑰保存庫刪除憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc4c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc4c5-104">SYNTAX</span></span>

### <span data-ttu-id="dc4c5-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="dc4c5-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc4c5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dc4c5-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc4c5-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc4c5-107">DESCRIPTION</span></span>
<span data-ttu-id="dc4c5-108">**AzureKeyVaultCertificateIssuer** Cmdlet 會從金鑰保存庫刪除憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="dc4c5-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc4c5-109">EXAMPLES</span></span>

### <span data-ttu-id="dc4c5-110">範例1：移除憑證頒發者</span><span class="sxs-lookup"><span data-stu-id="dc4c5-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="dc4c5-111">這個命令會從 [ContosoKV01] 金鑰保存庫中移除名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="dc4c5-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc4c5-112">PARAMETERS</span></span>

### <span data-ttu-id="dc4c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc4c5-113">-DefaultProfile</span></span>
<span data-ttu-id="dc4c5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dc4c5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc4c5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dc4c5-115">-Force</span></span>
<span data-ttu-id="dc4c5-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc4c5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc4c5-117">-InputObject</span></span>
<span data-ttu-id="dc4c5-118">憑證簽發者物件</span><span class="sxs-lookup"><span data-stu-id="dc4c5-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc4c5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc4c5-119">-Name</span></span>
<span data-ttu-id="dc4c5-120">指定要移除之頒發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4c5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc4c5-121">-PassThru</span></span>
<span data-ttu-id="dc4c5-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dc4c5-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc4c5-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dc4c5-124">-VaultName</span></span>
<span data-ttu-id="dc4c5-125">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4c5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="dc4c5-126">-Confirm</span></span>
<span data-ttu-id="dc4c5-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc4c5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc4c5-128">-WhatIf</span></span>
<span data-ttu-id="dc4c5-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc4c5-130">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc4c5-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc4c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc4c5-132">CommonParameters</span></span>
<span data-ttu-id="dc4c5-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc4c5-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc4c5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="dc4c5-135">INPUTS</span></span>

### <span data-ttu-id="dc4c5-136">PSKeyVaultCertificateIssuerIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="dc4c5-137">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="dc4c5-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dc4c5-138">輸出</span><span class="sxs-lookup"><span data-stu-id="dc4c5-138">OUTPUTS</span></span>

### <span data-ttu-id="dc4c5-139">PSKeyVaultCertificateIssuer 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="dc4c5-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="dc4c5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="dc4c5-140">NOTES</span></span>

## <span data-ttu-id="dc4c5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc4c5-141">RELATED LINKS</span></span>

[<span data-ttu-id="dc4c5-142">AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="dc4c5-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="dc4c5-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="dc4c5-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


