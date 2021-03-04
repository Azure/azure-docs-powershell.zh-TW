---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 4af261f10a4d5f3d7228f31b511a092600cb93bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902042"
---
# <span data-ttu-id="49320-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="49320-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="49320-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49320-102">SYNOPSIS</span></span>
<span data-ttu-id="49320-103">從備份檔案還原金鑰保存庫中的憑證。</span><span class="sxs-lookup"><span data-stu-id="49320-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="49320-104">語法</span><span class="sxs-lookup"><span data-stu-id="49320-104">SYNTAX</span></span>

### <span data-ttu-id="49320-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="49320-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49320-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="49320-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49320-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="49320-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49320-108">描述</span><span class="sxs-lookup"><span data-stu-id="49320-108">DESCRIPTION</span></span>
<span data-ttu-id="49320-109">**Restore-AzKeyVaultCertificate Cmdlet** 會從備份檔案，于指定的金鑰保存庫中建立憑證。</span><span class="sxs-lookup"><span data-stu-id="49320-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="49320-110">此憑證是輸入檔案中備份憑證的複本，其名稱與原始憑證相同。</span><span class="sxs-lookup"><span data-stu-id="49320-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="49320-111">如果金鑰庫已經包含相同名稱的憑證，此 Cmdlet 會失敗，而不會覆寫原始憑證。</span><span class="sxs-lookup"><span data-stu-id="49320-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="49320-112">如果備份包含多個版本的憑證，會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="49320-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="49320-113">您還原憑證的金鑰庫可能會與備份憑證的金鑰庫不同。</span><span class="sxs-lookup"><span data-stu-id="49320-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="49320-114">不過，金鑰庫必須使用相同的訂閱，而且位於位於相同地理位置的 Azure (例如北美地區) 。</span><span class="sxs-lookup"><span data-stu-id="49320-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="49320-115">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) Azure 區域與地理位置的相互比對。</span><span class="sxs-lookup"><span data-stu-id="49320-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="49320-116">例子</span><span class="sxs-lookup"><span data-stu-id="49320-116">EXAMPLES</span></span>

### <span data-ttu-id="49320-117">範例 1：還原備份憑證</span><span class="sxs-lookup"><span data-stu-id="49320-117">Example 1: Restore a backed-up certificate</span></span>
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

<span data-ttu-id="49320-118">此命令會從名為 Backup.blob 的備份檔案還原憑證 ，包括所有版本，到名為 MyKeyVault 的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="49320-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="49320-119">參數</span><span class="sxs-lookup"><span data-stu-id="49320-119">PARAMETERS</span></span>

### <span data-ttu-id="49320-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49320-120">-DefaultProfile</span></span>
<span data-ttu-id="49320-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49320-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49320-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="49320-122">-InputFile</span></span>
<span data-ttu-id="49320-123">輸入檔案。</span><span class="sxs-lookup"><span data-stu-id="49320-123">Input file.</span></span>
<span data-ttu-id="49320-124">包含備份 Blob 的輸入檔案</span><span class="sxs-lookup"><span data-stu-id="49320-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="49320-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49320-125">-InputObject</span></span>
<span data-ttu-id="49320-126">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="49320-126">KeyVault object</span></span>

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

### <span data-ttu-id="49320-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49320-127">-ResourceId</span></span>
<span data-ttu-id="49320-128">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="49320-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="49320-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="49320-129">-VaultName</span></span>
<span data-ttu-id="49320-130">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="49320-130">Vault name.</span></span>
<span data-ttu-id="49320-131">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="49320-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="49320-132">-確認</span><span class="sxs-lookup"><span data-stu-id="49320-132">-Confirm</span></span>
<span data-ttu-id="49320-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49320-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49320-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49320-134">-WhatIf</span></span>
<span data-ttu-id="49320-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49320-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49320-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49320-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49320-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49320-137">CommonParameters</span></span>
<span data-ttu-id="49320-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49320-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49320-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49320-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49320-140">輸入</span><span class="sxs-lookup"><span data-stu-id="49320-140">INPUTS</span></span>

### <span data-ttu-id="49320-141">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="49320-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="49320-142">System.String</span><span class="sxs-lookup"><span data-stu-id="49320-142">System.String</span></span>

## <span data-ttu-id="49320-143">輸出</span><span class="sxs-lookup"><span data-stu-id="49320-143">OUTPUTS</span></span>

### <span data-ttu-id="49320-144">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="49320-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="49320-145">筆記</span><span class="sxs-lookup"><span data-stu-id="49320-145">NOTES</span></span>

## <span data-ttu-id="49320-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="49320-146">RELATED LINKS</span></span>
