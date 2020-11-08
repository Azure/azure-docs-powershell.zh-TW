---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140495"
---
# <span data-ttu-id="a8dd0-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a8dd0-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="a8dd0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="a8dd0-103">從備份檔案還原金鑰保存庫中的憑證。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="a8dd0-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8dd0-104">SYNTAX</span></span>

### <span data-ttu-id="a8dd0-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="a8dd0-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8dd0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a8dd0-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8dd0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8dd0-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8dd0-108">說明</span><span class="sxs-lookup"><span data-stu-id="a8dd0-108">DESCRIPTION</span></span>
<span data-ttu-id="a8dd0-109">**Restore-AzKeyVaultCertificate** Cmdlet 會從備份檔案在指定的金鑰保存庫中建立證書。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="a8dd0-110">這個憑證是輸入檔案中已備份憑證的複本，且與原始憑證的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="a8dd0-111">如果 [主要電子倉庫] 已包含相同名稱的憑證，這個 Cmdlet 會失敗，而不會覆寫原始憑證。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="a8dd0-112">如果備份包含多個版本的憑證，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="a8dd0-113">您將憑證還原到哪個主要電子倉庫，可能會與您在其中備份憑證的主要電子倉庫不同。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="a8dd0-114">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="a8dd0-115">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="a8dd0-116">示例</span><span class="sxs-lookup"><span data-stu-id="a8dd0-116">EXAMPLES</span></span>

### <span data-ttu-id="a8dd0-117">範例1：還原已備份的憑證</span><span class="sxs-lookup"><span data-stu-id="a8dd0-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="a8dd0-118">這個命令會將憑證（包含其所有版本）從名為 MyKeyVault 的金鑰保存庫中的備份檔案還原。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="a8dd0-119">參數</span><span class="sxs-lookup"><span data-stu-id="a8dd0-119">PARAMETERS</span></span>

### <span data-ttu-id="a8dd0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8dd0-120">-DefaultProfile</span></span>
<span data-ttu-id="a8dd0-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dd0-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a8dd0-122">-InputFile</span></span>
<span data-ttu-id="a8dd0-123">輸入檔。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-123">Input file.</span></span>
<span data-ttu-id="a8dd0-124">包含已備份 blob 的輸入檔</span><span class="sxs-lookup"><span data-stu-id="a8dd0-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dd0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8dd0-125">-InputObject</span></span>
<span data-ttu-id="a8dd0-126">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="a8dd0-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8dd0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8dd0-127">-ResourceId</span></span>
<span data-ttu-id="a8dd0-128">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a8dd0-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8dd0-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a8dd0-129">-VaultName</span></span>
<span data-ttu-id="a8dd0-130">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-130">Vault name.</span></span>
<span data-ttu-id="a8dd0-131">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dd0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a8dd0-132">-Confirm</span></span>
<span data-ttu-id="a8dd0-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8dd0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8dd0-134">-WhatIf</span></span>
<span data-ttu-id="a8dd0-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8dd0-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8dd0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8dd0-137">CommonParameters</span></span>
<span data-ttu-id="a8dd0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8dd0-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8dd0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a8dd0-140">INPUTS</span></span>

### <span data-ttu-id="a8dd0-141">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a8dd0-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a8dd0-142">System.String</span></span>

## <span data-ttu-id="a8dd0-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a8dd0-143">OUTPUTS</span></span>

### <span data-ttu-id="a8dd0-144">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a8dd0-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="a8dd0-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a8dd0-145">NOTES</span></span>

## <span data-ttu-id="a8dd0-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8dd0-146">RELATED LINKS</span></span>
